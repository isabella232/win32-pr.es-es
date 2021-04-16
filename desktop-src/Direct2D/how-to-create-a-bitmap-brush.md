---
title: Cómo crear un pincel de mapa de bits
description: Muestra cómo crear un pincel de mapa de bits mediante Direct2D.
ms.assetid: 8f78b30a-7507-4dd8-b6f4-12d88e3c9a1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd8f28735368916d1abd0c1c9aa091dec4fd93f4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676441"
---
# <a name="how-to-create-a-bitmap-brush"></a>Cómo crear un pincel de mapa de bits

Para crear un pincel de mapa de bits, use el método [**ID2D1RenderTarget:: CreateBitmapBrush**](id2d1rendertarget-createbitmapbrush.md) y especifique las propiedades de pincel de mapa de bits. Algunas sobrecargas le permiten especificar las propiedades del pincel. En el código siguiente se muestra cómo crear un pincel de mapa de bits para rellenar un cuadrado y un pincel negro sólido para dibujar el contorno del cuadrado. El código genera el resultado que se muestra en la siguiente captura de pantalla.

> [!Note]  
> A partir de Windows 8, puede usar el método [**CreateBitmapBrush**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapbrush(id2d1bitmap_constd2d1_bitmap_brush_properties1_constd2d1_brush_properties_id2d1bitmapbrush1)) de la interfaz [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) para crear un [**ID2D1BitmapBrush1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1bitmapbrush1) en lugar de un **ID2D1BitmapBrush**. **ID2D1BitmapBrush1** agrega modos de escalado de alta calidad al pincel de mapa de bits.

 

![captura de pantalla de un cuadrado relleno con un mapa de bits de planta](images/brushes-ovw-bitmap.png)

1.  Declare una variable de tipo [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).
    ```C++
        ID2D1BitmapBrush *m_pBitmapBrush;
    ```

    

2.  Cargar un mapa de bits desde un recurso. Para obtener más información, vea [Cómo cargar un mapa de bits desde un recurso](how-to-load-a-bitmap-from-a-resource.md).
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

    

3.  Elija los modos de extensión [**( \_ \_ modo de extensión de D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode)) y el modo de interpolación ([**\_ \_ \_ modo de interpolación de mapas de bits D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_bitmap_interpolation_mode)) del pincel de mapa de bits y, a continuación, llame al método [**CreateBitmapBrush**](id2d1rendertarget-createbitmapbrush.md) para crear un pincel, tal y como se muestra en el código siguiente.
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

 

 