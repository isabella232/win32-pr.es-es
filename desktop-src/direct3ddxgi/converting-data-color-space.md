---
description: Para crear en la pantalla o realizar operaciones de punto flotante, debe trabajar en el espacio de color correcto.
ms.assetid: 1DD8E2D3-430F-4EE4-9C41-78736C904920
title: Conversión de datos para el espacio de colores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 391d7e1cfd2882603529e28261e6872020dfbb1bbf461a9fd6f5d03efb3aaee3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118289640"
---
# <a name="converting-data-for-the-color-space"></a>Conversión de datos para el espacio de colores

Para crear en la pantalla o realizar operaciones de punto flotante, debe trabajar en el espacio de color correcto. Se recomienda realizar operaciones de punto flotante en un espacio de color lineal. A continuación, para presentar las imágenes en la pantalla, convierta los datos en un espacio de colores estándar de datos RGB (sRGB, gamma 2.2-corrected). La presentación en la pantalla en el espacio de colores sRGB es importante para la precisión del color. Si las imágenes no se corrigen con gamma 2.2, asignan demasiados bits o demasiado ancho de banda para resaltar que las personas no pueden diferenciar, y demasiados bits o ancho de banda para los valores de sombra a los que las personas son sensibles, por lo que requerirían más bits o ancho de banda para mantener la misma calidad visual. Por lo tanto, para garantizar la mejor precisión del color, presente imágenes en la pantalla que estén corregidas con gamma 2.2.

-   [Precisión del color](#color-accuracy)
-   [Temas relacionados](#related-topics)

## <a name="color-accuracy"></a>Precisión del color

Para la presentación, los formatos de presentación con valores enteros (como [**DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM \_ SRGB,**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) [**DXGI \_ FORMAT \_ R10G10B10 \_ XR \_ BIAS \_ A2 \_ UNORM,**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)y así sucesivamente) siempre contienen datos corregidos gamma de sRGB. Los formatos de presentación con valores float (actualmente solo [**DXGI \_ FORMAT \_ R16G16B16A16 \_ FLOAT)**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)contienen datos con valores lineales.

El modificador de formato SRGB indica al sistema operativo que ayuda a la aplicación a colocar datos \_ sRGB en [](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) la pantalla. La aplicación siempre debe colocar datos sRGB en búferes de reserva con formatos con valores enteros para presentar los datos sRGB en la pantalla, incluso si los datos no tienen este modificador de formato en su nombre de formato. Para obtener una lista completa de los formatos de examen de pantalla:

-   [Compatibilidad con formato DXGI para hardware de nivel 12.1 de características de Direct3D](hardware-support-for-direct3d-12-1-formats.md)
-   [Compatibilidad con formato DXGI para hardware de nivel 12.0 de características de Direct3D](hardware-support-for-direct3d-12-0-formats.md)
-   [Compatibilidad con el formato DXGI para hardware de nivel 11.1 de características de Direct3D](format-support-for-direct3d-11-1-feature-level-hardware.md)
-   [Compatibilidad con formato DXGI para hardware de nivel 11.0 de características de Direct3D](format-support-for-direct3d-11-0-feature-level-hardware.md)
-   [Compatibilidad de hardware con formatos Direct3D 10Level9](/previous-versions//ff471324(v=vs.85))
-   [Compatibilidad de hardware con formatos de Direct3D 10.1](/previous-versions//cc627091(v=vs.85))
-   [Compatibilidad de hardware con formatos Direct3D 10](/previous-versions//cc627090(v=vs.85))

Al escribir valores de salida de punto flotante desde el sombreador de píxeles en vistas de destino de representación **(RenderTargetView** s) con el modificador de formato SRGB enlazado a la canalización , se convierten al espacio de color corregido \_ gamma 2.2. [](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) [](/windows/desktop/direct3d11/overviews-direct3d-11-graphics-pipeline) De forma similar, cuando las vistas de recursos de sombreador **(ShaderResourceView** s) con el modificador de formato SRGB están enlazadas a la canalización, los valores se convierten del espacio de color corregido por gamma 2.2 al espacio de color lineal cuando se leen desde \_ **shaderResourceView.** A continuación, el sombreador puede realizar operaciones en ellos.

Por ejemplo, use código similar a este para escribir valores de salida de punto flotante desde un sombreador en un **formato RenderTargetView:**


```
struct PSOut
{
    float4 color : SV_Target;
};

PSOut S( PSIn input )
{
    PSOut output;
    output.color = float4( 1.0, 0.0, 0.0, 1.0 );
    return output;
}
```



Cuando se devuelve la rutina 'S', los valores de punto flotante (1, 0, 0, 1) se convierten al **formato RenderTargetView.** A continuación, si asigna el \_ modificador de formato SRGB a **RenderTargetView,** se produce la conversión gamma. [](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

Estos son los pasos que se deben seguir para asegurarse de que el contenido que se muestra en la pantalla tiene la mejor precisión de color.

**Para garantizar la precisión del color en la canalización**

1.  Si una textura tiene contenido sRGB, asegúrese de que **ShaderResourceView** tiene el modificador de formato SRGB para que, al leer desde ShaderResourceView en el sombreador, convierta el contenido de textura del espacio de color corregido por \_ gamma [](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) 2.2 al espacio de  color lineal.
2.  Asegúrese de **que RenderTargetView también** tiene el modificador de formato SRGB para que los valores de salida del sombreador \_ se conviertan en gamma. [](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

Si sigue los pasos anteriores, al llamar al método [**IDXGISwapChain1::P resent1,**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) el contenido que se muestra en la pantalla tiene la mejor precisión de color.

Puede usar el método [**ID3D11Device::CreateRenderTargetView**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createrendertargetview) para crear vistas **\_ \_ \* \_ SRGB DE DXGI FORMAT** en búferes de reserva desde una cadena de intercambio que cree solo con un formato **\_ DXGI FORMAT \_ \* \_ UNORM.** Se trata de una excepción especial a la regla para crear vistas de destino de representación, que indica que puede usar un formato diferente con **ID3D11Device::CreateRenderTargetView** solo si ha creado el recurso que desea ver con **DXGI \_ FORMAT \_ \* \_ TYPELESS**.

Para obtener más información sobre las reglas para convertir datos, vea [Reglas de conversión de datos](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-data-conversion).

Para obtener información sobre cómo leer y escribir simultáneamente en una textura, vea [Unpacking and Packing DXGI \_ FORMAT for In-Place Image Editing](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-unpacking-packing-dxgi-format)(Desempaquetar y empaquetar DXGI FORMAT para editar imágenes).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mejora de la presentación con el modelo de volteo, rectángulos sucios y áreas desplazadas](dxgi-1-2-presentation-improvements.md)
</dt> </dl>

 

 
