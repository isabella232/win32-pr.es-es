---
title: Tendencia de profundidad
description: Los polígonos que se coplanan en el espacio 3D pueden crearse como si no fueran coplanares agregando un sesgo z (o una diferencia de profundidad) a cada uno de ellos.
ms.assetid: ee904316-dc6d-48a4-bdb7-0f7dcdb9d9d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d6f9a3850b03e033a90b358d0c6ffd1ceef830f
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "103797350"
---
# <a name="depth-bias"></a>Tendencia de profundidad

Los polígonos que se coplanan en el espacio 3D pueden crearse como si no fueran coplanares agregando un sesgo z (o una diferencia de profundidad) a cada uno de ellos.

Se trata de una técnica que se usa normalmente para asegurarse de que las sombras de una escena se muestran correctamente. Por ejemplo, una sombra en un muro probablemente tendrá el mismo valor de profundidad que la pared. Si una aplicación representa una pared primero y después una sombra, puede que la sombra no sea visible o que los artefactos de profundidad estén visibles.


Una aplicación puede ayudar a garantizar que los polígonos coplanares se representen correctamente agregando la diferencia (del miembro **DepthBias** de [**D3D11 \_ rasterizador \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)) a los valores z que el sistema utiliza al representar los conjuntos de polígonos coplanares. Los polígonos con un valor z más grande se dibujarán delante de los polígonos con un valor z más pequeño.

Hay dos opciones para calcular la diferencia de profundidad.

1.  Si el búfer de profundidad actualmente enlazado a la fase de combinación de resultados tiene un formato **UNORM** o no hay ningún búfer de profundidad enlazado, el valor de Bias se calcula como se indica a continuación:
    ```
    Bias = (float)DepthBias * r + SlopeScaledDepthBias * MaxDepthSlope;
    ```

    

    donde *r* es el valor representable mínimo > 0 en el formato de búfer de profundidad convertido en **float32**. Los valores **DepthBias** y **SlopeScaledDepthBias** son miembros de la estructura de [**\_ rasterizador D3D11 \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1) . El valor de **MaxDepthSlope** es el máximo de las pendientes horizontal y vertical del valor de profundidad en el píxel.
2.  Si un búfer de profundidad de punto flotante se enlaza a la fase de combinación de salida, el valor de la diferencia se calcula como se indica a continuación:
    ```
    Bias = (float)DepthBias * 2**(exponent(max z in primitive) - r) +
                SlopeScaledDepthBias * MaxDepthSlope;
    ```

    

    donde *r* es el número de bits de mantisa en la representación de punto flotante (sin incluir el bit oculto); por ejemplo, 23 para **float32**.

Después, el valor de la diferencia se fija de la siguiente manera:


```
if(DepthBiasClamp > 0)
    Bias = min(DepthBiasClamp, Bias)
else if(DepthBiasClamp < 0)
    Bias = max(DepthBiasClamp, Bias)
```



A continuación, el valor de diferencia se usa para calcular la profundidad del píxel.


```
if ( (DepthBias != 0) || (SlopeScaledDepthBias != 0) )
    z = z + Bias
```



Las operaciones de diferencia de profundidad se producen en los vértices después del recorte, por lo tanto, la diferencia de profundidad no tiene ningún efecto en el recorte geométrico. El valor de Bias es constante para un primitivo determinado y se agrega al valor z para cada vértice antes de la configuración del interpolador. Cuando se usan [los niveles de características](overviews-direct3d-11-devices-downlevel-intro.md) 10,0 y posteriores, todos los cálculos de sesgo se realizan mediante aritmética de punto flotante de 32 bits. La diferencia no se aplica a los primitivos de punto o de línea, excepto en el caso de las líneas dibujadas en el modo de alambre.

Uno de los artefactos con sombras basadas en el búfer de sombra es Shadow acne, o una sombra en sí misma debido a pequeñas diferencias entre el cálculo de profundidad en un sombreador y la profundidad de la misma superficie en el búfer de la sombra. Una manera de solucionar esto es usar **DepthBias** y **SlopeScaledDepthBias** al representar un búfer de sombra. La idea es que las superficies se inserten lo suficiente al representar un búfer de sombra, de modo que el resultado de la comparación (entre el búfer de la sombra z y el sombreador z) sea coherente en toda la superficie y evitar la sombra automática local.

Sin embargo, el uso de **DepthBias** y **SlopeScaledDepthBias** puede introducir nuevos problemas de representación cuando un polígono visto en un ángulo muy nítido hace que la ecuación de diferencia genere un valor z muy grande. Esto, de hecho, empuja el polígono muy lejos de la superficie original en la instantánea. Una manera de ayudar a mitigar este problema concreto es usar **DepthBiasClamp**, que proporciona un límite superior (positivo o negativo) en la magnitud de la diferencia de z calculada.

> [!Note]  
> No se admiten [los niveles de características](overviews-direct3d-11-devices-downlevel-intro.md) 9,1, 9,2, 9,3, **DepthBiasClamp** .

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Fase de combinación de salida](d3d10-graphics-programming-guide-output-merger-stage.md)
</dt> </dl>

 

 




