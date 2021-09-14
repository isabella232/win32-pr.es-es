---
title: Optimización de sombreadores HLSL
description: En esta sección se describen las estrategias de uso general que puede usar para optimizar los sombreadores. Puede aplicar estas estrategias a sombreadores escritos en cualquier lenguaje, en cualquier plataforma.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127258463"
---
# <a name="optimizing-hlsl-shaders"></a>Optimización de sombreadores HLSL

En esta sección se describen las estrategias de uso general que puede usar para optimizar los sombreadores. Puede aplicar estas estrategias a sombreadores escritos en cualquier lenguaje, en cualquier plataforma.

-   [Saber dónde realizar cálculos de sombreador](#know-where-to-perform-shader-calculations)
-   [Omitir instrucciones innecesarias](#skip-unnecessary-instructions)
-   [Empaquetar variables e interpoladores](#pack-variables-and-interpolants)
-   [Reducir la complejidad del sombreador](#reduce-shader-complexity)
-   [Temas relacionados](#related-topics)
-   [Temas relacionados](#related-topics)

## <a name="know-where-to-perform-shader-calculations"></a>Saber dónde realizar cálculos de sombreador

Los sombreadores de vértices realizan operaciones que incluyen la captura de vértices y la transformación de matriz de datos de vértices. Normalmente, los sombreadores de vértices se ejecutan una vez por vértice.

Los sombreadores de píxeles realizan operaciones que incluyen la captura de datos de textura y la realización de cálculos de iluminación. Normalmente, los sombreadores de píxeles se ejecutan una vez por píxel para un fragmento de geometría determinado.

Normalmente, los píxeles superan los vértices de una escena, por lo que los sombreadores de píxeles se ejecutan con más frecuencia que los sombreadores de vértices.

Al diseñar algoritmos de sombreador, tenga en cuenta lo siguiente:

-   Realice cálculos en el sombreador de vértices si es posible. Un cálculo que se realiza en un sombreador de píxeles es mucho más costoso que un cálculo que se realiza en un sombreador de vértices.
-   Considere la posibilidad de usar cálculos por vértice para mejorar el rendimiento en situaciones como mallas densas. En el caso de las mallas densas, los cálculos por vértice pueden producir resultados que son visualmente indistinguibles a partir de los resultados generados con cálculos por píxel.

## <a name="skip-unnecessary-instructions"></a>Omitir instrucciones innecesarias

En HLSL, la bifurcación dinámica proporciona la capacidad de limitar el número de instrucciones que se ejecutan. Por lo tanto, la bifurcación dinámica puede ayudar a acelerar el tiempo de ejecución del sombreador. Si no se muestran geometría o píxeles, use la bifurcación dinámica para salir del sombreador o para limitar las instrucciones. Por ejemplo, si un píxel no está encendido, no tiene sentido ejecutar el algoritmo de iluminación.

En la tabla siguiente se enumeran algunos casos en los que puede probar las condiciones del sombreador y usar la bifurcación dinámica para omitir instrucciones innecesarias. La tabla no es completa. En su lugar, está pensado para ofrecer ideas para optimizar el código.



| Condición que se debe comprobar                                    | Respuesta en el sombreador       |
|-------------------------------------------------------|------------------------------|
| La comprobación alfa determina que no se verá un píxel. | Omita el resto del sombreador. |
| El píxel o la geometría están completamente sombreados.                | Omita el resto del sombreador. |
| Los pesos de la máscara son cero.                                | Omita los esqueletos.                  |
| La atenuación de luz es cero.                            | Omitir iluminación.               |
| Término lambertiano no positivo.                         | Omitir iluminación.               |



 

## <a name="pack-variables-and-interpolants"></a>Empaquetar variables e interpoladores

Tenga en cuenta el espacio necesario para los datos del sombreador. Empaquete tanta información en una variable o interpolante como sea posible. A veces, la información de dos variables se puede empaquetar en el espacio de memoria de una sola variable.

## <a name="reduce-shader-complexity"></a>Reducir la complejidad del sombreador

Mantenga los sombreadores pequeños y sencillos. En general, los sombreadores con menos instrucciones se ejecutan más rápidamente que los sombreadores con más instrucciones. También es más fácil depurar y optimizar sombreadores más pequeños y menos complejos.

## <a name="related-topics"></a>Temas relacionados

[Guía de programación para HLSL](dx-graphics-hlsl-pguide.md)


## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación para HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 




