---
title: Optimizar los sombreadores HLSL
description: En esta sección se describen las estrategias de uso general que puede usar para optimizar los sombreadores. Puede aplicar estas estrategias a los sombreadores que se escriben en cualquier lenguaje, en cualquier plataforma.
ms.assetid: 014b9cb3-a489-48d7-8174-b97de168bf3a
keywords:
- lenguaje de sombreador de alto nivel
- HLSL, rendimiento
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 06d3bb806e98e489020aa1755ef2a6c952459d86
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076110"
---
# <a name="optimizing-hlsl-shaders"></a>Optimizar los sombreadores HLSL

En esta sección se describen las estrategias de uso general que puede usar para optimizar los sombreadores. Puede aplicar estas estrategias a los sombreadores que se escriben en cualquier lenguaje, en cualquier plataforma.

-   [Saber dónde realizar los cálculos del sombreador](#know-where-to-perform-shader-calculations)
-   [Omitir instrucciones innecesarias](#skip-unnecessary-instructions)
-   [Variables del paquete y Interpolants](#pack-variables-and-interpolants)
-   [Reducir la complejidad del sombreador](#reduce-shader-complexity)
-   [Temas relacionados](#related-topics)
-   [Temas relacionados](#related-topics)

## <a name="know-where-to-perform-shader-calculations"></a>Saber dónde realizar los cálculos del sombreador

Los sombreadores de vértices realizan operaciones que incluyen la captura de vértices y la transformación de la matriz de datos de vértices. Normalmente, los sombreadores de vértices se ejecutan una vez por vértice.

Los sombreadores de píxeles realizan operaciones que incluyen la captura de datos de textura y la realización de cálculos de iluminación. Normalmente, los sombreadores de píxeles se ejecutan una vez por píxel para un elemento de geometría determinado.

Normalmente, los píxeles superan los vértices de una escena, por lo que los sombreadores de píxeles se ejecutan con más frecuencia que los sombreadores de vértices.

Al diseñar algoritmos de sombreador, tenga en cuenta lo siguiente:

-   Realice cálculos en el sombreador de vértices si es posible. Un cálculo que se realiza en un sombreador de píxeles es mucho más caro que un cálculo que se realiza en un sombreador de vértices.
-   Considere la posibilidad de usar cálculos por vértices para mejorar el rendimiento en situaciones como mallas densas. En el caso de las mallas densas, los cálculos por vértices pueden producir resultados que no se pueden distinguir visualmente de los resultados generados con cálculos por píxel.

## <a name="skip-unnecessary-instructions"></a>Omitir instrucciones innecesarias

En HLSL, la bifurcación dinámica proporciona la capacidad de limitar el número de instrucciones que se ejecutan. Por lo tanto, la bifurcación dinámica puede ayudar a acelerar el tiempo de ejecución del sombreador. Si no se muestran geometría o píxeles, use la bifurcación dinámica para salir del sombreador o para limitar las instrucciones. Por ejemplo, si un píxel no está iluminado, no hay ningún punto en ejecutar el algoritmo de iluminación.

En la tabla siguiente se muestran algunos casos en los que puede probar condiciones en el sombreador y usar la bifurcación dinámica para omitir las instrucciones innecesarias. La tabla no es completa. En su lugar, se pretende ofrecer ideas para optimizar el código.



| Condición para comprobar                                    | Respuesta en el sombreador       |
|-------------------------------------------------------|------------------------------|
| La comprobación alfa determina que no se verá un píxel. | Omita el resto del sombreador. |
| El píxel o la geometría están totalmente nebulizados.                | Omita el resto del sombreador. |
| Los pesos de la máscara son cero.                                | Omita los huesos.                  |
| La atenuación de luz es cero.                            | Omitir iluminación.               |
| Término Lambertian no positivo.                         | Omitir iluminación.               |



 

## <a name="pack-variables-and-interpolants"></a>Variables del paquete y Interpolants

Tenga en cuentan el espacio necesario para los datos del sombreador. Empaquete toda la información en una variable o interpolant como sea posible. A veces, la información de dos variables se puede empaquetar en el espacio de memoria de una sola variable.

## <a name="reduce-shader-complexity"></a>Reducir la complejidad del sombreador

Mantenga los sombreadores pequeños y sencillos. En general, los sombreadores con menos instrucciones se ejecutan más rápidamente que los sombreadores con más instrucciones. También es más fácil depurar y optimizar los sombreadores más pequeños y menos complejos.

## <a name="related-topics"></a>Temas relacionados

[Guía de programación para HLSL](dx-graphics-hlsl-pguide.md)


## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación para HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 




