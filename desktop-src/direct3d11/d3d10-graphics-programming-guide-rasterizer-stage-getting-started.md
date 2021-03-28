---
title: Introducción con la fase de rasterizador
description: En esta sección se describe la configuración de la ventanilla, el rectángulo de tijeras, el estado de rasterizador y el muestreo múltiple.
ms.assetid: d78c3845-76fd-4bd7-a603-bb1d8c66ac49
keywords:
- muestreo múltiple, estado de rasterizador (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac95a15221f6fd4bd422e96c0686816afb35d4e8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359000"
---
# <a name="getting-started-with-the-rasterizer-stage"></a>Introducción con la fase de rasterizador

En esta sección se describe la configuración de la ventanilla, el rectángulo de tijeras, el estado de rasterizador y el muestreo múltiple.

## <a name="set-the-viewport"></a>Establecer la ventanilla

Una ventanilla asigna las posiciones de los vértices (en el espacio de recorte) en las posiciones de destino de representación. En este paso se escalan las posiciones 3D en el espacio 2D. Un destino de representación se orienta con los ejes Y que apuntan hacia abajo; Esto requiere que las coordenadas Y se invierten durante la escala de la ventanilla. Además, las extensiones x e y (rango de los valores x e y) se escalan para ajustarse al tamaño de la ventanilla según las fórmulas siguientes:


```
X = (X + 1) * Viewport.Width * 0.5 + Viewport.TopLeftX
Y = (1 - Y) * Viewport.Height * 0.5 + Viewport.TopLeftY
Z = Viewport.MinDepth + Z * (Viewport.MaxDepth - Viewport.MinDepth) 
```



El tutorial 1 crea una ventanilla 640 × 480 con [**D3D11 \_ viewport**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport) y llamando a [**ID3D11DeviceContext:: RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports).


```
    D3D11_VIEWPORT vp[1];
    vp[0].Width = 640.0f;
    vp[0].Height = 480.0f;
    vp[0].MinDepth = 0;
    vp[0].MaxDepth = 1;
    vp[0].TopLeftX = 0;
    vp[0].TopLeftY = 0;
    g_pd3dDevice->RSSetViewports( 1, vp );
```



La descripción de la ventanilla especifica el tamaño de la ventanilla, el intervalo al que se va a asignar profundidad (mediante *MinDepth* y *maxdepth*), y la posición de la parte superior izquierda de la ventanilla. *MinDepth* debe ser menor o igual que *maxdepth*; el intervalo de *MinDepth* y *MaxDepth* está entre 0,0 y 1,0, ambos incluidos. Es habitual que la ventanilla se asigne a un destino de representación, pero no es necesario; Además, la ventanilla no tiene que tener el mismo tamaño o la misma posición que el destino de representación.

Puede crear una matriz de ventanillas, pero solo se puede aplicar una a una salida primitiva del sombreador de geometría. Solo se puede establecer una ventanilla activa a la vez. La canalización usa una ventanilla predeterminada (y un rectángulo de tijeras, que se describe en la sección siguiente) durante la rasterización. El valor predeterminado es siempre la primera ventanilla (o rectángulo en tijera) de la matriz. Para realizar una selección por primitivo de la ventanilla en el sombreador de geometría, especifique la semántica ViewportArrayIndex en el componente de salida GS adecuado en la declaración de la firma de salida GS.

El número máximo de ventanillas (y rectángulos en tijeras) que se pueden enlazar a la fase de rasterizador en cualquier momento es 16 (especificado por la **\_ ventanilla \_ de D3D11 y el \_ recuento de objetos de SCISSORRECT \_ \_ \_ por \_ canalización**).

## <a name="set-the-scissor-rectangle"></a>Establecer el rectángulo en tijera

Un rectángulo en tijeras le ofrece otra oportunidad de reducir el número de píxeles que se enviarán a la fase de fusión de salida. Los píxeles que se encuentran fuera del rectángulo de tijera se descartan. El tamaño del rectángulo en tijera se especifica en enteros. Solo se puede aplicar un rectángulo en tijera (basado en *ViewportArrayIndex* en la [semántica del valor del sistema](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)) a un triángulo durante la rasterización.

Para habilitar el rectángulo en tijeras, use el miembro *ScissorEnable* (en [**D3D11 \_ rasterizador \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)). El rectángulo entre tijeras predeterminado es un rectángulo vacío; es decir, todos los valores Rect son 0. En otras palabras, si no configura el rectángulo en tijera y los tijeras están habilitados, no enviará ningún píxel a la fase de fusión de salida. La configuración más común consiste en inicializar el rectángulo de tijeras con el tamaño de la ventanilla.

Para establecer una matriz de rectángulos con tijeras en el dispositivo, llame a [**ID3D11DeviceContext:: RSSetScissorRects**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetscissorrects) con [**D3D11 \_ Rect**](d3d11-rect.md).


```
D3D11_RECT rects[1];
  rects[0].left = 0;
  rects[0].right = 640;
  rects[0].top = 0;
  rects[0].bottom = 480;

  D3DDevice->RSSetScissorRects( 1, rects );
```



Este método toma dos parámetros: (1) el número de rectángulos de la matriz y (2) una matriz de rectángulos.

La canalización utiliza un índice de rectángulo de tijeras predeterminado durante la rasterización (el valor predeterminado es un rectángulo de tamaño cero con el recorte deshabilitado). Para invalidar esto, especifique la \_ semántica de VP ViewportArrayIndex para un componente de salida GS en la declaración de la firma de salida GS. Esto hará que la fase GS marque este componente de salida GS como un componente generado por el sistema con esta semántica. La fase de rasterizador reconoce esta semántica y usará el parámetro al que se adjunta como índice de rectángulo en tijera para tener acceso a la matriz de rectángulos con tijeras. No se olvide de indicar a la fase de rasterizador que use el rectángulo de tijeras que define al habilitar el valor de *ScissorEnable* en la descripción de rasterizador antes de crear el objeto de rasterizador.

## <a name="set-rasterizer-state"></a>Establecer estado de rasterizador

A partir de Direct3D 10, el estado de rasterizador se encapsula en un objeto de estado de rasterizador. Puede crear hasta 4096 objetos de estado de rasterizador que se pueden establecer en el dispositivo pasando un identificador al objeto de estado.

Use [**ID3D11Device1:: CreateRasterizerState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createrasterizerstate1) para crear un objeto de estado de rasterizador a partir de una descripción de rasterizador (consulte [**D3D11 \_ rasterizador \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)).


```
    ID3D11RasterizerState1 * g_pRasterState;

    D3D11_RASTERIZER_DESC1 rasterizerState;
    rasterizerState.FillMode = D3D11_FILL_SOLID;
    rasterizerState.CullMode = D3D11_CULL_FRONT;
    rasterizerState.FrontCounterClockwise = true;
    rasterizerState.DepthBias = false;
    rasterizerState.DepthBiasClamp = 0;
    rasterizerState.SlopeScaledDepthBias = 0;
    rasterizerState.DepthClipEnable = true;
    rasterizerState.ScissorEnable = true;
    rasterizerState.MultisampleEnable = false;
    rasterizerState.AntialiasedLineEnable = false;
    rasterizerState.ForcedSampleCount = 0;
    pd3dDevice->CreateRasterizerState1( &rasterizerState, &g_pRasterState );
```



Este conjunto de estado de ejemplo lleva a cabo quizás la configuración de rasterizador más básica:

-   Modo de relleno sólido
-   Desactivación o eliminación de caras atrás; asuma el orden de bobinado en sentido contrario a las agujas del reloj para primitivos
-   Desactivar la diferencia de profundidad, habilitar el almacenamiento en búfer de profundidad y habilitar el rectángulo en tijera
-   Desactivar el suavizado de contorno de línea y muestreo múltiple

Además, las operaciones básicas de rasterizador siempre incluyen lo siguiente: recorte (al frustum de vista), División de perspectiva y escala de la ventanilla. Después de crear correctamente el objeto de estado de rasterizador, establézcalo en el dispositivo de la siguiente manera:


```
    pd3dDevice->RSSetState(g_pRasterState);
```



### <a name="multisampling"></a>Muestreo múltiple

Muestreo múltiple muestrea algunos o todos los componentes de una imagen con una resolución superior (seguida de una disminución de nivel de la resolución original) para reducir el formato de alias más visible causado por los bordes de polígonos de dibujo. Aunque el muestreo múltiple requiere muestras de subpíxeles, las GPU modernas implementan el multimuestreo para que un sombreador de píxeles se ejecute una vez por píxel. Esto proporciona un equilibrio aceptable entre el rendimiento (especialmente en una aplicación enlazada con GPU) y el suavizado de contorno de la imagen final.

Para usar el muestreo múltiple, establezca el campo habilitar en la descripción de la [**rasterización**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1), cree un destino de representación de muestreo múltiple y lea el destino de representación con un sombreador para resolver los ejemplos en un color de un solo píxel o llame a [**ID3D11DeviceContext:: ResolveSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-resolvesubresource) para resolver los ejemplos mediante la tarjeta de vídeo. El escenario más común es dibujar en uno o varios destinos de representación multimuestreados.

El muestreo múltiple es independiente de si se usa o no una máscara de ejemplo, se habilita la opción [de alfa a cobertura](d3d10-graphics-programming-guide-blend-state.md) o las operaciones de estarcido (que siempre se realizan por muestra).

Las pruebas de profundidad se ven afectadas por el muestreo múltiple:

-   Cuando se habilita el muestreo múltiple, la profundidad se interpola por muestra y la prueba de profundidad/estarcido se realiza por ejemplo. el color de salida del sombreador de píxeles se duplica para todas las muestras de paso. Si el sombreador de píxeles genera profundidad, el valor de profundidad se duplica para todos los ejemplos (aunque este escenario pierde la ventaja de la multimuestreo).
-   Cuando el muestreo múltiple está deshabilitado, las pruebas de profundidad y estarcido se siguen realizando por ejemplo, pero la profundidad no se interpola por muestra.

No hay restricciones para mezclar la representación multimuestreada y no multimuestreada en un único destino de representación. Si habilita el muestreo múltiple y dibuja en un destino de representación no multimuestreado, se produce el mismo resultado que si no se hubiera habilitado el muestreo múltiple; el muestreo se realiza con una sola muestra por píxel.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Etapa del rasterizador](d3d10-graphics-programming-guide-rasterizer-stage.md)
</dt> </dl>

 

 