---
description: Puede usar Microsoft Direct3D para simular fenómenos naturales que impliquen versiones de energía.
ms.assetid: a16af13d-3a38-42b5-900b-ff58a0c917b2
title: Fuego, destellos y explosiones (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 708730bd8e5f198664bb20c11fa98243ac98f0d6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805324"
---
# <a name="fire-flares-and-explosions-direct3d-9"></a>Fuego, destellos y explosiones (Direct3D 9)

Puede usar Microsoft Direct3D para simular fenómenos naturales que impliquen versiones de energía. Por ejemplo, una aplicación puede generar la apariencia del fuego aplicando texturas similares a una serie de cartelera. Esto es especialmente eficaz si la aplicación usa una secuencia de texturas de fuego para animar las llamas en cada cartelera del fuego. La variación de la velocidad de la reproducción de animaciones de la cartelera a la cartelera aumenta la apariencia de las llamas reales. El semblance de las llamas 3D entremezcladas se puede lograr mediante la disposición en capas de las cartelera y las texturas en las cartelera.

Puede simular destellos y destellos mediante la aplicación de mapas claros más brillantesmente claros a todos los primitivos de una escena. Aunque se trata de una técnica de gran sobrecarga computacional, permite que la aplicación simule un destello o Flash localizado. Es decir, la parte de la escena en la que se origina FLARE o Flash se puede aclarar primero.

Otra técnica consiste en colocar una cartelera delante de la escena para que se cubra toda la superficie de representación-destino. La aplicación aplica texturas sucesivamente a la cartelera y reduce la transparencia a lo largo del tiempo. Toda la escena se atenúa hasta el blanco a medida que pasa el tiempo. Se trata de un método bajo de sobrecarga para crear una flar. Sin embargo, con esta técnica, puede ser difícil generar la apariencia de un destello brillante a partir de una fuente de luz de un solo punto.

Las explosiones se pueden mostrar en un procedimiento de escena 3D similar a los que se usan para fuego, parpadeos e destellos. Por ejemplo, la aplicación puede usar una cartelera para mostrar una oleada de choque y aumentar la ciruela del humo cuando se produce la explosión. Al mismo tiempo, la aplicación puede usar un conjunto de cartelera para simular llamas. Además, puede colocar una sola cartelera delante de la escena para agregar un destello de luz a toda la escena.

Los haces de energía se pueden simular mediante las cartelera. La aplicación también puede mostrarlos mediante primitivas definidas como listas de líneas o bandas de líneas. Para obtener más información, consulte [listas de líneas](line-lists.md) y [franjas de líneas](line-strips.md).

La aplicación puede crear campos de fuerza mediante cartelera o primitivas definidas como listas de triángulos. Para crear un campo de fuerza a partir de las listas de triángulo, defina un conjunto de triángulos disjuntos en una lista de triángulos equidistantemente por la región incluida en el campo Force. Los huecos entre los triángulos permiten al usuario ver la escena detrás de los triángulos, como cabría esperar al mirar un campo de fuerza. Aplica una textura a la lista de triángulos que proporciona los triángulos de la apariencia del resplandor con energía. Para obtener más información, vea [listas de triángulos](triangle-lists.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos de alfa](alpha-examples.md)
</dt> </dl>

 

 



