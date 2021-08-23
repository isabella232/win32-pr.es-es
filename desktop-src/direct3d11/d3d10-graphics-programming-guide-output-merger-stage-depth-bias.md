---
title: Sesgo de profundidad
description: Se puede hacer que los polígonos coplanares en el espacio 3D aparezcan como si no fuera coplanar agregando un sesgo z (o sesgo de profundidad) a cada uno de ellos.
ms.assetid: ee904316-dc6d-48a4-bdb7-0f7dcdb9d9d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1f707a038a2da8ebe9c1adc21f6081c85f5a63fbbc1c360a4dfbbf5765d845d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990165"
---
# <a name="depth-bias"></a>Sesgo de profundidad

Se puede hacer que los polígonos coplanares en el espacio 3D aparezcan como si no fuera coplanar agregando un sesgo z (o sesgo de profundidad) a cada uno de ellos.

Se trata de una técnica que se usa normalmente para asegurarse de que las sombras de una escena se muestran correctamente. Por ejemplo, una sombra en una pared probablemente tendrá el mismo valor de profundidad que la pared. Si una aplicación representa primero una pared y, a continuación, una sombra, es posible que la sombra no esté visible o que los artefactos de profundidad sean visibles.


Una aplicación puede ayudar a garantizar que los polígonos coplanares se representan correctamente agregando el sesgo (del miembro **DepthBias** de [**D3D11 \_ RASTERIZER \_ DESC1)**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)a los valores z que usa el sistema al representar los conjuntos de polígonos coplanares. Los polígonos con un valor z mayor se dibujarán delante de los polígonos con un valor z más pequeño.

Hay dos opciones para calcular el sesgo de profundidad.

1.  Si el búfer de profundidad enlazado actualmente a la fase de fusión de salida tiene un formato **UNORM** o no hay ningún búfer de profundidad enlazado, el valor de sesgo se calcula de la siguiente manera:
    ```
    Bias = (float)DepthBias * r + SlopeScaledDepthBias * MaxDepthSlope;
    ```

    

    donde *r* es el valor mínimo que se puede representar > 0 en el formato de búfer de profundidad convertido a **float32.** Los **valores DepthBias** **y SlopeScaledDepthBias** son miembros de la estructura [**D3D11 \_ RASTERIZER \_ DESC1.**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1) El **valor MaxDepthSlope** es el máximo de pendientes horizontales y verticales del valor de profundidad en el píxel.
2.  Si un búfer de profundidad de punto flotante está enlazado a la fase de fusión de salida, el valor de sesgo se calcula de la siguiente forma:
    ```
    Bias = (float)DepthBias * 2**(exponent(max z in primitive) - r) +
                SlopeScaledDepthBias * MaxDepthSlope;
    ```

    

    donde *r* es el número de bits de mantisa en la representación de punto flotante (excepto el bit oculto); por ejemplo, 23 para **float32**.

A continuación, el valor de sesgo se fija de la siguiente forma:


```
if(DepthBiasClamp > 0)
    Bias = min(DepthBiasClamp, Bias)
else if(DepthBiasClamp < 0)
    Bias = max(DepthBiasClamp, Bias)
```



A continuación, el valor de sesgo se usa para calcular la profundidad de píxeles.


```
if ( (DepthBias != 0) || (SlopeScaledDepthBias != 0) )
    z = z + Bias
```



Las operaciones de sesgo de profundidad se producen en los vértices después del recorte, por lo que el sesgo de profundidad no tiene ningún efecto en el recorte geométrico. El valor de sesgo es constante para una primitiva determinada y se agrega al valor z de cada vértice antes de la configuración del interpolador. Cuando se usan [los niveles](overviews-direct3d-11-devices-downlevel-intro.md) de características 10.0 y superiores, todos los cálculos de sesgo se realizan mediante aritmética de punto flotante de 32 bits. El sesgo no se aplica a ningún primitivo de punto o línea, excepto para las líneas dibujadas en modo wireframe.

Uno de los artefactos con sombras basadas en búfer de sombras es la sombra o una sombra de superficie propiamente dicha debido a pequeñas diferencias entre el cálculo de profundidad en un sombreador y la profundidad de la misma superficie en el búfer de sombras. Una manera de mitigar esto es usar **DepthBias** y **SlopeScaledDepthBias** al representar un búfer de sombra. La idea es insertar superficies lo suficientemente out mientras se representa un búfer de sombras para que el resultado de la comparación (entre el búfer de sombra z y el sombreador z) sea coherente en toda la superficie y evitar el autoconsumo local.

Sin embargo, el uso de **DepthBias** y **SlopeScaledDepthBias** puede presentar nuevos problemas de representación cuando un polígono visto en un ángulo extremadamente nítido hace que la ecuación de sesgo genere un valor z muy grande. De hecho, esto aleja el polígono de la superficie original en el mapa de sombras. Una manera de ayudar a mitigar este problema concreto es usar **DepthBiasClamp,** que proporciona un límite superior (positivo o negativo) en la magnitud del sesgo z calculado.

> [!Note]  
> Para [los niveles de](overviews-direct3d-11-devices-downlevel-intro.md) características 9.1, 9.2, 9.3, **DepthBiasClamp** no se admite.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Fase de fusión de salida](d3d10-graphics-programming-guide-output-merger-stage.md)
</dt> </dl>

 

 




