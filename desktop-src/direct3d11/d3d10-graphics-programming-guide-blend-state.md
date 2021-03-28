---
title: Configuración de la funcionalidad de fusión
description: Las operaciones de combinación se realizan en cada salida del sombreador de píxeles (valor RGBA) antes de que el valor de salida se escriba en un destino de representación. Si el muestreo múltiple está habilitado, la combinación se realiza en cada muestreo múltiple; de lo contrario, se realiza la combinación en cada píxel.
ms.assetid: f5c79baf-7bd3-4f58-abe7-8e96cd6be9d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08acf1ea286b29a1cb96873bbfe170c6f38699f7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997064"
---
# <a name="configuring-blending-functionality"></a>Configuración de la funcionalidad de fusión

Las operaciones de combinación se realizan en cada salida del sombreador de píxeles (valor RGBA) antes de que el valor de salida se escriba en un destino de representación. Si el muestreo múltiple está habilitado, la combinación se realiza en cada muestreo múltiple; de lo contrario, se realiza la combinación en cada píxel.

-   [Crear el estado de Blend](#create-the-blend-state)
-   [Enlazar el estado de Blend](#bind-the-blend-state)
-   [Temas de blending avanzado](#advanced-blending-topics)
    -   [Alfa a cobertura](#alpha-to-coverage)
    -   [Resultados del sombreador de píxeles de fusión](#blending-pixel-shader-outputs)
-   [Temas relacionados](#related-topics)

## <a name="create-the-blend-state"></a>Crear el estado de Blend

El estado de blend es una colección de Estados que se usa para controlar la fusión. Estos Estados (definidos en [**D3D11 \_ Blend \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1)) se usan para crear el objeto de estado de Blend llamando a [**ID3D11Device1:: CreateBlendState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createblendstate1).

Por ejemplo, a continuación se muestra un ejemplo muy sencillo de creación del estado de mezcla que deshabilita la combinación alfa y no utiliza el enmascaramiento de píxeles por componente.


```
ID3D11BlendState1* g_pBlendStateNoBlend = NULL;

D3D11_BLEND_DESC1 BlendState;
ZeroMemory(&BlendState, sizeof(D3D11_BLEND_DESC1));
BlendState.RenderTarget[0].BlendEnable = FALSE;
BlendState.RenderTarget[0].RenderTargetWriteMask = D3D11_COLOR_WRITE_ENABLE_ALL;
pd3dDevice->CreateBlendState1(&BlendState, &g_pBlendStateNoBlend);
```



Este ejemplo es similar al [ejemplo HLSLWithoutFX10](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).

## <a name="bind-the-blend-state"></a>Enlazar el estado de Blend

Después de crear el objeto de estado de Blend, enlace el objeto de estado de mezcla a la fase de combinación de salida llamando a [**ID3D11DeviceContext:: OMSetBlendState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetblendstate).


```
float blendFactor[4] = { 0.0f, 0.0f, 0.0f, 0.0f };
UINT sampleMask   = 0xffffffff;

pd3dDevice->OMSetBlendState(g_pBlendStateNoBlend, blendFactor, sampleMask);
```



Esta API toma tres parámetros: el objeto de estado de mezcla, un factor de mezcla de cuatro componentes y una máscara de ejemplo. Puede pasar **null** para que el objeto de estado de mezcla especifique el estado de Blend predeterminado o pase un objeto de estado de mezcla. Si creó el objeto de estado de Blend con el factor de mezcla de [**D3D11 \_ Blend \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_blend) o el [**\_ factor de \_ \_ mezcla \_ de inv de D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_blend), puede pasar un factor de mezcla a los valores modulares para el sombreador de píxeles, el destino de representación o ambos. Si no ha creado el objeto de estado de Blend con el factor de mezcla de **D3D11 \_ Blend \_ \_** o el **\_ \_ \_ \_ factor** de mezcla de inv de D3D11, puede pasar un factor de mezcla que no sea nulo, pero la fase de fusión no utiliza el factor de mezcla; el Runtime almacena el factor de mezcla y, posteriormente, puede llamar a [**ID3D11DeviceContext:: OMGetBlendState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omgetblendstate) para recuperar el factor de mezcla. Si se pasa **null**, el motor en tiempo de ejecución usa o almacena un factor de mezcla igual a {1, 1, 1, 1}. La máscara de ejemplo es una máscara definida por el usuario que determina cómo se muestra el destino de representación existente antes de actualizarlo. La máscara de muestreo predeterminada es 0xFFFFFFFF, que designa el muestreo del punto.

En la mayoría de los esquemas de almacenamiento en búfer, el píxel más cercano a la cámara es el que se dibuja. Al [configurar el estado de la galería de símbolos de profundidad](d3d10-graphics-programming-guide-depth-stencil.md), el miembro **DepthFunc** de la [**Galería de \_ símbolos de profundidad \_ \_ D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc) puede ser cualquier función de [**\_ comparación \_ D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_comparison_func). Normalmente, desearía que **DepthFunc** se D3D11 de la **\_ comparación \_ menos**, de modo que los píxeles más cercanos a la cámara sobrescribirán los píxeles que se encuentran detrás. Sin embargo, en función de las necesidades de la aplicación, se puede usar cualquiera de las demás funciones de comparación para realizar la prueba de profundidad.

## <a name="advanced-blending-topics"></a>Temas de blending avanzado

-   [Alfa a cobertura](#alpha-to-coverage)
-   [Resultados del sombreador de píxeles de fusión](#blending-pixel-shader-outputs)

### <a name="alpha-to-coverage"></a>Alfa a cobertura

Alpha-to-Coverage es una técnica de muestreo múltiple que es más útil para situaciones como el follaje denso, donde hay varios polígonos superpuestos que usan transparencia alfa para definir bordes dentro de la superficie.

Puede usar el miembro **AlphaToCoverageEnable** de [**D3D11 \_ Blend \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1) o [**D3D11 \_ Blend \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc) para alternar si el Runtime convierte. un componente (alfa) del registro de salida VP de [ \_ destino](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0 del sombreador de píxeles a una máscara de cobertura de n pasos (dado un valor de **RenderTarget** de ejemplo n). El motor en tiempo de ejecución realiza una operación **and** de esta máscara con la cobertura de ejemplo típica para el píxel de la primitiva (además de la máscara de ejemplo) para determinar qué ejemplos se deben actualizar en todas las **RenderTarget** activas.

Si el sombreador de píxeles produce la [ \_ cobertura](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)de la VP, el tiempo de ejecución deshabilita la de alfa a cobertura.

> [!Note]  
> En el muestreo múltiple, el Runtime solo comparte una cobertura para todos los objetos **RenderTarget**. El hecho de que el tiempo de ejecución de Lea y convierta. a del [ \_ destino](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)de la VP de salida 0 a la cobertura cuando **AlphaToCoverageEnable** es true no cambia. un valor que se dirige al mezclador en **RenderTarget** 0 (si se produce un error de **RenderTarget** ). En general, si habilita la operación de alfa a cobertura, no afecta al modo en que todas las salidas de color de los sombreadores de píxeles interactúan con **RenderTarget** s a través de la [fase de fusión de salida](d3d10-graphics-programming-guide-output-merger-stage.md) , salvo que el Runtime realiza una operación **and** de la máscara de cobertura con la máscara de alfa a cobertura. Alpha-to-Coverage funciona de forma independiente a si el runtime puede mezclar **RenderTarget** o si se usa la combinación en **RenderTarget**.

 

El hardware de gráficos no especifica exactamente el modo en que convierte el [ \_ destino](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)de la VP del sombreador de píxeles 0. a (alfa) en una máscara de cobertura, salvo que el valor alfa de 0 (o menos) debe estar asignado a ninguna cobertura y el alfa de 1 (o superior) debe asignarse a la cobertura completa (antes de que el tiempo de ejecución realice una operación **and** con Como el alfa va de 0 a 1, la cobertura resultante debería aumentar de forma continuada. Sin embargo, el hardware puede realizar una interpolación de área para proporcionar una mejor cuantificación de los valores alfa a costa de la resolución espacial y el ruido. Un valor alfa de NaN (no un número) da como resultado una máscara sin cobertura (cero).

La utilización de Alpha-to-Coverage también se usa tradicionalmente para la transparencia de la puerta de pantalla o la definición de siluetas detalladas para sprites opacos de otro modo.

### <a name="blending-pixel-shader-outputs"></a>Resultados del sombreador de píxeles de fusión

Esta característica permite que la fusión de salida Use las salidas del sombreador de píxeles simultáneamente como orígenes de entrada para una operación de combinación con el destino de representación único en la ranura 0.

Este ejemplo toma dos resultados y los combina en un solo paso, mezclando uno en el destino con una multiplicación y el otro con un agregado:


```
SrcBlend = D3D11_BLEND_ONE;
DestBlend = D3D11_BLEND_SRC1_COLOR;
```



En este ejemplo se configura la salida del primer sombreador de píxeles como el color de origen y la segunda salida como factor de mezcla de componentes por color.


```
SrcBlend = D3D11_BLEND_SRC1_COLOR;
DestBlend = D3D11_BLEND_INV_SRC1_COLOR;
```



En este ejemplo se muestra cómo los factores de mezcla deben coincidir con el sombreador swizzles:


```
SrcFactor = D3D11_BLEND_SRC1_ALPHA;
DestFactor = D3D11_BLEND_SRC_COLOR;
OutputWriteMask[0] = .ra; // pseudocode for setting the mask at
                          // RenderTarget slot 0 to .ra
```



Juntos, los factores de mezcla y el código del sombreador implican que el sombreador de píxeles es necesario para generar al menos O0. r y O1. a. Los componentes de salida adicionales pueden ser generados por el sombreador, pero se omitirán, menos componentes generarán resultados sin definir.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Fase de combinación de salida](d3d10-graphics-programming-guide-output-merger-stage.md)
</dt> <dt>

[Fases de canalización (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 