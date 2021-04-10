---
title: Formatos de píxel admitidos y modos alfa
description: Describe los formatos de píxel y los modos alfa admitidos por cada tipo de destino de representación.
ms.assetid: 09b1f9c6-1780-4733-ac22-9e8c21466b67
keywords:
- Direct2D, formatos de píxel
- Direct2D, modos alfa
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 9a3777cac7cc0a258002d1475fb7b1c6dd2546ca
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "104149722"
---
# <a name="supported-pixel-formats-and-alpha-modes"></a>Formatos de píxel admitidos y modos alfa

En este tema se describen los formatos de píxel y los modos alfa admitidos por las distintas partes de Direct2D, incluidos los tipos de destino de representación, [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)y [**ID2D1ImageSource**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource). Contiene las siguientes secciones:

-   [Formatos YUV compatibles para el origen de imagen de DXGI](#supported-yuv-formats-for-dxgi-image-source)
-   [Especificar un formato de píxel para un destino de representación](#specifying-a-pixel-format-for-a-render-target)
-   [Formatos admitidos para ID2D1HwndRenderTarget](#supported-formats-for-id2d1hwndrendertarget)
-   [Formatos admitidos para ID2D1DeviceContext](#supported-formats-for-id2d1devicecontext)
-   [Formatos admitidos para el destino de representación compatible](#supported-formats-for-compatible-render-target)
-   [Formatos admitidos para el destino de representación de la superficie de DXGI](#supported-formats-for-dxgi-surface-render-target)
-   [Formatos admitidos para el destino de representación de mapas de bits WIC](#supported-formats-for-wic-bitmap-render-target)
-   [Formatos admitidos para ID2D1DCRenderTarget](#supported-formats-for-id2d1dcrendertarget)
-   [Especificar un formato de píxel para un ID2D1Bitmap](#specifying-a-pixel-format-for-an-id2d1bitmap)
    -   [Formatos WIC compatibles](#supported-wic-formats)
-   [Usar un formato no admitido](#using-an-unsupported-format)
-   [Acerca de los modos alfa](#about-alpha-modes)
    -   [Acerca de los modos alfa premultiplicados y rectos](#about-premultiplied-and-straight-alpha-modes)
    -   [Diferencias entre alfa recto y premultiplicado](#the-differences-between-straight-and-premultiplied-alpha)
    -   [Modo alfa para destinos de representación](#alpha-mode-for-render-targets)
    -   [Modos ClearType y Alpha](#cleartype-and-alpha-modes)
-   [Temas relacionados](#related-topics)

## <a name="supported-yuv-formats-for-dxgi-image-source"></a>Formatos YUV compatibles para el origen de imagen de DXGI

Un [**ID2D1ImageSource**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource) es un proveedor de píxeles abstracto. Se pueden crear instancias desde WIC ([**CreateImageSourceFromWic**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_id2d1imagesourcefromwic)) o [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) ([**CreateImageSourceFromDxgi**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromdxgi)).

[**ID2D1ImageSourceFromWic**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic) admite el mismo conjunto de formatos de píxeles y modos alfa que [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).

Además de lo anterior, un [**ID2D1ImageSource**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource) del que se crean instancias desde [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) también admite algunos formatos de píxeles YUV, incluida la división de datos planos en varias superficies. Consulte [**CreateImageSourceFromDxgi**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromdxgi) para obtener más información sobre los requisitos de cada formato de píxel.



| Formato                    |
|---------------------------|
| formato de DXGI \_ \_ AYUV        |
| Formato de DXGI \_ \_ NV12        |
| Formato de DXGI \_ \_ YUY2        |
| Formato de DXGI \_ \_ P208        |
| Formato de DXGI \_ \_ V208        |
| Formato de DXGI \_ \_ V408        |
| Formato de DXGI \_ \_ R8 \_ UNORM   |
| Formato de DXGI \_ \_ R8G8 \_ UNORM |



 

## <a name="specifying-a-pixel-format-for-a-render-target"></a>Especificar un formato de píxel para un destino de representación

Al crear un destino de representación, debe especificar su formato de píxel. Para especificar el formato de píxel, se usa una estructura de [**\_ \_ formato de píxel de D2D1**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format) para establecer el miembro **PixelFormat** de una estructura de propiedades de [**\_ \_ destino \_ de representación D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) . A continuación, se pasa esa estructura al método Create adecuado, como [**ID2D1Factory:: CreateHwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)).

La estructura de [**\_ \_ formato de píxel de D2D1**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format) tiene dos campos:

-   **formato**, un valor de [ \_ formato de DXGI](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) que describe el tamaño y la disposición de los canales en cada píxel.
-   **Alpha**, un valor de [**\_ \_ modo alfa D2D1**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) que describe cómo se interpreta la información alfa.

En el ejemplo siguiente se crea una estructura de [**\_ \_ formato de píxel de D2D1**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format) y se usa para especificar el formato de píxel y el modo alfa de un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget).


```C++
RECT rc;
GetClientRect(m_hwnd, &rc);

D2D1_SIZE_U size = D2D1::SizeU(
    rc.right - rc.left,
    rc.bottom - rc.top
    );

// Create a pixel format and initial its format
// and alphaMode fields.
D2D1_PIXEL_FORMAT pixelFormat = D2D1::PixelFormat(
    DXGI_FORMAT_B8G8R8A8_UNORM,
    D2D1_ALPHA_MODE_IGNORE
    );

D2D1_RENDER_TARGET_PROPERTIES props = D2D1::RenderTargetProperties();
props.pixelFormat = pixelFormat;

// Create a Direct2D render target.
hr = m_pD2DFactory->CreateHwndRenderTarget(
    props,
    D2D1::HwndRenderTargetProperties(m_hwnd, size),
    &m_pRT
    );

```



Distintos destinos de representación admiten diferentes combinaciones de formato alfa y de formato. En las secciones siguientes se enumeran las combinaciones de formato y alfa que admite cada destino de representación.

## <a name="supported-formats-for-id2d1hwndrendertarget"></a>Formatos admitidos para ID2D1HwndRenderTarget

Los formatos admitidos para un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) dependen de si se representa mediante hardware o software, o si Direct2D controla el modo de representación automáticamente de forma predeterminada.

> [!Note]  
> Se recomienda usar el [**formato de \_ DXGI \_ B8G8R8A8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) como formato de píxel para mejorar el rendimiento. Esto es especialmente útil para los destinos de representación de software. Los destinos de formato BGRA funcionan mejor que los formatos RGBA.

 

Cuando se crea una [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget), se usa la estructura de propiedades de destino de representación de D2D1 para especificar las opciones de representación. [**\_ \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) Las opciones incluyen el formato de píxel, tal como se indicó en la sección anterior. El campo de tipo de esta estructura le permite especificar si el destino de representación se representa en el hardware o software, o si Direct2D debe determinar automáticamente el modo de representación.

Para habilitar Direct2D para determinar si el destino de representación usa la representación de hardware o software, use la configuración [**predeterminada de tipo de destino de representación de D2D1 \_ \_ \_ \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) .

En la tabla siguiente se enumeran los formatos admitidos para los objetos [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) que se crean mediante la configuración predeterminada de tipo de [**destino de \_ representación \_ \_ \_ D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) .



| Formato                        | Modo alfa                       |
|-------------------------------|----------------------------------|
| Formato de DXGI \_ \_ B8G8R8A8 \_ UNORM | D2D1 \_ de \_ modo alfa \_ premultiplicado |
| Formato de DXGI \_ \_ B8G8R8A8 \_ UNORM | D2D1 \_ \_ modo alfa \_ omitir        |
| Formato de DXGI \_ \_ B8G8R8A8 \_ UNORM | \_Modo alfa \_ D2D1 \_ desconocido       |
| formato de DXGI \_ \_ desconocido         | D2D1 \_ de \_ modo alfa \_ premultiplicado |
| formato de DXGI \_ \_ desconocido         | D2D1 \_ \_ modo alfa \_ omitir        |
| formato de DXGI \_ \_ desconocido         | \_Modo alfa \_ D2D1 \_ desconocido       |



 

Para forzar a un destino de representación a usar la representación de hardware, use la configuración de [**\_ \_ \_ \_ hardware tipo de destino de representación de D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) . En la tabla siguiente se enumeran los formatos admitidos para los objetos [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) que usan explícitamente la representación de hardware.



| Formato                        | Modo alfa                       |
|-------------------------------|----------------------------------|
| Formato de DXGI \_ \_ B8G8R8A8 \_ UNORM | D2D1 \_ de \_ modo alfa \_ premultiplicado |
| Formato de DXGI \_ \_ B8G8R8A8 \_ UNORM | D2D1 \_ \_ modo alfa \_ omitir        |
| Formato de DXGI \_ \_ B8G8R8A8 \_ UNORM | \_Modo alfa \_ D2D1 \_ desconocido       |
| Formato de DXGI \_ \_ R8G8B8A8 \_ UNORM | D2D1 \_ de \_ modo alfa \_ premultiplicado |
| Formato de DXGI \_ \_ R8G8B8A8 \_ UNORM | D2D1 \_ \_ modo alfa \_ omitir        |
| Formato de DXGI \_ \_ R8G8B8A8 \_ UNORM | \_Modo alfa \_ D2D1 \_ desconocido       |
| formato de DXGI \_ \_ desconocido         | D2D1 \_ de \_ modo alfa \_ premultiplicado |
| formato de DXGI \_ \_ desconocido         | D2D1 \_ \_ modo alfa \_ omitir        |
| formato de DXGI \_ \_ desconocido         | \_Modo alfa \_ D2D1 \_ desconocido       |



 

Para forzar que un destino de representación use la representación de software, use la configuración de [**\_ \_ \_ \_ software tipo de destino de representación de D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) . En la tabla siguiente se enumeran los formatos admitidos para los objetos [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) que usan explícitamente la representación de software.



| Formato                        | Modo alfa                       |
|-------------------------------|----------------------------------|
| Formato de DXGI \_ \_ B8G8R8A8 \_ UNORM | D2D1 \_ de \_ modo alfa \_ premultiplicado |
| Formato de DXGI \_ \_ B8G8R8A8 \_ UNORM | D2D1 \_ \_ modo alfa \_ omitir        |
| Formato de DXGI \_ \_ B8G8R8A8 \_ UNORM | \_Modo alfa \_ D2D1 \_ desconocido       |
| formato de DXGI \_ \_ desconocido         | D2D1 \_ de \_ modo alfa \_ premultiplicado |
| formato de DXGI \_ \_ desconocido         | D2D1 \_ \_ modo alfa \_ omitir        |
| formato de DXGI \_ \_ desconocido         | \_Modo alfa \_ D2D1 \_ desconocido       |



 

Independientemente de si el [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) es acelerado por hardware, el formato de [dxgi \_ \_ desconocido](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) usa el formato de [dxgi \_ \_ B8G8R8A8](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) de forma predeterminada y el modo alfa D2D1 de modo Alpha utiliza el modo alfa **D2D1 \_ \_ \_ omitir** de forma predeterminada. [**\_ \_ \_**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode)

## <a name="supported-formats-for-id2d1devicecontext"></a>Formatos admitidos para ID2D1DeviceContext

A partir de Windows 8, el [**contexto de dispositivo**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) saca partido de los [**formatos de alto color de Direct3D**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) como:

-   Formato de DXGI \_ \_ B8G8R8A8 \_ UNORM \_ sRGB
-   Formato de DXGI \_ \_ R8G8B8A8 \_ UNORM \_ sRGB
-   Formato de DXGI \_ \_ R16G16B16A16 \_ UNORM
-   Formato de DXGI \_ \_ R16G16B16A16 \_ float
-   Formato de DXGI \_ \_ R32G32B32A32 \_ float

Use el método [**ID2D1DeviceContext:: IsDxgiFormatSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isdxgiformatsupported) para ver si un formato funciona en un contexto de dispositivo determinado. Estos formatos también pueden funcionar en un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget).

Estos formatos se suman a los formatos admitidos por la interfaz [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) en Windows 7. Consulte [dispositivos y contextos de dispositivo](devices-and-device-contexts.md) para obtener más información.

## <a name="supported-formats-for-compatible-render-target"></a>Formatos admitidos para el destino de representación compatible

Un destino de representación compatible (un [**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget) creado por uno de los métodos [**ID2D1RenderTarget:: CreateCompatibleRenderTarget**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) ) hereda los formatos admitidos y los modos alfa del destino de representación que lo creó. Un destino de representación compatible también admite las siguientes combinaciones de formato y modo alfa, independientemente de lo que admita su elemento primario.



| Formato                  | Modo alfa                       |
|-------------------------|----------------------------------|
| Formato de DXGI \_ \_ a8 \_ UNORM | D2D1 \_ de \_ modo alfa \_ premultiplicado |
| Formato de DXGI \_ \_ a8 \_ UNORM | D2D1 \_ \_ modo alfa \_ recto      |
| formato de DXGI \_ \_ desconocido   | \_Modo alfa \_ D2D1 \_ desconocido       |



 

El formato de [DXGI formato \_ \_ desconocido](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) usa el formato de destino de representación principal de forma predeterminada y el modo alfa [**\_ \_ \_ desconocido del modo**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) alfa de D2D1 utiliza el modo alfa **D2D1 \_ \_ \_ premultiplicado** de forma predeterminada.

## <a name="supported-formats-for-dxgi-surface-render-target"></a>Formatos admitidos para el destino de representación de la superficie de DXGI

Un destino de representación de DXGI es un [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) creado por uno de los métodos [**ID2D1Factory:: CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) . Admite las siguientes combinaciones de formato y modo alfa.



| Formato                        | Modo alfa                       |
|-------------------------------|----------------------------------|
| Formato de DXGI \_ \_ B8G8R8A8 \_ UNORM | D2D1 \_ de \_ modo alfa \_ premultiplicado |
| Formato de DXGI \_ \_ B8G8R8A8 \_ UNORM | D2D1 \_ \_ modo alfa \_ omitir        |
| Formato de DXGI \_ \_ R8G8B8A8 \_ UNORM | D2D1 \_ de \_ modo alfa \_ premultiplicado |
| Formato de DXGI \_ \_ R8G8B8A8 \_ UNORM | D2D1 \_ \_ modo alfa \_ omitir        |
| Formato de DXGI \_ \_ a8 \_ UNORM       | D2D1 \_ de \_ modo alfa \_ premultiplicado |
| Formato de DXGI \_ \_ a8 \_ UNORM       | D2D1 \_ \_ modo alfa \_ recto      |
| formato de DXGI \_ \_ desconocido         | D2D1 \_ de \_ modo alfa \_ premultiplicado |
| formato de DXGI \_ \_ desconocido         | D2D1 \_ \_ modo alfa \_ omitir        |



 

> [!Note]  
> El formato debe coincidir con el formato de la superficie de DXGI en la que se dibuja el destino de representación de la superficie de DXGI.

 

El formato de [dxgi \_ \_ desconocido](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) usa el formato de superficie de dxgi de forma predeterminada. No use el modo [**alfa \_ \_ \_ desconocido del modo D2D1 Alpha**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) con un destino de representación de la superficie de DXGI. No tiene ningún valor predeterminado y hará que se produzca un error en la creación del destino de representación de la superficie de DXGI.

## <a name="supported-formats-for-wic-bitmap-render-target"></a>Formatos admitidos para el destino de representación de mapas de bits WIC

Un destino de representación de mapas de bits WIC es un [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) creado por uno de los métodos [**ID2D1Factory:: CreateWicBitmapRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties_id2d1rendertarget)) . Admite las siguientes combinaciones de formato y modo alfa.



| Formato                        | Modo alfa                       |
|-------------------------------|----------------------------------|
| Formato de DXGI \_ \_ B8G8R8A8 \_ UNORM | D2D1 \_ de \_ modo alfa \_ premultiplicado |
| Formato de DXGI \_ \_ B8G8R8A8 \_ UNORM | D2D1 \_ \_ modo alfa \_ omitir        |
| Formato de DXGI \_ \_ B8G8R8A8 \_ UNORM | \_Modo alfa \_ D2D1 \_ desconocido       |
| Formato de DXGI \_ \_ a8 \_ UNORM       | D2D1 \_ de \_ modo alfa \_ premultiplicado |
| Formato de DXGI \_ \_ a8 \_ UNORM       | D2D1 \_ \_ modo alfa \_ recto      |
| Formato de DXGI \_ \_ a8 \_ UNORM       | \_Modo alfa \_ D2D1 \_ desconocido       |
| formato de DXGI \_ \_ desconocido         | D2D1 \_ de \_ modo alfa \_ premultiplicado |
| formato de DXGI \_ \_ desconocido         | D2D1 \_ \_ modo alfa \_ omitir        |
| formato de DXGI \_ \_ desconocido         | \_Modo alfa \_ D2D1 \_ desconocido       |



 

El formato de píxel del destino de mapa de bits de WIC debe coincidir con el formato de píxel del mapa de bits de WIC.

El formato de DXGI con formato [ \_ \_ desconocido](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) usa el formato de mapa de bits de WIC de forma predeterminada y el modo alfa [**\_ \_ \_ desconocido del modo alfa de D2D1**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) usa el modo alfa de mapa de bits de WIC de forma predeterminada.

## <a name="supported-formats-for-id2d1dcrendertarget"></a>Formatos admitidos para ID2D1DCRenderTarget

Un [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) admite las siguientes combinaciones de formato y modo alfa.



| Formato                        | Modo alfa                       |
|-------------------------------|----------------------------------|
| Formato de DXGI \_ \_ B8G8R8A8 \_ UNORM | D2D1 \_ de \_ modo alfa \_ premultiplicado |
| Formato de DXGI \_ \_ B8G8R8A8 \_ UNORM | D2D1 \_ \_ modo alfa \_ omitir        |



 

No use el formato [de \_ DXGI \_ Unknown](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) Format o el modo alfa [**\_ \_ \_ desconocido de D2D1**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) con un [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget). No tiene ningún valor predeterminado y hará que se produzca un error en la creación de **ID2D1DCRenderTarget** .

## <a name="specifying-a-pixel-format-for-an-id2d1bitmap"></a>Especificar un formato de píxel para un ID2D1Bitmap

Por lo general, los objetos [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) admiten los siguientes formatos y modos alfa (con algunas restricciones, que se describen en los párrafos siguientes).



| Formato                                                      | Modo alfa                       |
|-------------------------------------------------------------|----------------------------------|
| Formato de DXGI \_ \_ B8G8R8A8 \_ UNORM                               | D2D1 \_ de \_ modo alfa \_ premultiplicado |
| Formato de DXGI \_ \_ B8G8R8A8 \_ UNORM                               | D2D1 \_ \_ modo alfa \_ omitir        |
| Formato de DXGI \_ \_ B8G8R8A8 \_ UNORM                               | \_Modo alfa \_ D2D1 \_ desconocido       |
| Formato de DXGI \_ \_ a8 \_ UNORM                                     | D2D1 \_ de \_ modo alfa \_ premultiplicado |
| Formato de DXGI \_ \_ a8 \_ UNORM                                     | D2D1 \_ \_ modo alfa \_ recto      |
| Formato de DXGI \_ \_ a8 \_ UNORM                                     | \_Modo alfa \_ D2D1 \_ desconocido       |
| formato de DXGI \_ \_ desconocido                                       | D2D1 \_ de \_ modo alfa \_ premultiplicado |
| formato de DXGI \_ \_ desconocido                                       | D2D1 \_ \_ modo alfa \_ omitir        |
| formato de DXGI \_ \_ desconocido                                       | \_Modo alfa \_ D2D1 \_ desconocido       |
| \_Formato \_ de DXGI B8G8R8X8 \_ UNORM (Windows 8.1 y versiones posteriores, solo) | D2D1 \_ \_ modo alfa \_ omitir        |
| \_Formato \_ de DXGI BC1 \_ UNORM (Windows 8.1 y versiones posteriores, solo)      | D2D1 \_ de \_ modo alfa \_ premultiplicado |
| \_Formato \_ de DXGI BC1 \_ UNORM (Windows 8.1 y versiones posteriores, solo)      | D2D1 \_ \_ modo alfa \_ omitir        |
| \_Formato \_ de DXGI BC1 \_ UNORM (Windows 8.1 y versiones posteriores, solo)      | \_Modo alfa \_ D2D1 \_ desconocido       |
| \_Formato \_ de DXGI BC2 \_ UNORM (Windows 8.1 y versiones posteriores, solo)      | D2D1 \_ de \_ modo alfa \_ premultiplicado |
| \_Formato \_ de DXGI BC2 \_ UNORM (Windows 8.1 y versiones posteriores, solo)      | D2D1 \_ \_ modo alfa \_ omitir        |
| \_Formato \_ de DXGI BC2 \_ UNORM (Windows 8.1 y versiones posteriores, solo)      | \_Modo alfa \_ D2D1 \_ desconocido       |
| \_Formato \_ de DXGI BC3 \_ UNORM (Windows 8.1 y versiones posteriores, solo)      | D2D1 \_ de \_ modo alfa \_ premultiplicado |
| \_Formato \_ de DXGI BC3 \_ UNORM (Windows 8.1 y versiones posteriores, solo)      | D2D1 \_ \_ modo alfa \_ omitir        |
| \_Formato \_ de DXGI BC3 \_ UNORM (Windows 8.1 y versiones posteriores, solo)      | \_Modo alfa \_ D2D1 \_ desconocido       |



 

Cuando se usa el método [**ID2D1RenderTarget:: CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) , se usa el campo **PixelFormat** de una estructura de [**\_ \_ propiedades de mapa de bits de D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bitmap_properties) para especificar el formato de píxel del nuevo destino de representación. Debe coincidir con el formato de píxel del origen de [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) .

Cuando se usa el método [**CreateBitmapFromWicBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties__id2d1bitmap)) , se usa el campo **PixelFormat** de una estructura de [**\_ \_ propiedades de mapa de bits D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bitmap_properties) (en lugar del miembro **PixelFormat** de una estructura de propiedades de [**\_ \_ destino \_ de representación D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) ) para especificar el formato de píxel del nuevo destino de representación. Debe coincidir con el formato de píxel del origen de mapa de bits de WIC.

> [!Note]  
> Para obtener más información sobre la compatibilidad con los formatos de píxel comprimidos en bloques (BCn), consulte bloqueo de la [compresión](block-compression.md).

 

### <a name="supported-wic-formats"></a>Formatos WIC compatibles

Cuando se usa el método [**CreateBitmapFromWicBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties__id2d1bitmap)) para crear un mapa de bits a partir de un mapa de bits de WIC, o cuando se usa el método [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) con un [**IWICBITMAPLOCK**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmaplock), el origen de WIC debe tener un formato compatible con Direct2D.



| Formato WIC                     | Formato de DXGI correspondiente     | Modo alfa correspondiente                                        |
|--------------------------------|-------------------------------|-----------------------------------------------------------------|
| GUID \_ WICPixelFormat8bppAlpha  | Formato de DXGI \_ \_ a8 \_ UNORM       | D2D1 \_ \_ modo alfa \_ recto o D2D1 \_ \_ \_ premultiplicado |
| GUID \_ WICPixelFormat32bppPRGBA | Formato de DXGI \_ \_ R8G8B8A8 \_ UNORM | D2D1 modo alfa \_ \_ \_ premultiplicado o \_ D2D1 \_ modo alfa \_ omitir   |
| GUID \_ WICPixelFormat32bppBGR   | Formato de DXGI \_ \_ B8G8R8A8 \_ UNORM | D2D1 \_ \_ modo alfa \_ omitir                                       |
| GUID \_ WICPixelFormat32bppPBGRA | Formato de DXGI \_ \_ B8G8R8A8 \_ UNORM | D2D1 \_ de \_ modo alfa \_ premultiplicado                                |



 

Para obtener un ejemplo en el que se muestra cómo convertir un mapa de bits de WIC a un formato compatible, vea [Cómo cargar un mapa de bits desde un archivo](how-to-load-a-direct2d-bitmap-from-a-file.md).

## <a name="using-an-unsupported-format"></a>Usar un formato no admitido

El uso de cualquier combinación que no sea los formatos de píxel y los modos alfa que se enumeran en las tablas anteriores da como resultado un [**\_ \_ \_ formato de píxel no admitido de D2DERR**](direct2d-error-codes.md) o un error **E \_ INVALIDARG** .

## <a name="about-alpha-modes"></a>Acerca de los modos alfa

### <a name="about-premultiplied-and-straight-alpha-modes"></a>Acerca de los modos alfa premultiplicados y rectos

La enumeración de [**\_ \_ modo alfa D2D1**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) indica si el canal alfa usa alfa premultiplicado, alfa recto o debe omitirse y considerarse opaco. Con alfa recto, el canal alfa indica un valor que corresponde a la transparencia de un color.

Los colores siempre se tratan como alfa recto mediante comandos y pinceles de dibujo de Direct2D, independientemente del formato de destino.

Con alfa premultiplicado, cada canal de color se escala mediante el valor alfa. Normalmente, ningún valor de canal de color es mayor que el valor de canal alfa. Si un valor de canal de color en un formato premultiplicado es mayor que el canal alfa, la combinación de mezcla de origen a través de la mezcla matemática crea una mezcla aditiva.

El valor del canal alfa es el mismo en alfa recto y premultiplicado.

### <a name="the-differences-between-straight-and-premultiplied-alpha"></a>Diferencias entre alfa recto y premultiplicado

Al describir un color RGBA mediante el uso de alfa recto, el valor alfa del color se almacena en el canal alfa. Por ejemplo, para describir un color rojo de un 60% opaco, use los valores siguientes: (255, 0, 0, 255 \* 0,6) = (255, 0, 0, 153). El valor 255 indica rojo completo y 153 (que es 60 por ciento de 255) indica que el color debe tener una opacidad de 60 por ciento.

Al describir un color RGBA mediante el uso de alfa premultiplicado, cada color se multiplica por el valor alfa: (255 \* 0,6, 0 \* 0,6, 0 \* 0,6, 255 \* 0,6) = (153, 0, 0, 153).

Independientemente del modo alfa del destino de representación, los valores de [**\_ color \_ F de D2D1**](d2d1-color-f.md) siempre se interpretan como alfa recto. Por ejemplo, al especificar el color de un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) para su uso con un destino de representación que usa el modo alfa premultiplicado, especifique el color tal como lo haría si el destino de representación usara el alfa recto. Al pintar con el pincel, Direct2D traduce el color al formato de destino.

### <a name="alpha-mode-for-render-targets"></a>Modo alfa para destinos de representación

Independientemente de la configuración del modo alfa, el contenido de un destino de representación admite la transparencia. Por ejemplo, si dibuja un rectángulo rojo totalmente transparente con un destino de representación con un modo alfa de [**D2D1 \_ alpha \_ Mode \_ Ignore**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode), el rectángulo aparecerá en rosa (si el fondo es blanco).

Si dibuja un rectángulo rojo parcialmente transparente cuando el modo alfa es [**\_ \_ \_ premultiplicado**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode)por el modo alfa D2D1, el rectángulo aparecerá de color rosa (suponiendo que el fondo es blanco) y puede ver lo que hay detrás del destino de representación. Esto resulta útil cuando se usa un [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) para representarlo en una ventana transparente o cuando se usa un destino de representación compatible (una representación de destino creada por el método [**CreateCompatibleRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) ) para crear un mapa de bits que admita la transparencia.

### <a name="cleartype-and-alpha-modes"></a>Modos ClearType y Alpha

Si especifica un modo alfa que no sea el [**modo de D2D1 \_ alfa \_ \_**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) para un destino de representación, el modo de suavizado de contorno de texto cambia automáticamente del modo de [**\_ \_ suavizado \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_text_antialias_mode) de contorno de texto D2D1 al modo de desalias de **\_ texto D2D1 \_ \_**. (Cuando se especifica un modo alfa de **\_ modo alfa \_ D2D1 \_ desconocido**, Direct2D establece el alfa en función del tipo de destino de representación).

Puede usar el método [**SetTextAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settextantialiasmode) para cambiar el modo de suavizado de contorno de texto a [**\_ CLEARTYPE en \_ \_ modo de suavizado de texto D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_text_antialias_mode), pero la representación de texto ClearType en una superficie transparente puede crear resultados imprevisibles. Si desea representar texto ClearType en un destino de representación transparente, se recomienda usar una de las dos técnicas siguientes.

-   Use el método [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f_d2d1_antialias_mode)) para recortar el destino de representación en el área donde se representará el texto, después llame al método [**Clear**](id2d1rendertarget-clear.md) y especifique un color opaco y, a continuación, represente el texto.
-   Use [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f_id2d1brush_float_id2d1strokestyle)) para dibujar un rectángulo opaco detrás del área donde se representará el texto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**\_Formato de píxel de D2D1 \_**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format)
</dt> <dt>

[**\_Modo alfa \_ D2D1**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode)
</dt> <dt>

[formato de DXGI \_](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)
</dt> </dl>

 

 