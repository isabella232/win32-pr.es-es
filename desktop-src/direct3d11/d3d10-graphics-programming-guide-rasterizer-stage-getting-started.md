---
title: Tareas iniciales con la fase rasterizadora
description: En esta sección se describe el establecimiento de la ventanilla, el rectángulo de las manos, el estado del rasterizador y el muestreo múltiple.
ms.assetid: d78c3845-76fd-4bd7-a603-bb1d8c66ac49
keywords:
- multimuestreo, estado de rasterizador (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e819dd92dd9c07a71f3830d3b67e371bc3d0e0c98f62fa36fdcf8ee3550ecd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117914006"
---
# <a name="getting-started-with-the-rasterizer-stage"></a>Tareas iniciales con la fase rasterizadora

En esta sección se describe el establecimiento de la ventanilla, el rectángulo de las manos, el estado del rasterizador y el muestreo múltiple.

## <a name="set-the-viewport"></a>Establecer la ventanilla

Una ventanilla asigna posiciones de vértice (en el espacio de recorte) en posiciones de destino de representación. Este paso escala las posiciones 3D en un espacio 2D. Un destino de representación está orientado con los ejes Y apuntando hacia abajo; esto requiere que las coordenadas Y se voltearán durante la escala de la ventanilla. Además, las extensiones x e y (intervalo de los valores x e y) se escalan para ajustarse al tamaño de la ventanilla según las fórmulas siguientes:


```
X = (X + 1) * Viewport.Width * 0.5 + Viewport.TopLeftX
Y = (1 - Y) * Viewport.Height * 0.5 + Viewport.TopLeftY
Z = Viewport.MinDepth + Z * (Viewport.MaxDepth - Viewport.MinDepth) 
```



El tutorial 1 crea una ventanilla 640 × 480 mediante [**D3D11 \_ VIEWPORT**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport) y llamando a [**ID3D11DeviceContext::RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports).


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



La descripción de la ventanilla especifica el tamaño de la ventanilla, el intervalo al que se va a asignar la profundidad (mediante *MinDepth* y *MaxDepth)* y la posición de la parte superior izquierda de la ventanilla. *MinDepth* debe ser menor o igual que *MaxDepth*; El intervalo de *MinDepth* y *MaxDepth* está entre 0,0 y 1,0, ambos inclusive. Es habitual que la ventanilla se asigne a un destino de representación, pero no es necesario; Además, la ventanilla no tiene que tener el mismo tamaño o posición que el destino de representación.

Puede crear una matriz de ventanillas, pero solo se puede aplicar una a una salida primitiva del sombreador de geometría. Solo se puede establecer una ventanilla activa a la vez. La canalización usa una ventanilla predeterminada (y un rectángulo de rectángulo de rectángulos, que se describe en la sección siguiente) durante la rasterización. El valor predeterminado es siempre la primera ventanilla (o rectángulo de rectángulo) de la matriz. Para realizar una selección por primitiva de la ventanilla en el sombreador de geometría, especifique la semántica ViewportArrayIndex en el componente de salida GS adecuado en la declaración de firma de salida de GS.

El número máximo de ventanillas (y rectángulos de rectángulos de rectángulos) que se pueden enlazar a la fase de rasterizador en cualquier momento es 16 (especificado por **D3D11 \_ \_ VIEWPORT Y \_ VIEWPORTRECT \_ OBJECT COUNT PER \_ \_ \_ PIPELINE**).

## <a name="set-the-scissor-rectangle"></a>Establecer el rectángulo de rectángulo de rectángulos de rectángulos

Un rectángulo de rectángulo de rectángulos le ofrece otra oportunidad para reducir el número de píxeles que se enviarán a la fase de fusión de salida. Se descartan los píxeles situados fuera del rectángulo de rectángulos. El tamaño del rectángulo de rectángulo de rectángulo se especifica en enteros. Durante la rasterización, solo se puede aplicar un rectángulo de rectángulos (basado en *ViewportArrayIndex* en la [semántica](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)de valores del sistema) a un triángulo.

Para habilitar el rectángulo de rectángulo de rectángulo, use el miembro [**\_ \_ DesC1 de Rasterizer de D3D11 ( en D3D11 RASTERIZER ).**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)  El rectángulo de rectángulo de rectángulo predeterminado es un rectángulo vacío; Es decir, todos los valores de rect son 0. En otras palabras, si no configura el rectángulo de rectángulo de rectángulos y el relleno está habilitado, no enviará ningún píxel a la fase de fusión de salida. La configuración más común es inicializar el rectángulo de relleno al tamaño de la ventanilla.

Para establecer una matriz de rectángulos en el dispositivo, llame a [**ID3D11DeviceContext::RSSetScissorRects**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetscissorrects) con [**D3D11 \_ RECT**](d3d11-rect.md).


```
D3D11_RECT rects[1];
  rects[0].left = 0;
  rects[0].right = 640;
  rects[0].top = 0;
  rects[0].bottom = 480;

  D3DDevice->RSSetScissorRects( 1, rects );
```



Este método toma dos parámetros: (1) el número de rectángulos de la matriz y (2) una matriz de rectángulos.

La canalización usa un índice de rectángulo predeterminado durante la rasterización (el valor predeterminado es un rectángulo de tamaño cero con recorte deshabilitado). Para invalidar esto, especifique la semántica SV \_ ViewportArrayIndex para un componente de salida GS en la declaración de firma de salida de GS. Esto hará que la fase GS marque este componente de salida de GS como un componente generado por el sistema con esta semántica. La fase del rasterizador reconoce esta semántica y usará el parámetro al que está asociado como índice del rectángulo de rectángulos. No olvide decir a la fase del rasterizador que use el rectángulo de relleno que defina habilitando el valor *Desenable en* la descripción del rasterizador antes de crear el objeto rasterizador.

## <a name="set-rasterizer-state"></a>Establecer el estado del rasterizador

A partir de Direct3D 10, el estado del rasterizador se encapsula en un objeto de estado de rasterizador. Puede crear hasta 4096 objetos de estado de rasterizador que, a continuación, se pueden establecer en el dispositivo pasando un identificador al objeto de estado.

Use [**ID3D11Device1::CreateRasterizerState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createrasterizerstate1) para crear un objeto de estado de rasterizador a partir de una descripción de rasterizador (vea [**D3D11 \_ RASTERIZER \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)).


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



Este conjunto de estado de ejemplo realiza quizás la configuración de rasterizador más básica:

-   Modo de relleno sólido
-   Quitar o quitar caras; asumir el orden de sinuoso en el sentido contrario a las agujas del reloj para las primitivas
-   Desactivar el sesgo de profundidad, pero habilitar el almacenamiento en búfer de profundidad y habilitar el rectángulo de relleno
-   Desactivar el suavizado multimuestreo y el suavizado de alias de línea

Además, las operaciones básicas de rasterizador incluyen siempre lo siguiente: recorte (al frustum de vista), división de perspectiva y escala de ventanilla. Después de crear correctamente el objeto de estado del rasterizador, estadón en el dispositivo de la siguiente manera:


```
    pd3dDevice->RSSetState(g_pRasterState);
```



### <a name="multisampling"></a>Muestreo múltiple

El muestreo múltiple muestra algunos o todos los componentes de una imagen con una resolución más alta (seguido de una reducción a la resolución original) para reducir la forma más visible de alias causada por el dibujo de bordes de polígono. Aunque la multimuestreo requiere ejemplos de subpíxeles, las GPU modernas implementan multimuestreo para que un sombreador de píxeles se ejecute una vez por píxel. Esto proporciona un equilibrio aceptable entre el rendimiento (especialmente en una aplicación enlazada a GPU) y el suavizado de alias de la imagen final.

Para usar multimuestreo, establezca el campo enable en la descripción de [**rasterización**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1), cree un destino de representación multimuestreo y lea el destino de representación con un sombreador para resolver los ejemplos en un color de un solo píxel o llame a [**ID3D11DeviceContext::ResolveSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-resolvesubresource) para resolver los ejemplos mediante la tarjeta de vídeo. El escenario más común es dibujar en uno o varios destinos de representación multimuestreo.

La multimuestreo es independiente de si se usa o no una máscara de [muestra,](d3d10-graphics-programming-guide-blend-state.md) de si está habilitada la cobertura alfa o de las operaciones de galería de símbolos (que siempre se realizan por muestra).

Las pruebas de profundidad se ven afectadas por la multimuestreo:

-   Cuando se habilita la multimuestreo, la profundidad se interpola por muestra y la prueba de profundidad o galería de símbolos se realiza por muestra. El color de salida del sombreador de píxeles está duplicado para todas las muestras que pasan. Si el sombreador de píxeles genera profundidad, el valor de profundidad se duplica para todas las muestras (aunque este escenario pierde la ventaja de la multimuestreo).
-   Cuando se deshabilita la multimuestreo, las pruebas de profundidad o galería de símbolos se siguen haciendo por muestra, pero la profundidad no se interpola por muestra.

No hay ninguna restricción para mezclar la representación multimuestreo y no multimuestreo dentro de un único destino de representación. Si habilita la multimuestreo y dibuja en un destino de representación no multimuestreo, se produce el mismo resultado que si no se habilitara la multimuestreo. el muestreo se realiza con una sola muestra por píxel.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Etapa del rasterizador](d3d10-graphics-programming-guide-rasterizer-stage.md)
</dt> </dl>

 

 