---
description: Para componer en la pantalla o realizar operaciones de punto flotante, debe trabajar en el espacio de color correcto.
ms.assetid: 1DD8E2D3-430F-4EE4-9C41-78736C904920
title: Conversión de datos para el espacio de colores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91b5dbec2f826c40d5274cbddb3b54d1cdd9f695
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805600"
---
# <a name="converting-data-for-the-color-space"></a>Conversión de datos para el espacio de colores

Para componer en la pantalla o realizar operaciones de punto flotante, debe trabajar en el espacio de color correcto. Se recomienda realizar operaciones de punto flotante en un espacio de colores lineal. A continuación, para presentar las imágenes en la pantalla, convierta los datos en un espacio de colores de datos RGB estándar (sRGB, gamma 2,2-corregido). La presentación en la pantalla en el espacio de color sRGB es importante para la precisión del color. Si las imágenes no tienen una corrección de gamma 2,2, asignan demasiados bits o demasiado ancho de banda para resaltar que las personas no pueden diferenciar, y demasiado pocos bits o ancho de banda para prevalecer sobre los valores a los que los usuarios son confidenciales, por lo que necesitaría más bits o ancho de banda para mantener la misma calidad visual. Por lo tanto, para garantizar la mejor precisión del color, presente imágenes en la pantalla que sean gamma 2,2-corregido.

-   [Precisión del color](#color-accuracy)
-   [Temas relacionados](#related-topics)

## <a name="color-accuracy"></a>Precisión del color

En cuanto a presentación, los formatos de presentación con valores enteros (como el [**formato de dxgi \_ \_ B8G8R8A8 \_ UNORM \_ sRGB**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), el [**\_ formato dxgi \_ R10G10B10 \_ XR \_ \_ \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), y así sucesivamente) siempre contienen datos con corrección gamma. Los formatos de visualización con valores de punto flotante (actualmente solo el [**formato de DXGI \_ \_ R16G16B16A16 \_ float**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)) contienen datos con valores lineales.

El \_ [modificador de formato](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) sRGB indica al sistema operativo que ayude a la aplicación a colocar datos sRGB en la pantalla. La aplicación debe colocar siempre los datos sRGB en búferes de reserva con formatos con valores enteros para presentar los datos sRGB en la pantalla, aunque los datos no tengan este modificador de formato en el nombre de formato. Para obtener una lista completa de los formatos de análisis de la presentación:

-   [Compatibilidad con el formato de DXGI para el hardware de nivel de característica de Direct3D 12,1](hardware-support-for-direct3d-12-1-formats.md)
-   [Compatibilidad con el formato de DXGI para el hardware de nivel de característica de Direct3D 12,0](hardware-support-for-direct3d-12-0-formats.md)
-   [Compatibilidad con el formato de DXGI para el hardware de nivel de característica de Direct3D 11,1](format-support-for-direct3d-11-1-feature-level-hardware.md)
-   [Compatibilidad con el formato de DXGI para el hardware de nivel de característica de Direct3D 11,0](format-support-for-direct3d-11-0-feature-level-hardware.md)
-   [Compatibilidad de hardware con formatos 10Level9 de Direct3D](/previous-versions//ff471324(v=vs.85))
-   [Compatibilidad de hardware con formatos de Direct3D 10,1](/previous-versions//cc627091(v=vs.85))
-   [Compatibilidad de hardware con formatos de Direct3D 10](/previous-versions//cc627090(v=vs.85))

Al escribir valores de salida de punto flotante desde el sombreador de píxeles en vistas de destino de representación (**RenderTargetView** s) con el \_ [modificador de formato](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) sRGB que está enlazado a la [canalización](/windows/desktop/direct3d11/overviews-direct3d-11-graphics-pipeline), los convierte en el espacio de colores de gamma 2,2. Del mismo modo, cuando las vistas de recursos del sombreador (**ShaderResourceView** s) con el \_ modificador de formato sRGB están enlazadas a la canalización, los valores se convierten de un espacio de colores de gamma 2,2 a un espacio de colores lineal cuando se leen desde **ShaderResourceView** s. A continuación, el sombreador puede realizar operaciones en ellos.

Por ejemplo, use código similar a este para escribir valores de salida de punto flotante de un sombreador en un formato **RenderTargetView** :


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



Cuando se devuelve la rutina ' de ', los valores de punto flotante (1, 0, 0, 1) se convierten al formato **RenderTargetView** . Después, si asigna el \_ [modificador de formato](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) sRGB a **RenderTargetView**, se produce la conversión gamma.

Estos son los pasos que se deben seguir para asegurarse de que el contenido que se muestra en la pantalla tiene la mejor precisión del color.

**Para garantizar la precisión del color de la canalización**

1.  Si una textura tiene contenido sRGB, asegúrese de que el **ShaderResourceView** tenga el \_ [modificador de formato](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) sRGB, de modo que cuando lea desde el **ShaderResourceView** en el sombreador, convierta el contenido de la textura del espacio de colores gamma 2,2-corregido al espacio de colores lineal.
2.  Asegúrese de que **RenderTargetView** tenga también \_ el [modificador de formato](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) sRGB para que los valores de salida del sombreador se conviertan en gamma.

Si sigue los pasos anteriores, al llamar al método [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) , el contenido que se muestra en la pantalla tiene la mejor precisión del color.

Puede usar el método [**ID3D11Device:: CreateRenderTargetView**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createrendertargetview) para crear vistas **\_ \_ \* \_ sRGB con formato de dxgi** en búferes de reserva desde una cadena de intercambio que solo se crea con un formato de formato de **dxgi \_ \_ \* \_ UNORM** . Esta es una excepción especial a la regla para crear vistas de representación y destino, que indica que puede usar un formato diferente con **ID3D11Device:: CreateRenderTargetView** solo si ha creado el recurso que desea ver con el **formato de DXGI sin \_ \_ \* \_ tipo**.

Para obtener más información sobre las reglas de conversión de datos, vea [reglas de conversión de datos](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-data-conversion).

Para obtener información sobre cómo leer y escribir simultáneamente en una textura, consulte [desempaquetar y empaquetar el \_ formato de DXGI para la edición de In-Place imagen](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-unpacking-packing-dxgi-format).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mejorar la presentación con el modelo de volteo, los rectángulos modificados y las áreas desplazadas](dxgi-1-2-presentation-improvements.md)
</dt> </dl>

 

 
