---
title: Cómo crear un pincel de mapa de bits
description: Muestra cómo crear un pincel de mapa de bits mediante Direct2D.
ms.assetid: 8f78b30a-7507-4dd8-b6f4-12d88e3c9a1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d274d359b8ad8298a4e45d01014a6e9b19aa58c4b81725c5d8c41ac931e24eec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569305"
---
# <a name="how-to-create-a-bitmap-brush"></a>Cómo crear un pincel de mapa de bits

Para crear un pincel de mapa de bits, use el [**método ID2D1RenderTarget::CreateBitmapBrush**](id2d1rendertarget-createbitmapbrush.md) y especifique las propiedades del pincel de mapa de bits. Algunas sobrecargas permiten especificar las propiedades del pincel. En el código siguiente se muestra cómo crear un pincel de mapa de bits para rellenar un cuadrado y un pincel negro sólido para dibujar el contorno del cuadrado. El código genera la salida que se muestra en la siguiente captura de pantalla.

> [!Note]  
> A partir Windows 8, puede usar el método [**CreateBitmapBrush**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapbrush(id2d1bitmap_constd2d1_bitmap_brush_properties1_constd2d1_brush_properties_id2d1bitmapbrush1)) en la interfaz [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) para crear un [**objeto ID2D1BitmapBrush1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1bitmapbrush1) en lugar de **id2D1BitmapBrush.** **ID2D1BitmapBrush1** agrega modos de escalado de alta calidad al pincel de mapa de bits.

 

![captura de pantalla de un cuadrado relleno con un mapa de bits de planta](images/brushes-ovw-bitmap.png)

1.  Declare una variable de tipo [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).
    ```C++
        ID2D1BitmapBrush *m_pBitmapBrush;
    ```

    

2.  Cargar un mapa de bits desde un recurso. Para obtener más información, [vea How to Load a Bitmap from a Resource](how-to-load-a-bitmap-from-a-resource.md).
    ```C++
    // Create the bitmap to be used by the bitmap brush.
    if (SUCCEEDED(hr))
    {
        hr = LoadResourceBitmap(
            m_pRenderTarget,
            m_pWICFactory,
            L"FERN",
            L"Image",
            &m_pBitmap
            );
    ```

    

3.  Elija los modos de extensión ([**D2D1 \_ EXTEND \_ MODE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode)) y el modo de interpolación ([**D2D1 \_ BITMAP \_ INTERPOLATION \_ MODE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_bitmap_interpolation_mode)) del pincel de mapa de bits y, a continuación, llame al [**método CreateBitmapBrush**](id2d1rendertarget-createbitmapbrush.md) para crear un pincel, como se muestra en el código siguiente.
    ```C++
    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pBitmap,
        &m_pBitmapBrush
        );
    ```

    

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de Direct2D](reference.md)
</dt> </dl>

 

 