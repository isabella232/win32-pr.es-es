---
title: Configuración de la funcionalidad de Depth-Stencil
description: En esta sección se explican los pasos para configurar el búfer de estarcido de profundidad y el estado de la galería de símbolos de profundidad para la fase de combinación de salida.
ms.assetid: e8f52d5f-266f-4e2c-b38d-d7fd9e27fe1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65bf48b0ba9a782be25568ac3fc0569314dae76e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792706"
---
# <a name="configuring-depth-stencil-functionality"></a>Configuración de la funcionalidad de Depth-Stencil

En esta sección se explican los pasos para configurar el búfer de estarcido de profundidad y el estado de la galería de símbolos de profundidad para la fase de combinación de salida.

-   [Creación de un recurso de Depth-Stencil](#create-a-depth-stencil-resource)
-   [Crear estado de Depth-Stencil](#create-depth-stencil-state)
-   [Enlazar datos de Depth-Stencil a la fase de OM](#bind-depth-stencil-data-to-the-om-stage)

Una vez que sepa cómo usar el búfer de estarcido de profundidad y el estado de la galería de símbolos de profundidad correspondiente, consulte [técnicas avanzadas de estarcido](#advanced-stencil-techniques).

## <a name="create-a-depth-stencil-resource"></a>Creación de un recurso de Depth-Stencil

Cree el búfer de estarcido de profundidad con un recurso de textura.


```
ID3D11Texture2D* pDepthStencil = NULL;
D3D11_TEXTURE2D_DESC descDepth;
descDepth.Width = backBufferSurfaceDesc.Width;
descDepth.Height = backBufferSurfaceDesc.Height;
descDepth.MipLevels = 1;
descDepth.ArraySize = 1;
descDepth.Format = pDeviceSettings->d3d11.AutoDepthStencilFormat;
descDepth.SampleDesc.Count = 1;
descDepth.SampleDesc.Quality = 0;
descDepth.Usage = D3D11_USAGE_DEFAULT;
descDepth.BindFlags = D3D11_BIND_DEPTH_STENCIL;
descDepth.CPUAccessFlags = 0;
descDepth.MiscFlags = 0;
hr = pd3dDevice->CreateTexture2D( &descDepth, NULL, &pDepthStencil );
```



## <a name="create-depth-stencil-state"></a>Crear estado de Depth-Stencil

El estado de la galería de símbolos de profundidad indica a la fase de combinación de salida cómo realizar la [prueba de la galería de símbolos de profundidad](d3d10-graphics-programming-guide-output-merger-stage.md). La prueba de profundidad-estarcido determina si se debe dibujar un píxel determinado.


```
D3D11_DEPTH_STENCIL_DESC dsDesc;

// Depth test parameters
dsDesc.DepthEnable = true;
dsDesc.DepthWriteMask = D3D11_DEPTH_WRITE_MASK_ALL;
dsDesc.DepthFunc = D3D11_COMPARISON_LESS;

// Stencil test parameters
dsDesc.StencilEnable = true;
dsDesc.StencilReadMask = 0xFF;
dsDesc.StencilWriteMask = 0xFF;

// Stencil operations if pixel is front-facing
dsDesc.FrontFace.StencilFailOp = D3D11_STENCIL_OP_KEEP;
dsDesc.FrontFace.StencilDepthFailOp = D3D11_STENCIL_OP_INCR;
dsDesc.FrontFace.StencilPassOp = D3D11_STENCIL_OP_KEEP;
dsDesc.FrontFace.StencilFunc = D3D11_COMPARISON_ALWAYS;

// Stencil operations if pixel is back-facing
dsDesc.BackFace.StencilFailOp = D3D11_STENCIL_OP_KEEP;
dsDesc.BackFace.StencilDepthFailOp = D3D11_STENCIL_OP_DECR;
dsDesc.BackFace.StencilPassOp = D3D11_STENCIL_OP_KEEP;
dsDesc.BackFace.StencilFunc = D3D11_COMPARISON_ALWAYS;

// Create depth stencil state
ID3D11DepthStencilState * pDSState;
pd3dDevice->CreateDepthStencilState(&dsDesc, &pDSState);
```



DepthEnable y StencilEnable habilitan (y deshabilitan) las pruebas de profundidad y estarcido. Establezca DepthEnable en **false** para deshabilitar las pruebas de profundidad y evitar la escritura en el búfer de profundidad. Establezca StencilEnable en **false** para deshabilitar las pruebas de estarcido y evitar la escritura en el búfer de estarcido (cuando DepthEnable es **false** y StencilEnable es **true**, la prueba de profundidad siempre pasa en la operación de estarcido).

DepthEnable solo afecta a la fase de combinación de salida, no afecta al recorte, a la diferencia de profundidad ni a la fijación de valores antes de que los datos se escriban en un sombreador de píxeles.

## <a name="bind-depth-stencil-data-to-the-om-stage"></a>Enlazar datos de Depth-Stencil a la fase de OM

Enlazar el estado de la galería de símbolos de profundidad.


```
// Bind depth stencil state
pDevice->OMSetDepthStencilState(pDSState, 1);
```



Enlazar el recurso de la galería de símbolos de profundidad mediante una vista.


```
D3D11_DEPTH_STENCIL_VIEW_DESC descDSV;
descDSV.Format = DXGI_FORMAT_D32_FLOAT_S8X24_UINT;
descDSV.ViewDimension = D3D11_DSV_DIMENSION_TEXTURE2D;
descDSV.Texture2D.MipSlice = 0;

// Create the depth stencil view
ID3D11DepthStencilView* pDSV;
hr = pd3dDevice->CreateDepthStencilView( pDepthStencil, // Depth stencil texture
                                         &descDSV, // Depth stencil desc
                                         &pDSV );  // [out] Depth stencil view

// Bind the depth stencil view
pd3dDeviceContext->OMSetRenderTargets( 1,          // One rendertarget view
                                &pRTV,      // Render target view, created earlier
                                pDSV );     // Depth stencil view for the render target
```



Se puede pasar una matriz de vistas de representación-destino a [**ID3D11DeviceContext:: OMSetRenderTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets), pero todas esas vistas de destino de representación se corresponden con una vista de galería de símbolos de profundidad única. La matriz de destino de representación en Direct3D 11 es una característica que permite que una aplicación se represente en varios destinos de representación simultáneamente en el nivel primitivo. Las matrices de destino de representación ofrecen mayor rendimiento que la configuración individual de destinos de representación con varias llamadas a **ID3D11DeviceContext:: OMSetRenderTargets** (esencialmente, el método empleado en Direct3D 9).

Todos los destinos de representación deben ser del mismo tipo de recurso. Si se usa el suavizado de contorno Multimuestra, todos los destinos de representación enlazados y los búferes de profundidad deben tener el mismo número de muestras.

Cuando se usa un búfer como destino de representación, no se admiten las pruebas de la galería de símbolos de profundidad y los diversos destinos de representación.

-   Hasta 8 destinos de representación se pueden enlazar simultáneamente.
-   Todos los destinos de representación deben tener el mismo tamaño en todas las dimensiones (ancho y alto, y profundidad para el tamaño 3D o de la matriz para los \* tipos de matriz).
-   Cada destino de representación puede tener un formato de datos diferente.
-   Las máscaras de escritura controlan los datos que se escriben en un destino de representación. El control de máscaras de escritura de salida controla el destino de cada representación y el nivel de cada componente de los datos que se escriben en los destinos de representación.

## <a name="advanced-stencil-techniques"></a>Técnicas avanzadas de estarcido

La parte de la galería de símbolos del búfer de estarcido de profundidad se puede usar para crear efectos de representación como composición, alineación y esquematización.

-   [Composición](#compositing)
-   [Marcas](#decaling)
-   [Contornos y siluetas](#outlines-and-silhouettes)
-   [Galería de símbolos de dos caras](#two-sided-stencil)
-   [Leer el búfer de Depth-Stencil como una textura](#reading-the-depth-stencil-buffer-as-a-texture)

### <a name="compositing"></a>Composición

La aplicación puede usar el búfer de estarcido para componer imágenes 2D o 3D en una escena 3D. Se utiliza una máscara en el búfer de estarcido para tapabar un área de la superficie de destino de representación. La información de 2D almacenada, como texto o mapas de bits, se puede escribir en el área ocluidos. Como alternativa, la aplicación puede representar primitivos 3D adicionales en la región enmascarada de estarcido de la superficie de destino de representación. Incluso puede representar una escena completa.

A menudo, los juegos componen varias escenas 3D juntas. Por ejemplo, los juegos de conducción suelen mostrar un reflejo de la vista trasera. El reflejo contiene la vista de la escena 3D detrás del controlador. En esencia, es una segunda escena 3D compuesta con la vista hacia delante del controlador.

### <a name="decaling"></a>Marcas

Las aplicaciones de Direct3D usan las marcas para controlar qué píxeles de una imagen primitiva determinada se dibujan en la superficie de destino de representación. Las aplicaciones aplican marcas a las imágenes de primitivas para permitir que los polígonos coplanoles se representen correctamente.

Por ejemplo, al aplicar las marcas de neumático y las líneas amarillas a un Roadway, las marcas deben aparecer directamente encima de la carretera. Sin embargo, los valores z de las marcas y la carretera son los mismos. Por lo tanto, es posible que el búfer de profundidad no produzca una separación limpia entre ambos. Algunos píxeles de la primitiva inversa se pueden representar encima de la primitiva delantera y viceversa. La imagen resultante parece Shimmer de fotograma a fotograma. Este efecto se denomina lucha z o flimmering.

Para solucionar este problema, use una galería de símbolos para enmascarar la sección de la primitiva inversa en la que aparecerá la calcomanía. Desactive el almacenamiento en búfer z y represente la imagen de la primitiva delantera en el área enmascarada de la superficie de representación-destino.

Se puede usar la combinación de varias texturas para resolver este problema.

### <a name="outlines-and-silhouettes"></a>Contornos y siluetas

Puede usar el búfer de estarcido para efectos más abstractos, como la esquematización y la silhouetting.

Si la aplicación realiza dos fases de representación: una para generar la máscara de la galería de símbolos y la segunda para aplicar la máscara de la galería de símbolos a la imagen, pero con los primitivos ligeramente más pequeños en el segundo paso: la imagen resultante contendrá solo el contorno de la primitiva. A continuación, la aplicación puede rellenar el área enmascarada de estarcido de la imagen con un color sólido, lo que proporciona al primitivo una apariencia en relieve.

Si la máscara de la galería de símbolos tiene el mismo tamaño y forma que la primitiva que se está representando, la imagen resultante contiene un hueco en el que el primitivo debe ser. A continuación, la aplicación puede rellenar el hueco con negro para producir una silueta de la primitiva.

### <a name="two-sided-stencil"></a>Two-Sided Galería de símbolos

Los volúmenes de sombra se usan para dibujar sombras con el búfer de estarcido. La aplicación calcula los volúmenes de sombra convertidos por geometría occluding, mediante el cálculo de los bordes de la silueta y la extrusión de la luz en un conjunto de volúmenes 3D. A continuación, estos volúmenes se representan dos veces en el búfer de estarcido.

La primera representación dibuja polígonos hacia delante e incrementa los valores del búfer de estarcido. La segunda representación dibuja los polígonos hacia delante del volumen de instantáneas y disminuye los valores de búfer de la galería de símbolos. Normalmente, todos los valores incrementados y disminuidos se cancelan entre sí. Sin embargo, la escena ya se representó con geometría normal, lo que provoca que algunos píxeles no superen la prueba de búfer z mientras se representa el volumen de la instantánea. Los valores que quedan en el búfer de estarcido se corresponden con los píxeles que están en la sombra. El resto del contenido del búfer de la galería de símbolos se usa como máscara, para que la combinación de alfa sea una gran cantidad de color negro que abarque a la escena. Con el búfer de estarcido que actúa como máscara, el resultado es oscurecer los píxeles que se encuentran en las sombras.

Esto significa que la geometría de la sombra se dibuja dos veces por origen de la luz, por lo que se pone presión sobre el rendimiento de los vértices de la GPU. La característica de galería de símbolos de dos caras se ha diseñado para mitigar esta situación. En este enfoque, hay dos conjuntos de estado de la galería de símbolos (denominados a continuación), uno para cada uno de los triángulos orientados delante y otro para los triángulos de cara a la inversa. De este modo, solo se dibuja un único paso por volumen de instantánea, por luz.

En el [ejemplo ShadowVolume10](https://msdn.microsoft.com/library/Ee416427(v=VS.85).aspx)se puede encontrar un ejemplo de implementación de una galería de símbolos de dos caras.

### <a name="reading-the-depth-stencil-buffer-as-a-texture"></a>Leer el búfer de Depth-Stencil como una textura

Un sombreador puede leer un búfer de estarcido de profundidad inactivo como textura. Una aplicación que lee un búfer de estarcido de profundidad como una textura se representa en dos fases, la primera pasada escribe en el búfer de la galería de símbolos de profundidad y el segundo paso Lee del búfer. Esto permite a un sombreador comparar los valores de profundidad o de estarcido previamente escritos en el búfer con el valor de la Currrently de píxeles que se está representando. El resultado de la comparación se puede usar para crear efectos como la asignación de sombras o las partículas flexibles en un sistema de partículas.

Para crear un búfer de estarcido de profundidad que se pueda usar como un recurso de estarcido de profundidad y un recurso de sombreador, es necesario realizar algunos cambios en el código de ejemplo de la sección [crear un recurso de Depth-Stencil](#create-a-depth-stencil-resource) .

-   El recurso de la galería de símbolos de profundidad debe tener un formato sin tipo, como el formato de DXGI \_ \_ R32 \_ sin tipo.
    ```
    descDepth.Format = DXGI_FORMAT_R32_TYPELESS;
    ```

    

-   El recurso de la galería de símbolos de profundidad debe usar tanto la galería de símbolos de \_ profundidad de enlace D3D10 como las marcas de enlace del \_ \_ \_ recurso de sombreador de enlace D3D10 \_ \_ .
    ```
    descDepth.BindFlags = D3D10_BIND_DEPTH_STENCIL | D3D10_BIND_SHADER_RESOURCE;
    ```

    

Además, es necesario crear una vista de recursos del sombreador para el búfer de profundidad mediante una estructura de DESC de la [**\_ vista de \_ recursos \_ \_ del sombreador D3D11**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc) y [**ID3D11Device:: CreateShaderResourceView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createshaderresourceview). La vista de recursos del sombreador usará un formato con tipo como **DXGI \_ format \_ R32 \_ float** equivalente al formato sin tipo especificado cuando se creó el recurso de estarcido de profundidad.

En la primera fase de representación, el búfer de profundidad se enlaza tal y como se describe en la sección [enlazar Depth-Stencil datos a la fase de OM](#bind-depth-stencil-data-to-the-om-stage) . Tenga en cuenta que el formato que se pasa a [**D3D11 \_ Depth \_ estarcido \_ View \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_view_desc). Format usará un formato con tipo como **DXGI \_ format \_ D32 \_ float**. Después del primer paso de representación, el búfer de profundidad contendrá los valores de profundidad de la escena.

En el segundo paso de representación, la función [**ID3D11DeviceContext:: OMSetRenderTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets) se usa para establecer la vista de la galería de símbolos de profundidad en **null** o en un recurso de estarcido de profundidad diferente y la vista de recursos del sombreador se pasa al sombreador mediante [**ID3D11EffectShaderResourceVariable:: SetResource**](id3dx11effectshaderresourcevariable-setresource.md). Esto permite al sombreador buscar los valores de profundidad calculados en la primera fase de representación. Tenga en cuenta que se debe aplicar una transformación para recuperar los valores de profundidad si el punto de vista de la primera fase de representación es diferente de la segunda fase de representación. Por ejemplo, si se usa una técnica de asignación de instantáneas, la primera fase de representación será desde la perspectiva de una fuente de luz, mientras que la segunda pasa desde la perspectiva del visor.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Fase de combinación de salida](d3d10-graphics-programming-guide-output-merger-stage.md)
</dt> <dt>

[Fases de canalización (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 