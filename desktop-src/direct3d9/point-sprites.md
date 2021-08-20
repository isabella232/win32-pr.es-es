---
description: La compatibilidad con sprites de punto en Direct3D 9 permite la representación de alto rendimiento de puntos (sistemas de partículas). Los sprites de punto son generalizaciones de puntos genéricos que permiten representar formas arbitrarias tal como las definen las texturas.
ms.assetid: a9046c7e-779c-4f33-b8ff-f189da3dcfc5
title: Sprites de punto (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90abd21207d9b3866ff93bd6c73069b655056f1c28811689762b0ce669183793
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118520478"
---
# <a name="point-sprites-direct3d-9"></a>Sprites de punto (Direct3D 9)

La compatibilidad con sprites de punto en Direct3D 9 permite la representación de alto rendimiento de puntos (sistemas de partículas). Los sprites de punto son generalizaciones de puntos genéricos que permiten representar formas arbitrarias tal como las definen las texturas.

-   [Controles de representación primitiva de punto](#point-primitive-rendering-controls)
-   [Cálculos de tamaño de punto](#point-size-computations)
-   [Representación de puntos](#point-rendering)

## <a name="point-primitive-rendering-controls"></a>Controles de representación primitiva de punto

Direct3D 9 admite parámetros adicionales para controlar la representación de sprites de punto (primitivas de punto). Estos parámetros permiten que los puntos sean de tamaño variable y que se aplique un mapa de textura completo. El tamaño de cada punto viene determinado por un tamaño especificado por la aplicación combinado con una función basada en distancia calculada por Direct3D. La aplicación puede especificar el tamaño de punto como por vértice o estableciendo D3DRS POINTSIZE, que se aplica a los puntos sin un tamaño \_ por vértice. El tamaño del punto se expresa en unidades de espacio de la cámara, a excepción de cuando la aplicación pasa vértices de formato de vértice flexible (FVF) transformados posteriormente. En este caso, la función basada en distancia no se aplica y el tamaño del punto se expresa en unidades de píxeles en el destino de representación.

Las coordenadas de textura calculadas y usadas al representar puntos dependen de la configuración de D3DRS \_ POINTSPRITEENABLE. Cuando este valor se establece en **TRUE,** las coordenadas de textura se establecen para que cada punto muestre la textura completa. En general, esto solo es útil cuando los puntos son significativamente mayores que un píxel. Cuando D3DRS POINTSPRITEENABLE se establece en FALSE, se usa la coordenada de textura de vértice de cada punto \_ para todo el punto. 

## <a name="point-size-computations"></a>Cálculos de tamaño de punto

El tamaño del punto viene determinado por D3DRS \_ POINTSCALEENABLE. Si este valor se establece en **FALSE,** el tamaño de punto especificado por la aplicación se usa como tamaño de espacio de pantalla (posterior a la transformación). Los vértices que se pasan a Direct3D en el espacio de pantalla no tienen tamaños de punto calculados; el tamaño de punto especificado se interpreta como tamaño de espacio en pantalla.

Si D3DRS \_ POINTSCALEENABLE es **TRUE,** Direct3D calcula el tamaño del punto de espacio de pantalla según la fórmula siguiente. El tamaño de punto especificado por la aplicación se expresa en unidades de espacio de la cámara.

S = Vh \* S <sub>i</sub> \* sqrt(1/(A + B D ₑ + C ( D \* \* ₑ):))

En esta fórmula, el tamaño del punto de entrada, S <sub>i</sub>, es por vértice o el valor del estado de representación \_ POINTSIZE de D3DRS. Los factores de escala de punto, D3DRS \_ POINTSCALE \_ A, D3DRS POINTSCALE B y \_ \_ D3DRS \_ POINTSCALE C, se representan mediante los puntos \_ A, B y C. El alto de la ventanilla, V h, es el miembro Height de la estructura [**D3DVIEWPORT9**](d3dviewport9.md) que representa la ventanilla. D ₑ, la distancia entre el ojo y la posición (el ojo en el origen) se calcula tomando la posición del espacio ocular del punto (Xₑ, Yₑ, Zₑ) y realizando la siguiente operación.

D ₑ = sqrt (Xₑ): + Y ₑ asínto + Z ₑ):

El tamaño máximo de punto, Pmₐₓ, se determina tomando el menor del miembro MaxPointSize de la estructura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) o del estado de representación D3DRS \_ POINTSIZE \_ MAX. El tamaño de punto mínimo, P<sub>min</sub>, se determina consultando el valor de D3DRS \_ POINTSIZE \_ MIN. Por lo tanto, el tamaño final del punto de espacio en pantalla, S, se determina de la siguiente manera.

-   Si Ss > Pmₐₓ, S = P mₐₓ
-   si S < P<sub>min</sub>, S = P <sub>min</sub>
-   De lo contrario, S = S s

## <a name="point-rendering"></a>Representación de puntos

Un punto de espacio de pantalla, P = ( X, Y, Z, W), del tamaño del espacio de pantalla S se rasteriza como un cuadrículo de los cuatro vértices siguientes.

(( X + S/2, Y + S/2, Z, W), ( X + S/2, Y - S/2, Z, W), ( X - S/2, Y- S/2, Z, W), ( X - S/2, Y + S/2, Z, W))

Los atributos de color del vértice se duplican en cada vértice; por lo tanto, cada punto siempre se representa con colores constantes.

La asignación de índices de textura se controla mediante la configuración de estado de representación D3DRS \_ POINTSPRITEENABLE. Si D3DRS POINTSPRITEENABLE se establece en FALSE, las coordenadas de textura de vértice se \_ duplican en cada vértice.  Si D3DRS POINTSPRITEENABLE se establece en TRUE, las coordenadas de textura de los cuatro vértices se establecen \_ en los valores siguientes. 

(0.F, 0.F), (0.F, 1.F), (1.F, 0.F), (1.F, 1.F)

Esto se muestra en el diagrama siguiente.

![diagrama de un cuadrado con vértices etiquetados para los valores de coordenadas (u,v) y (x,y)](images/spritepoint.png)

Cuando el recorte está habilitado, los puntos se recortan de la siguiente manera. Si el vértice supera el intervalo de valores de profundidad (MinZ y MaxZ de la estructura [**D3DVIEWPORT9)**](d3dviewport9.md) en el que se va a representar una escena, el punto existe fuera del frustum de la vista y no se representa. Si el punto, teniendo en cuenta el tamaño de punto, está completamente fuera de la ventanilla en X e Y, el punto no se representa; se representan los puntos restantes. Es posible que la posición de punto esté fuera de la ventanilla en X o Y y todavía esté parcialmente visible.

Los puntos pueden o no recortarse correctamente a planos de recorte definidos por el usuario. Si D3DPMISCCAPS CLIPPLANESCALEDPOINTS no está establecido en el miembro PrimitiveMiscCaps de la estructura \_ [**D3DCAPS9,**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) los puntos se recortan a planos de recorte definidos por el usuario solo en función de la posición del vértice, omitiendo el tamaño del punto. En este caso, los puntos escalados se representan completamente cuando la posición del vértice está dentro de los planos de recorte y se descartan cuando la posición del vértice está fuera de un plano de recorte. Las aplicaciones pueden evitar posibles artefactos agregando una geometría de borde para recortar planos que sea tan grande como el tamaño máximo de punto.

Si se establece el bit CLIPPLANESCALEDPOINTS de D3DPMISCCAPS, los puntos escalados se recortan correctamente a planos de recorte definidos por \_ el usuario.

El procesamiento de vértices de hardware puede admitir o no el tamaño de punto. Por ejemplo, si se crea un dispositivo con D3DCREATE HARDWARE VERTEXPROCESSING en un dispositivo de capa de abstracción de hardware (HAW) (D3DDEVTYPE UNO) que tiene el miembro MaxPointSize de la estructura \_ \_ \_ [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) establecido en 1.0 o 0.0, todos los puntos son un solo píxel. Para representar sprites de punto de píxeles inferiores a 1,0, debe usar vértices tl FVF (transformados y encendidos) o procesamiento de vértices de software (D3DCREATE SOFTWARE VERTEXPROCESSING), en cuyo caso el tiempo de \_ ejecución de Direct3D emula la representación de sprite de \_ punto.

Un dispositivo de hardware que realiza el procesamiento de vértices y admite sprites de punto (MaxPointSize establecido en mayor que 1,0f) es necesario para realizar el cálculo de tamaño para sprites no transformadores y es necesario establecer correctamente el valor por vértice o D3DRS \_ POINTSIZED3DRS POINTSIZE para vértices \_ TL.

Para obtener información sobre las reglas de representación de puntos, líneas y triángulos, vea Reglas de [rasterización (Direct3D 9).](rasterization-rules.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Canalización de vértices](vertex-pipeline.md)
</dt> </dl>

 

 



