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
ms.openlocfilehash: d5b260741cae6aebb447a11692f03dad6e35498a19f33221aa77ac8a8507144a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119917165"
---
# <a name="supported-pixel-formats-and-alpha-modes"></a>Formatos de píxel admitidos y modos alfa

En este tema se describen los formatos de píxel y los modos alfa admitidos por las distintas partes de Direct2D, incluidos cada tipo de destino de representación, [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)e [**ID2D1ImageSource.**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource) Contiene las siguientes secciones:

-   [Formatos YUV admitidos para el origen de imagen DXGI](#supported-yuv-formats-for-dxgi-image-source)
-   [Especificar un formato de píxel para un destino de representación](#specifying-a-pixel-format-for-a-render-target)
-   [Formatos admitidos para ID2D1HwndRenderTarget](#supported-formats-for-id2d1hwndrendertarget)
-   [Formatos admitidos para ID2D1DeviceContext](#supported-formats-for-id2d1devicecontext)
-   [Formatos admitidos para el destino de representación compatible](#supported-formats-for-compatible-render-target)
-   [Formatos admitidos para el destino de representación de superficie DXGI](#supported-formats-for-dxgi-surface-render-target)
-   [Formatos admitidos para el destino de representación de mapa de bits de WIC](#supported-formats-for-wic-bitmap-render-target)
-   [Formatos admitidos para ID2D1DCRenderTarget](#supported-formats-for-id2d1dcrendertarget)
-   [Especificar un formato de píxel para un id2D1Bitmap](#specifying-a-pixel-format-for-an-id2d1bitmap)
    -   [Formatos de WIC admitidos](#supported-wic-formats)
-   [Usar un formato no compatible](#using-an-unsupported-format)
-   [Acerca de los modos alfa](#about-alpha-modes)
    -   [Acerca de los modos alfa premultiplicado y recta](#about-premultiplied-and-straight-alpha-modes)
    -   [Diferencias entre alfa recta y alfa premultiplicada](#the-differences-between-straight-and-premultiplied-alpha)
    -   [Modo alfa para destinos de representación](#alpha-mode-for-render-targets)
    -   [Modos ClearType y Alpha](#cleartype-and-alpha-modes)
-   [Temas relacionados](#related-topics)

## <a name="supported-yuv-formats-for-dxgi-image-source"></a>Formatos YUV admitidos para el origen de imagen DXGI

[**Id2D1ImageSource es**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource) un proveedor abstracto de píxeles. Se pueden crear instancias desde WIC ([**CreateImageSourceFromWic**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_id2d1imagesourcefromwic)) o [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) ([**CreateImageSourceFromDxgi**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromdxgi)).

[**ID2D1ImageSourceFromWic admite**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic) el mismo conjunto de formatos de píxel y modos alfa que [**ID2D1Bitmap.**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)

Además de lo anterior, un [**id2D1ImageSource del**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource) que se crea una instancia desde [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) también admite algunos formatos de píxeles YUV, incluidos los datos planas divididos en varias superficies. Vea [**CreateImageSourceFromDxgi para**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromdxgi) obtener más información sobre los requisitos para cada formato de píxel.



| Formato                    |
|---------------------------|
| FORMATO DXGI \_ \_ AYUV        |
| FORMATO DXGI \_ \_ NV12        |
| DXGI \_ FORMAT \_ YUY2        |
| FORMATO \_ DXGI \_ P208        |
| DXGI \_ FORMAT \_ V208        |
| FORMATO DXGI \_ \_ V408        |
| DXGI \_ FORMAT \_ R8 \_ UNORM   |
| DXGI \_ FORMAT \_ R8G8 \_ UNORM |



 

## <a name="specifying-a-pixel-format-for-a-render-target"></a>Especificar un formato de píxel para un destino de representación

Al crear un destino de representación, debe especificar su formato de píxel. Para especificar el formato de píxel, use una estructura [**D2D1 \_ PIXEL \_ FORMAT**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format) para establecer el **miembro pixelFormat** de una estructura [**RENDER TARGET PROPERTIES \_ \_ \_ de D2D1.**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) A continuación, pase esa estructura al método Create adecuado, como [**ID2D1Factory::CreateHwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)).

La [**estructura D2D1 \_ PIXEL \_ FORMAT**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format) tiene dos campos:

-   **format**, un [valor DXGI \_ FORMAT](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) que describe el tamaño y la organización de los canales en cada píxel, y
-   **alpha**, un [**valor D2D1 \_ ALPHA \_ MODE**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) que describe cómo se interpreta la información alfa.

En el ejemplo siguiente se crea una estructura [**\_ PIXEL \_ FORMAT D2D1**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format) y se usa para especificar el formato de píxel y el modo alfa de [**un id2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget).


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



Los distintos destinos de representación admiten combinaciones de formato y modo alfa diferentes. En las secciones siguientes se incluyen las combinaciones de formato y alfa admitidas por cada destino de representación.

## <a name="supported-formats-for-id2d1hwndrendertarget"></a>Formatos admitidos para ID2D1HwndRenderTarget

Los formatos admitidos para [**un ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) dependen de si se representa mediante hardware o software, o de si Direct2D controla el modo de representación automáticamente de forma predeterminada.

> [!Note]  
> Se recomienda usar [**DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM como**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) formato de píxel para mejorar el rendimiento. Esto resulta especialmente útil para los destinos de representación de software. Los destinos de formato BGRA se realizan mejor que los formatos RGBA.

 

Cuando se crea un [**id2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget), se usa la estructura RENDER TARGET PROPERTIES de [**D2D1 \_ \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) para especificar opciones de representación. Las opciones incluyen el formato de píxel, como se indicó en la sección anterior. El campo type de esta estructura permite especificar si el destino de representación se representa en hardware o software, o si Direct2D debe determinar automáticamente el modo de representación.

Para permitir que Direct2D determine si el destino de representación usa la representación de hardware o software, use la configuración [**D2D1 \_ RENDER TARGET TYPE \_ \_ \_ DEFAULT.**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type)

En la tabla siguiente se enumeran los formatos admitidos para los objetos [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) que se crean mediante el valor [**D2D1 \_ RENDER TARGET TYPE \_ \_ \_ DEFAULT.**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type)



| Formato                        | Modo alfa                       |
|-------------------------------|----------------------------------|
| DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM | MODO ALFA D2D1 \_ \_ \_ PREMULTIPLICADO |
| DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM | D2D1 \_ ALPHA \_ MODE \_ IGNORE        |
| DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM | MODO ALFA D2D1 \_ \_ \_ DESCONOCIDO       |
| FORMATO DXGI \_ \_ DESCONOCIDO         | MODO ALFA D2D1 \_ \_ \_ PREMULTIPLICADO |
| FORMATO DXGI \_ \_ DESCONOCIDO         | D2D1 \_ ALPHA \_ MODE \_ IGNORE        |
| FORMATO DXGI \_ \_ DESCONOCIDO         | MODO ALFA D2D1 \_ \_ \_ DESCONOCIDO       |



 

Para forzar que un destino de representación use la representación de hardware, use la configuración [**D2D1 \_ RENDER TARGET TYPE \_ \_ \_ HARDWARE.**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) En la tabla siguiente se enumeran los formatos admitidos para [**los objetos ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) que usan explícitamente la representación de hardware.



| Formato                        | Modo alfa                       |
|-------------------------------|----------------------------------|
| DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM | MODO ALFA D2D1 \_ \_ \_ PREMULTIPLICADO |
| DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM | D2D1 \_ ALPHA \_ MODE \_ IGNORE        |
| DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM | MODO ALFA D2D1 \_ \_ \_ DESCONOCIDO       |
| DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM | MODO ALFA D2D1 \_ \_ \_ PREMULTIPLICADO |
| DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM | D2D1 \_ ALPHA \_ MODE \_ IGNORE        |
| DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM | MODO ALFA D2D1 \_ \_ \_ DESCONOCIDO       |
| FORMATO DXGI \_ \_ DESCONOCIDO         | MODO ALFA D2D1 \_ \_ \_ PREMULTIPLICADO |
| FORMATO DXGI \_ \_ DESCONOCIDO         | D2D1 \_ ALPHA \_ MODE \_ IGNORE        |
| FORMATO DXGI \_ \_ DESCONOCIDO         | MODO ALFA D2D1 \_ \_ \_ DESCONOCIDO       |



 

Para forzar que un destino de representación use la representación de software, use la configuración [**D2D1 \_ RENDER TARGET TYPE \_ \_ \_ SOFTWARE.**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) En la tabla siguiente se enumeran los formatos admitidos para [**los objetos ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) que usan explícitamente la representación de software.



| Formato                        | Modo alfa                       |
|-------------------------------|----------------------------------|
| DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM | MODO ALFA D2D1 \_ \_ \_ PREMULTIPLICADO |
| DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM | D2D1 \_ ALPHA \_ MODE \_ IGNORE        |
| DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM | MODO ALFA D2D1 \_ \_ \_ DESCONOCIDO       |
| FORMATO DXGI \_ \_ DESCONOCIDO         | MODO ALFA D2D1 \_ \_ \_ PREMULTIPLICADO |
| FORMATO DXGI \_ \_ DESCONOCIDO         | D2D1 \_ ALPHA \_ MODE \_ IGNORE        |
| FORMATO DXGI \_ \_ DESCONOCIDO         | MODO ALFA D2D1 \_ \_ \_ DESCONOCIDO       |



 

Independientemente de si [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) está acelerado por hardware, el formato [DXGI \_ FORMAT \_ UNKNOWN](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) usa [DXGI \_ FORMAT \_ B8G8R8A8](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) de forma predeterminada y el modo alfa UNKNOWN del modo ALFA [**D2D1 \_ \_ \_**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) usa **D2D1 \_ ALPHA MODE \_ \_ IGNORE** de forma predeterminada.

## <a name="supported-formats-for-id2d1devicecontext"></a>Formatos admitidos para ID2D1DeviceContext

A partir Windows 8 el [**contexto del dispositivo**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) aprovecha más de los formatos de color alto de [**Direct3D,**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) como:

-   FORMATO DXGI \_ \_ B8G8R8A8 \_ UNORM \_ SRGB
-   FORMATO DXGI \_ \_ R8G8B8A8 \_ UNORM \_ SRGB
-   DXGI \_ FORMAT \_ R16G16B16A16 \_ UNORM
-   DXGI \_ FORMAT \_ R16G16B16A16 \_ FLOAT
-   DXGI \_ FORMAT \_ R32G32B32A32 \_ FLOAT

Use el [**método ID2D1DeviceContext::IsDxgiFormatSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isdxgiformatsupported) para ver si un formato funciona en un contexto de dispositivo determinado. Estos formatos también pueden funcionar en [**un id2D1HwndRenderTarget.**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget)

Estos formatos se suban a los formatos admitidos por la interfaz [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) Windows 7. Consulte [Devices and Device Contexts (Dispositivos y contextos de dispositivo)](devices-and-device-contexts.md) para obtener más información.

## <a name="supported-formats-for-compatible-render-target"></a>Formatos admitidos para el destino de representación compatible

Un destino de representación compatible [**(id2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget) creado por uno de los métodos [**ID2D1RenderTarget::CreateCompatibleRenderTarget)**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) hereda los formatos admitidos y los modos alfa del destino de representación que lo creó. Un destino de representación compatible también admite las siguientes combinaciones de formato y modo alfa, independientemente de lo que admita su elemento primario.



| Formato                  | Modo alfa                       |
|-------------------------|----------------------------------|
| DXGI \_ FORMAT \_ A8 \_ UNORM | MODO ALFA D2D1 \_ \_ \_ PREMULTIPLICADO |
| DXGI \_ FORMAT \_ A8 \_ UNORM | MODO ALFA D2D1 \_ \_ \_ DIRECTO      |
| FORMATO DXGI \_ \_ DESCONOCIDO   | MODO ALFA D2D1 \_ \_ \_ DESCONOCIDO       |



 

El [formato DXGI \_ FORMAT \_ UNKNOWN](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) usa el formato de destino de representación primario de forma predeterminada y el modo alfa UNKNOWN DEL MODO [**\_ ALFA \_ \_ D2D1**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) usa **D2D1 \_ ALPHA MODE \_ \_ PREMULTIPLIED** de forma predeterminada.

## <a name="supported-formats-for-dxgi-surface-render-target"></a>Formatos admitidos para el destino de representación de superficie DXGI

Un destino de representación DXGI es [**un ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) creado por uno de los métodos [**ID2D1Factory::CreateDxgiSurfaceRenderTarget.**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) Admite las siguientes combinaciones de formato y modo alfa.



| Formato                        | Modo alfa                       |
|-------------------------------|----------------------------------|
| DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM | MODO ALFA D2D1 \_ \_ \_ PREMULTIPLICADO |
| DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM | D2D1 \_ ALPHA \_ MODE \_ IGNORE        |
| DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM | MODO ALFA D2D1 \_ \_ \_ PREMULTIPLICADO |
| DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM | D2D1 \_ ALPHA \_ MODE \_ IGNORE        |
| DXGI \_ FORMAT \_ A8 \_ UNORM       | MODO ALFA D2D1 \_ \_ \_ PREMULTIPLICADO |
| DXGI \_ FORMAT \_ A8 \_ UNORM       | MODO ALFA D2D1 \_ \_ \_ DIRECTO      |
| FORMATO DXGI \_ \_ DESCONOCIDO         | MODO ALFA D2D1 \_ \_ \_ PREMULTIPLICADO |
| FORMATO DXGI \_ \_ DESCONOCIDO         | D2D1 \_ ALPHA \_ MODE \_ IGNORE        |



 

> [!Note]  
> El formato debe coincidir con el formato de la superficie DXGI a la que se dibuja el destino de representación de la superficie DXGI.

 

El [formato DXGI \_ FORMAT \_ UNKNOWN](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) usa el formato de superficie DXGI de forma predeterminada. No use el modo [**alfa D2D1 \_ ALPHA MODE UNKNOWN \_ \_ con**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) un destino de representación de superficie DXGI. No tiene ningún valor predeterminado y provocará un error en la creación del destino de representación de la superficie DXGI.

## <a name="supported-formats-for-wic-bitmap-render-target"></a>Formatos admitidos para el destino de representación de mapa de bits de WIC

Un destino de representación de mapa de bits de WIC es [**un ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) creado por uno de los métodos [**ID2D1Factory::CreateWicBitmapRenderTarget.**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties_id2d1rendertarget)) Admite las siguientes combinaciones de formato y modo alfa.



| Formato                        | Modo alfa                       |
|-------------------------------|----------------------------------|
| DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM | MODO ALFA D2D1 \_ \_ \_ PREMULTIPLICADO |
| DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM | D2D1 \_ ALPHA \_ MODE \_ IGNORE        |
| DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM | MODO ALFA D2D1 \_ \_ \_ DESCONOCIDO       |
| DXGI \_ FORMAT \_ A8 \_ UNORM       | MODO ALFA D2D1 \_ \_ \_ PREMULTIPLICADO |
| DXGI \_ FORMAT \_ A8 \_ UNORM       | MODO ALFA D2D1 \_ \_ \_ DIRECTO      |
| DXGI \_ FORMAT \_ A8 \_ UNORM       | MODO ALFA D2D1 \_ \_ \_ DESCONOCIDO       |
| FORMATO DXGI \_ \_ DESCONOCIDO         | MODO ALFA D2D1 \_ \_ \_ PREMULTIPLICADO |
| FORMATO DXGI \_ \_ DESCONOCIDO         | D2D1 \_ ALPHA \_ MODE \_ IGNORE        |
| FORMATO DXGI \_ \_ DESCONOCIDO         | MODO ALFA D2D1 \_ \_ \_ DESCONOCIDO       |



 

El formato de píxel del destino de mapa de bits de WIC debe coincidir con el formato de píxel del mapa de bits de WIC.

El [formato DXGI \_ FORMAT \_ UNKNOWN](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) usa el formato de mapa de bits WIC de forma predeterminada y el modo alfa UNKNOWN DEL MODO [**\_ ALFA \_ \_ D2D1**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) usa el modo alfa de mapa de bits WIC de forma predeterminada.

## <a name="supported-formats-for-id2d1dcrendertarget"></a>Formatos admitidos para ID2D1DCRenderTarget

[**Id2D1DCRenderTarget admite**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) las siguientes combinaciones de formato y modo alfa.



| Formato                        | Modo alfa                       |
|-------------------------------|----------------------------------|
| DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM | MODO ALFA D2D1 \_ \_ \_ PREMULTIPLICADO |
| DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM | D2D1 \_ ALPHA \_ MODE \_ IGNORE        |



 

No use el formato [DXGI \_ FORMAT \_ UNKNOWN](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ni el modo alfa DESCONOCIDO [**D2D1 \_ ALPHA MODE \_ \_ UNKNOWN**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) con [**id2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget). No tiene ningún valor predeterminado y provocará un error en la creación de **ID2D1DCRenderTarget.**

## <a name="specifying-a-pixel-format-for-an-id2d1bitmap"></a>Especificar un formato de píxel para un id2D1Bitmap

Por lo general, los objetos [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) admiten los siguientes formatos y modos alfa (con algunas restricciones, descritas en los párrafos siguientes).



| Formato                                                      | Modo alfa                       |
|-------------------------------------------------------------|----------------------------------|
| DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM                               | MODO ALFA D2D1 \_ \_ \_ PREMULTIPLICADO |
| DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM                               | OMITIR EL MODO ALFA D2D1 \_ \_ \_        |
| DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM                               | D2D1 \_ MODO \_ ALFA \_ DESCONOCIDO       |
| DXGI \_ FORMAT \_ A8 \_ UNORM                                     | MODO ALFA D2D1 \_ \_ \_ PREMULTIPLICADO |
| DXGI \_ FORMAT \_ A8 \_ UNORM                                     | MODO ALFA D2D1 \_ \_ \_ DIRECTO      |
| DXGI \_ FORMAT \_ A8 \_ UNORM                                     | D2D1 \_ MODO \_ ALFA \_ DESCONOCIDO       |
| FORMATO DXGI \_ \_ DESCONOCIDO                                       | MODO ALFA D2D1 \_ \_ \_ PREMULTIPLICADO |
| FORMATO DXGI \_ \_ DESCONOCIDO                                       | OMITIR EL MODO ALFA D2D1 \_ \_ \_        |
| FORMATO DXGI \_ \_ DESCONOCIDO                                       | D2D1 \_ MODO \_ ALFA \_ DESCONOCIDO       |
| DXGI \_ FORMAT \_ B8G8R8X8 \_ UNORM (Windows 8.1 y versiones posteriores, solo) | OMITIR EL MODO ALFA D2D1 \_ \_ \_        |
| DXGI \_ FORMAT \_ BC1 \_ UNORM (solo Windows 8.1 y versiones posteriores)      | MODO ALFA D2D1 \_ \_ \_ PREMULTIPLICADO |
| DXGI \_ FORMAT \_ BC1 \_ UNORM (solo Windows 8.1 y versiones posteriores)      | OMITIR EL MODO ALFA D2D1 \_ \_ \_        |
| DXGI \_ FORMAT \_ BC1 \_ UNORM (solo Windows 8.1 y versiones posteriores)      | D2D1 \_ MODO \_ ALFA \_ DESCONOCIDO       |
| DXGI \_ FORMAT \_ BC2 \_ UNORM (solo Windows 8.1 y versiones posteriores)      | MODO ALFA D2D1 \_ \_ \_ PREMULTIPLICADO |
| DXGI \_ FORMAT \_ BC2 \_ UNORM (solo Windows 8.1 y versiones posteriores)      | OMITIR EL MODO ALFA D2D1 \_ \_ \_        |
| DXGI \_ FORMAT \_ BC2 \_ UNORM (solo Windows 8.1 y versiones posteriores)      | D2D1 \_ MODO \_ ALFA \_ DESCONOCIDO       |
| DXGI \_ FORMAT \_ BC3 \_ UNORM (solo Windows 8.1 y versiones posteriores)      | MODO ALFA D2D1 \_ \_ \_ PREMULTIPLICADO |
| DXGI \_ FORMAT \_ BC3 \_ UNORM (solo Windows 8.1 y versiones posteriores)      | OMITIR EL MODO ALFA D2D1 \_ \_ \_        |
| DXGI \_ FORMAT \_ BC3 \_ UNORM (solo Windows 8.1 y versiones posteriores)      | D2D1 \_ MODO \_ ALFA \_ DESCONOCIDO       |



 

Cuando se usa el método [**ID2D1RenderTarget::CreateSharedBitmap,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) se usa el campo **pixelFormat** de una estructura BITMAP [**\_ \_ PROPERTIES de D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bitmap_properties) para especificar el formato de píxel del nuevo destino de representación. Debe coincidir con el formato de píxel del [**origen ID2D1Bitmap.**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)

Cuando se usa el método [**CreateBitmapFromWicBitmap,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties__id2d1bitmap)) se usa el campo **pixelFormat** de una estructura BITMAP PROPERTIES de [**D2D1 \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bitmap_properties) (en lugar del miembro **pixelFormat** de una estructura RENDER TARGET [**\_ \_ \_ PROPERTIES de D2D1)**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) para especificar el formato de píxel del nuevo destino de representación. Debe coincidir con el formato de píxel del origen de mapa de bits de WIC.

> [!Note]  
> Para obtener más información sobre la compatibilidad con formatos de píxeles comprimidos en bloques (BCn), vea [Compresión de bloques](block-compression.md).

 

### <a name="supported-wic-formats"></a>Formatos de WIC admitidos

Cuando se usa el [**método CreateBitmapFromWicBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties__id2d1bitmap)) para crear un mapa de bits a partir de un mapa de bits de WIC, o cuando se usa el método [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) con [**un IWICBitmapLock,**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmaplock)el origen de WIC debe estar en un formato compatible con Direct2D.



| Formato WIC                     | Formato DXGI correspondiente     | Modo alfa correspondiente                                        |
|--------------------------------|-------------------------------|-----------------------------------------------------------------|
| GUID \_ WICPixelFormat8bppAlpha  | DXGI \_ FORMAT \_ A8 \_ UNORM       | MODO ALFA D2D1 \_ \_ STRAIGHT o \_ D2D1 \_ ALPHA MODE \_ \_ PREMULTIPLIED |
| GUID \_ WICPixelFormat32bppPRGBA | DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM | MODO ALFA D2D1 \_ \_ \_ PREMULTIPLIED o D2D1 \_ ALPHA \_ MODE \_ IGNORE   |
| GUID \_ WICPixelFormat32bppBGR   | DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM | OMITIR EL MODO ALFA D2D1 \_ \_ \_                                       |
| GUID \_ WICPixelFormat32bppPBGRA | DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM | MODO ALFA D2D1 \_ \_ \_ PREMULTIPLICADO                                |



 

Para obtener un ejemplo en el que se muestra cómo convertir un mapa de bits de WIC a un formato [compatible,](how-to-load-a-direct2d-bitmap-from-a-file.md)vea Cómo cargar un mapa de bits desde un archivo .

## <a name="using-an-unsupported-format"></a>Usar un formato no compatible

El uso de cualquier combinación que no sea los formatos de píxel y los modos alfa que se muestran en las tablas anteriores da como resultado un formato de píxel no admitido de [**D2DERR \_ \_ \_**](direct2d-error-codes.md) o un error **E \_ INVALIDARG.**

## <a name="about-alpha-modes"></a>Acerca de los modos alfa

### <a name="about-premultiplied-and-straight-alpha-modes"></a>Acerca de los modos alfa premultiplicado y recta

La [**enumeración \_ D2D1 ALPHA \_ MODE**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) indica si el canal alfa usa alfa premultiplicado, alfa recta o debe omitirse y considerarse opaco. Con alfa recta, el canal alfa indica un valor que corresponde a lo transparente que es un color.

Los colores siempre se tratan como alfa recta mediante los comandos y pinceles de dibujo de Direct2D, independientemente del formato de destino.

Con alfa premultiplicado, el valor alfa escala cada canal de color. Normalmente, ningún valor de canal de color es mayor que el valor del canal alfa. Si un valor de canal de color en un formato multiplicado previamente es mayor que el canal alfa, la combinación estándar de origen sobre crea una mezcla aditiva.

El valor del propio canal alfa es el mismo tanto en alfa recta como multiplicada previamente.

### <a name="the-differences-between-straight-and-premultiplied-alpha"></a>Diferencias entre alfa recta y premultiplicada

Al describir un color RGBA mediante alfa recta, el valor alfa del color se almacena en el canal alfa. Por ejemplo, para describir un color rojo que sea 60 % opaco, use los siguientes valores: (255, 0, 0, 255 \* 0,6) = (255, 0, 0, 153). El valor 255 indica rojo completo y 153 (que es el 60 por ciento de 255) indica que el color debe tener una opacidad del 60 por ciento.

Al describir un color RGBA mediante alfa premultiplicado, cada color se multiplica por el valor alfa: (255 \* 0,6, 0 \* 0,6, 0 \* 0,6, 255 \* 0,6) = (153, 0, 0, 153).

Independientemente del modo alfa del destino de representación, los valores [**D2D1 \_ COLOR \_ F**](d2d1-color-f.md) siempre se interpretan como alfa recta. Por ejemplo, al especificar el color de [**un objeto ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) para su uso con un destino de representación que usa el modo alfa premultiplicado, especifique el color igual que lo haría si el destino de representación usara alfa recta. Al pintar con el pincel, Direct2D traduce el color al formato de destino automáticamente.

### <a name="alpha-mode-for-render-targets"></a>Modo alfa para destinos de representación

Independientemente de la configuración del modo alfa, el contenido de un destino de representación admite la transparencia. Por ejemplo, si dibuja un rectángulo rojo parcialmente transparente con un destino de representación con un modo alfa [**D2D1 \_ ALPHA \_ MODE \_ IGNORE**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode), el rectángulo aparecerá de color rosa (si el fondo es blanco).

Si dibuja un rectángulo rojo parcialmente transparente cuando el modo alfa es [**D2D1 \_ ALPHA \_ MODE \_ PREMULTIPLIED**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode), el rectángulo aparecerá de color rosa (suponiendo que el fondo sea blanco) y podrá ver a través de él lo que esté detrás del destino de representación. Esto resulta útil cuando se usa un [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) para representar en una ventana transparente o cuando se usa un destino de representación compatible (una representación destinada creada por el método [**CreateCompatibleRenderTarget)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) para crear un mapa de bits que admita transparencia.

### <a name="cleartype-and-alpha-modes"></a>Modos ClearType y Alpha

Si especifica un modo alfa distinto de [**D2D1 \_ ALPHA \_ MODE \_ IGNORE**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) para un destino de representación, el modo de suavizado de contorno de texto cambia automáticamente de [**D2D1 \_ TEXT \_ ANTIALIAS \_ MODE CLEARTYPE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_text_antialias_mode) a **D2D1 \_ TEXT \_ ANTIALIAS \_ MODE GRAYSCALE**. (Cuando se especifica un modo alfa de **D2D1 \_ ALPHA \_ MODE \_ UNKNOWN,** Direct2D establece el valor alfa automáticamente, en función del tipo de destino de representación).

Puede usar el método [**SetTextAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settextantialiasmode) para volver a cambiar el modo de suavizado de contorno de texto a [**D2D1 \_ TEXT \_ ANTIALIAS \_ MODE CLEARTYPE,**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_text_antialias_mode)pero la representación de texto ClearType en una superficie transparente puede crear resultados impredecibles. Si desea representar texto ClearType en un destino de representación transparente, se recomienda usar una de las dos técnicas siguientes.

-   Use el [**método PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f_d2d1_antialias_mode)) para recortar el destino de representación en el área donde se representará el texto, llame al método [**Clear**](id2d1rendertarget-clear.md) y especifique un color opaco y, a continuación, represente el texto.
-   Use [**DrawRectangle para**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f_id2d1brush_float_id2d1strokestyle)) dibujar un rectángulo opaco detrás del área donde se representará el texto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**FORMATO DE PÍXELES D2D1 \_ \_**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format)
</dt> <dt>

[**MODO ALFA D2D1 \_ \_**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode)
</dt> <dt>

[FORMATO \_ DXGI](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)
</dt> </dl>

 

 