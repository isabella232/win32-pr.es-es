---
description: La compatibilidad con los sprites de punto en Direct3D 9 permite la representación de puntos (sistemas de partículas) de alto rendimiento. Los sprites de punto son generalizaciones de puntos genéricos que permiten representar formas arbitrarias tal y como se definen en las texturas.
ms.assetid: a9046c7e-779c-4f33-b8ff-f189da3dcfc5
title: Sprites de punto (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c988a104eb65b5e2d7e56ff2444e8d422c422df2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537432"
---
# <a name="point-sprites-direct3d-9"></a>Sprites de punto (Direct3D 9)

La compatibilidad con los sprites de punto en Direct3D 9 permite la representación de puntos (sistemas de partículas) de alto rendimiento. Los sprites de punto son generalizaciones de puntos genéricos que permiten representar formas arbitrarias tal y como se definen en las texturas.

-   [Controles de representación de punto primitivo](#point-primitive-rendering-controls)
-   [Cálculos de tamaño de punto](#point-size-computations)
-   [Representación de puntos](#point-rendering)

## <a name="point-primitive-rendering-controls"></a>Controles de representación de punto primitivo

Direct3D 9 admite parámetros adicionales para controlar la representación de los sprites de punto (primitivos de punto). Estos parámetros permiten que los puntos sean de tamaño variable y tengan aplicado un mapa de textura completo. El tamaño de cada punto viene determinado por un tamaño especificado por la aplicación combinado con una función basada en distancia calculada por Direct3D. La aplicación puede especificar el tamaño del punto como por vértice o mediante el establecimiento de D3DRS \_ , que se aplica a los puntos sin un tamaño por vértice. El tamaño de los puntos se expresa en unidades de espacio de la cámara, con la excepción de cuando la aplicación pasa los vértices del formato de vértice flexible (FVF) transformados. En este caso, no se aplica la función basada en distancia y el tamaño del punto se expresa en unidades de píxeles en el destino de representación.

Las coordenadas de textura calculadas y utilizadas cuando los puntos de representación dependen de la configuración de D3DRS \_ POINTSPRITEENABLE. Cuando este valor se establece en **true**, las coordenadas de textura se establecen para que cada punto muestre la textura completa. En general, esto solo es útil cuando los puntos son significativamente mayores de un píxel. Cuando D3DRS \_ POINTSPRITEENABLE se establece en **false**, se usa la coordenada de textura del vértice de cada punto para todo el punto.

## <a name="point-size-computations"></a>Cálculos de tamaño de punto

D3DRS POINTSCALEENABLE determina el tamaño de los puntos \_ . Si este valor se establece en **false**, el tamaño de punto especificado por la aplicación se usa como el tamaño del espacio de pantalla (posterior a la transformación). Los vértices que se pasan a Direct3D en el espacio de pantalla no tienen tamaños de punto calculados; el tamaño de punto especificado se interpreta como el tamaño del espacio de pantalla.

Si D3DRS \_ POINTSCALEENABLE es **true**, Direct3D calcula el tamaño del punto de espacio de pantalla según la fórmula siguiente. El tamaño de punto especificado por la aplicación se expresa en unidades de espacio de la cámara.

S s = VH \* s <sub>i</sub> \* sqrt (1/(A + B \* D ₑ + C \* (D ₑ ²)))

En esta fórmula, el tamaño del punto de entrada, S <sub>i</sub>, es por vértice o el valor del estado de representación de los puntos de D3DRS \_ . Los factores de escala de puntos, D3DRS \_ POINTSCALE \_ A, D3DRS \_ POINTSCALE \_ B y D3DRS \_ POINTSCALE \_ C, se representan mediante los puntos a, B y c. El alto de la ventanilla, V h, es el miembro de alto de la estructura [**D3DVIEWPORT9**](d3dviewport9.md) que representa la ventanilla. D ₑ, la distancia desde el ojo hasta la posición (el ojo en el origen), se calcula tomando la posición del espacio ocular del punto (X ₑ, Y ₑ, Z ₑ) y realizando la operación siguiente.

D ₑ = sqrt (X ₑ ² + Y ₑ ² + Z ₑ ²)

El tamaño de punto máximo, PM ₐ ₓ, se determina tomando el menor del miembro MaxPointSize de la estructura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) o el estado de representación de D3DRS en el límite \_ \_ máximo. El tamaño mínimo de los puntos, P<sub>min</sub>, se determina consultando el valor de D3DRS de \_ puntuación \_ mín. Por lo tanto, el tamaño final del punto de espacio de la pantalla, S, se determina de la siguiente manera.

-   Si SS > PM ₐ ₓ, entonces S = P m ₐ ₓ
-   Si S < P<sub>min</sub>, entonces s = P <sub>min</sub>
-   De lo contrario, S = S

## <a name="point-rendering"></a>Representación de puntos

Un punto de espacio de pantalla, P = (X, Y, Z, W), de tamaño de espacio de pantalla S se rasteriza como cuadrangular de los cuatro vértices siguientes.

((X + S/2, Y + S/2, Z, W), (X + S/2, Y-S/2, Z, W), (X-S/2, Y-S/2, Z, W), (X-S/2, Y + S/2, Z, W))

Los atributos de color de vértice se duplican en cada vértice; por lo tanto, cada punto siempre se representa con colores constantes.

La asignación de índices de textura se controla mediante la configuración de \_ Estado de representación de D3DRS POINTSPRITEENABLE. Si D3DRS \_ POINTSPRITEENABLE se establece en **false**, las coordenadas de textura de los vértices se duplican en cada vértice. Si D3DRS \_ POINTSPRITEENABLE se establece en **true**, las coordenadas de textura de los cuatro vértices se establecen en los valores siguientes.

(0. F, 0. F), (0. F, 1. F), (1. F, 0. F), (1. F, 1. F)

Esto se muestra en el diagrama siguiente.

![diagrama de un cuadrado con vértices etiquetados para los valores de coordenadas (u, v) y (x, y)](images/spritepoint.png)

Cuando está habilitado el recorte, los puntos se recortan de la siguiente manera. Si el vértice supera el intervalo de valores de profundidad-MinZ y MaxZ de la estructura [**D3DVIEWPORT9**](d3dviewport9.md) -en la que se va a representar una escena, el punto existe fuera del frustum de la vista y no se representa. Si el punto que tiene en cuenta el tamaño del punto está completamente fuera de la ventanilla en X e y, no se representa el punto; se representan los puntos restantes. Es posible que la posición del punto esté fuera de la ventanilla en X o Y y siga siendo parcialmente visible.

Los puntos se pueden recortar correctamente en los planos de clip definidos por el usuario. Si \_ no se establece D3DPMISCCAPS CLIPPLANESCALEDPOINTS en el miembro PrimitiveMiscCaps de la estructura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) , los puntos se recortan a los planos de clip definidos por el usuario basados solo en la posición del vértice, omitiendo el tamaño del punto. En este caso, los puntos de escala se representan completamente cuando la posición del vértice está dentro de los planos de recorte y se descartan cuando la posición del vértice está fuera de un plano de recorte. Las aplicaciones pueden impedir posibles artefactos si agregan una geometría de borde a los planos de recorte que sea tan grande como el tamaño máximo de los puntos.

Si \_ se establece el bit CLIPPLANESCALEDPOINTS de D3DPMISCCAPS, los puntos con escala se recortan correctamente en los planos de clips definidos por el usuario.

El procesamiento de vértices de hardware puede admitir o no el tamaño de los puntos. Por ejemplo, si se crea un dispositivo con D3DCREATE \_ hardware \_ VERTEXPROCESSING en un dispositivo de capa de abstracción de hardware (HAL) (D3DDEVTYPE \_ HAL) que tenga el miembro MaxPointSize de la estructura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) establecido en 1,0 o 0,0, todos los puntos serán de un solo píxel. Para representar los sprites de punto de píxel en menos de 1,0, debe usar vértices FVF TL (transformados y iluminados) o el procesamiento de vértices de software (D3DCREATE \_ software \_ VERTEXPROCESSING), en cuyo caso el tiempo de ejecución de Direct3D emula la representación de Sprite de punto.

Un dispositivo de hardware que realiza el procesamiento de vértices y admite sprites de punto: MaxPointSize establecido en un valor mayor que 1,0 f es necesario para realizar el cálculo de tamaño para los sprites no transformados y es necesario para establecer correctamente los puntos de POINTSIZED3DRS por vértice o D3DRS \_ \_ para los vértices TL.

Para obtener información sobre las reglas de representación de puntos, líneas y triángulos, vea [reglas de rasterización (Direct3D 9)](rasterization-rules.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Canalización de vértices](vertex-pipeline.md)
</dt> </dl>

 

 



