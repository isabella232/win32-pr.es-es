---
title: Configuración de Depth-Stencil funcionalidad
description: En esta sección se tratan los pasos para configurar el búfer de galería de símbolos de profundidad y el estado de la galería de símbolos de profundidad para la fase de fusión de salida.
ms.assetid: e8f52d5f-266f-4e2c-b38d-d7fd9e27fe1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e994c5a11215d245d8101edff410a91ffb788583b07f651fdfbd1f2771d7deab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990195"
---
# <a name="configuring-depth-stencil-functionality"></a>Configuración de Depth-Stencil funcionalidad

En esta sección se tratan los pasos para configurar el búfer de galería de símbolos de profundidad y el estado de la galería de símbolos de profundidad para la fase de fusión de salida.

-   [Creación de un Depth-Stencil recurso](#create-a-depth-stencil-resource)
-   [Crear Depth-Stencil estado](#create-depth-stencil-state)
-   [Enlazar Depth-Stencil datos a la fase de OM](#bind-depth-stencil-data-to-the-om-stage)

Una vez que sepa cómo usar el búfer de la galería de símbolos de profundidad y el estado de galería de símbolos de profundidad correspondiente, consulte técnicas avanzadas de galería [de símbolos](#advanced-stencil-techniques).

## <a name="create-a-depth-stencil-resource"></a>Creación de un Depth-Stencil recurso

Cree el búfer de galería de símbolos de profundidad mediante un recurso de textura.


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



## <a name="create-depth-stencil-state"></a>Crear Depth-Stencil estado

El estado de la galería de símbolos de profundidad indica a la fase de fusión de salida cómo realizar la prueba de galería [de símbolos de profundidad](d3d10-graphics-programming-guide-output-merger-stage.md). La prueba de galería de símbolos de profundidad determina si se debe dibujar o no un píxel determinado.


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



DepthEnable y StencilHabilite (y deshabilite) las pruebas de profundidad y galería de símbolos. Establezca DepthEnable en **FALSE para deshabilitar** las pruebas de profundidad y evitar la escritura en el búfer de profundidad. Establezca StencilEnable en **FALSE** para deshabilitar las pruebas de galería de símbolos y evitar la escritura en el búfer de la galería de símbolos (cuando DepthEnable es **FALSE** y StencilEnable es **TRUE,** la prueba de profundidad siempre pasa en la operación de galería de símbolos).

DepthEnable solo afecta a la fase de fusión de salida: no afecta al recorte, al sesgo de profundidad ni a la fijación de valores antes de que los datos se introduzcan en un sombreador de píxeles.

## <a name="bind-depth-stencil-data-to-the-om-stage"></a>Enlazar Depth-Stencil datos a la fase de OM

Enlace el estado de la galería de símbolos de profundidad.


```
// Bind depth stencil state
pDevice->OMSetDepthStencilState(pDSState, 1);
```



Enlace el recurso de galería de símbolos de profundidad mediante una vista.


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



Se puede pasar una matriz de vistas de destino de representación a [**ID3D11DeviceContext::OMSetRenderTargets,**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets)pero todas esas vistas de destino de representación se corresponderán con una sola vista de galería de símbolos de profundidad. La matriz de destino de representación en Direct3D 11 es una característica que permite que una aplicación se represente en varios destinos de representación simultáneamente en el nivel primitivo. Las matrices de destino de representación ofrecen un mayor rendimiento con respecto a la configuración individual de destinos de representación con varias llamadas a **ID3D11DeviceContext::OMSetRenderTargets** (básicamente, el método empleado en Direct3D 9).

Los destinos de representación deben ser del mismo tipo de recurso. Si se usa el suavizado de contorno de múltiples muestras, todos los destinos de representación enlazados y los búferes de profundidad deben tener los mismos recuentos de muestras.

Cuando se usa un búfer como destino de representación, no se admiten las pruebas de galería de símbolos de profundidad y varios destinos de representación.

-   Se pueden enlazar hasta 8 destinos de representación simultáneamente.
-   Todos los destinos de representación deben tener el mismo tamaño en todas las dimensiones (ancho y alto, y profundidad para 3D o tamaño de matriz para tipos \* de matriz).
-   Cada destino de representación puede tener un formato de datos diferente.
-   Las máscaras de escritura controlan qué datos se escriben en un destino de representación. La escritura de salida enmascara el control en un destino por representación, en el nivel de componente, qué datos se escriben en los destinos de representación.

## <a name="advanced-stencil-techniques"></a>Técnicas avanzadas de galería de símbolos

La parte de la galería de símbolos del búfer de la galería de símbolos de profundidad se puede usar para crear efectos de representación, como la composición, la descalización y la delineación.

-   [Composición](#compositing)
-   [Escalado](#decaling)
-   [Contornos y sobresalciones](#outlines-and-silhouettes)
-   [Galería de símbolos de dos lados](#two-sided-stencil)
-   [Leer el búfer Depth-Stencil como una textura](#reading-the-depth-stencil-buffer-as-a-texture)

### <a name="compositing"></a>Composición

La aplicación puede usar el búfer de galería de símbolos para componer imágenes 2D o 3D en una escena 3D. Se usa una máscara en el búfer de la galería de símbolos para occluir un área de la superficie de destino de representación. La información 2D almacenada, como texto o mapas de bits, se puede escribir en el área ocluida. Como alternativa, la aplicación puede representar primitivas 3D adicionales en la región enmascarada por galería de símbolos de la superficie de destino de representación. Incluso puede representar una escena completa.

Los juegos suelen componer varias escenas 3D juntas. Por ejemplo, los juegos de conducción suelen mostrar un reflejo de la vista trasera. El reflejo contiene la vista de la escena 3D detrás del controlador. Es básicamente una segunda escena 3D compuesta con la vista hacia delante del controlador.

### <a name="decaling"></a>Escalado

Las aplicaciones de Direct3D usan el escalado para controlar qué píxeles de una imagen primitiva determinada se dibujan en la superficie de destino de representación. Las aplicaciones aplican lascales a las imágenes de primitivas para permitir que los polígonos coplanares se represente correctamente.

Por ejemplo, al aplicar marcas de rueda y líneas amarillas a una carretera, las marcas deben aparecer directamente sobre la carretera. Sin embargo, los valores z de las marcas y la carretera son los mismos. Por lo tanto, es posible que el búfer de profundidad no produzca una separación limpia entre los dos. Algunos píxeles de la primitiva inversa se pueden representar sobre la primitiva frontal y viceversa. La imagen resultante parece atenuar de marco a marco. Este efecto se denomina z-fighting o flimmering.

Para solucionar este problema, use una galería de símbolos para enmascarar la sección de la primitiva posterior donde aparecerá lacal. Desactive el almacenamiento en búfer z y represente la imagen de la primitiva frontal en el área enmascarada de la superficie de destino de representación.

Se puede usar la combinación de varias texturas para resolver este problema.

### <a name="outlines-and-silhouettes"></a>Contornos y sobresalciones

Puede usar el búfer de galería de símbolos para obtener efectos más abstractos, como la delineación y la silación.

Si la aplicación realiza dos pases de representación (uno para generar la máscara de galería de símbolos y el segundo para aplicar la máscara de galería de símbolos a la imagen, pero con las primitivas ligeramente más pequeñas en el segundo paso), la imagen resultante contendrá solo el contorno de la primitiva. A continuación, la aplicación puede rellenar el área enmascarada de la galería de símbolos de la imagen con un color sólido, lo que da a la primitiva una apariencia con relieve.

Si la máscara de galería de símbolos tiene el mismo tamaño y forma que la primitiva que está representando, la imagen resultante contiene un hueco donde debe estar la primitiva. A continuación, la aplicación puede rellenar el hueco de color negro para producir una desmesada de la primitiva.

### <a name="two-sided-stencil"></a>Two-Sided galería de símbolos

Los volúmenes de sombra se usan para dibujar sombras con el búfer de galería de símbolos. La aplicación calcula los volúmenes de sombra convertidos mediante la oclusión de la geometría, calculando los bordes de contorno y extruyéndolos de la luz en un conjunto de volúmenes 3D. Estos volúmenes se representan dos veces en el búfer de galería de símbolos.

La primera representación dibuja polígonos orientados hacia delante e incrementa los valores de stencil-buffer. La segunda representación dibuja los polígonos orientados hacia atrás del volumen de sombra y disminuye los valores del búfer de galería de símbolos. Normalmente, todos los valores incrementados y decrementados se cancelan entre sí. Sin embargo, la escena ya se representó con geometría normal, lo que provocaba que algunos píxeles no se realizaran en la prueba del búfer z a medida que se representaba el volumen de sombras. Los valores que quedan en el búfer de la galería de símbolos corresponden a píxeles que están en la sombra. Estos contenidos restantes del búfer de galería de símbolos se usan como máscara para combinar alfamente un cuadrándular negro grande que abarca todo el contenido de la escena. Con el búfer de galería de símbolos que actúa como una máscara, el resultado es que los píxeles oscuros están en las sombras.

Esto significa que la geometría de sombra se dibuja dos veces por fuente de luz, lo que supone presión sobre el rendimiento de vértices de la GPU. La característica de galería de símbolos de dos lados se ha diseñado para mitigar esta situación. En este enfoque, hay dos conjuntos de estado de galería de símbolos (denominados a continuación), uno para los triángulos orientados hacia delante y el otro para los triángulos orientados hacia atrás. De este modo, solo se dibuja un solo paso por volumen de sombra, por luz.

Puede encontrar un ejemplo de implementación de galería de símbolos de dos lados en [el ejemplo ShadowVolume10](https://msdn.microsoft.com/library/Ee416427(v=VS.85).aspx).

### <a name="reading-the-depth-stencil-buffer-as-a-texture"></a>Leer el búfer Depth-Stencil como una textura

Un sombreador puede leer un búfer de galería de símbolos de profundidad inactivo como una textura. Una aplicación que lee un búfer de galería de símbolos de profundidad como una textura se representa en dos pases, el primero escribe en el búfer de galería de símbolos de profundidad y el segundo se lee desde el búfer. Esto permite que un sombreador compare los valores de profundidad o galería de símbolos escritos previamente en el búfer con el valor del píxel que se representa de forma recurrente. El resultado de la comparación se puede usar para crear efectos como la asignación de sombras o las partículas soft en un sistema de partículas.

Para crear un búfer de galería de símbolos de profundidad que se pueda usar como un recurso de galería [](#create-a-depth-stencil-resource) de símbolos de profundidad y un recurso de sombreador, es necesario realizar algunos cambios en el código de ejemplo en la sección Crear un recurso Depth-Stencil profundidad.

-   El recurso de galería de símbolos de profundidad debe tener un formato sin tipo, como DXGI \_ FORMAT \_ R32 \_ TYPELESS.
    ```
    descDepth.Format = DXGI_FORMAT_R32_TYPELESS;
    ```

    

-   El recurso de galería de símbolos de profundidad debe usar las marcas de enlace D3D10 \_ BIND \_ DEPTH STENCIL y \_ D3D10 \_ BIND SHADER \_ \_ RESOURCE.
    ```
    descDepth.BindFlags = D3D10_BIND_DEPTH_STENCIL | D3D10_BIND_SHADER_RESOURCE;
    ```

    

Además, es necesario crear una vista de recursos de sombreador para el búfer de profundidad mediante una estructura [**D3D11 \_ SHADER RESOURCE VIEW \_ \_ \_ DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc) e [**ID3D11Device::CreateShaderResourceView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createshaderresourceview). La vista de recursos del sombreador usará un formato con tipo, **como DXGI \_ FORMAT \_ R32 \_ FLOAT,** que es el equivalente al formato sin tipo especificado cuando se creó el recurso de galería de símbolos de profundidad.

En el primer paso de representación, el búfer de profundidad se enlaza como se describe en la sección Enlazar [Depth-Stencil datos a la fase de OM.](#bind-depth-stencil-data-to-the-om-stage) Tenga en cuenta que el formato pasado a [**D3D11 \_ DEPTH \_ STENCIL \_ VIEW \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_view_desc). El formato usará un formato con tipo, **como DXGI \_ FORMAT \_ D32 \_ FLOAT.** Después del primer paso de representación, el búfer de profundidad contendrá los valores de profundidad de la escena.

En el segundo paso de representación, la función [**ID3D11DeviceContext::OMSetRenderTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets) se usa para establecer la vista de galería de símbolos de profundidad en **NULL** o en otro recurso de galería de símbolos de profundidad y la vista de recursos del sombreador se pasa al sombreador mediante [**ID3D11EffectShaderResourceVariable::SetResource**](id3dx11effectshaderresourcevariable-setresource.md). Esto permite que el sombreador busque los valores de profundidad calculados en el primer paso de representación. Tenga en cuenta que será necesario aplicar una transformación para recuperar los valores de profundidad si el punto de vista del primer paso de representación es diferente del segundo paso de representación. Por ejemplo, si se usa una técnica de asignación de sombras, el primer paso de representación será desde la perspectiva de una fuente de luz, mientras que el segundo paso de representación lo hará desde la perspectiva del visor.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Fase de fusión de salida](d3d10-graphics-programming-guide-output-merger-stage.md)
</dt> <dt>

[Fases de canalización (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 