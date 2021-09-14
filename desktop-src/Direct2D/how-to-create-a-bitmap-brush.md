---
title: Cómo crear un pincel de mapa de bits
description: Muestra cómo crear un pincel de mapa de bits mediante Direct2D.
ms.assetid: 8f78b30a-7507-4dd8-b6f4-12d88e3c9a1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd8f28735368916d1abd0c1c9aa091dec4fd93f4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127163182"
---
# <a name="how-to-create-a-bitmap-brush"></a>Cómo crear un pincel de mapa de bits

Para crear un pincel de mapa de bits, use el [**método ID2D1RenderTarget::CreateBitmapBrush**](id2d1rendertarget-createbitmapbrush.md) y especifique las propiedades del pincel de mapa de bits. Algunas sobrecargas permiten especificar las propiedades del pincel. El código siguiente muestra cómo crear un pincel de mapa de bits para rellenar un cuadrado y un pincel negro sólido para dibujar el contorno del cuadrado. El código genera la salida que se muestra en la siguiente captura de pantalla.

> [!Note]  
> A partir Windows 8, puede usar el método [**CreateBitmapBrush**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapbrush(id2d1bitmap_constd2d1_bitmap_brush_properties1_constd2d1_brush_properties_id2d1bitmapbrush1)) en la interfaz [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) para crear un [**id2D1BitmapBrush1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1bitmapbrush1) en lugar de un **objeto ID2D1BitmapBrush.** **ID2D1BitmapBrush1** agrega modos de escalado de alta calidad al pincel de mapa de bits.

 

![captura de pantalla de un cuadrado rellenado con un mapa de bits de la planta](images/brushes-ovw-bitmap.png)

1.  Declare una variable de tipo [**ID2D1BitmapBrush.**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)
    ```C++
        ID2D1BitmapBrush *m_pBitmapBrush;
    ```

    

2.  Carga de un mapa de bits desde un recurso. Para obtener más información, [vea How to Load a Bitmap from a Resource](how-to-load-a-bitmap-from-a-resource.md).
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

    

3.  Elija los modos de extensión ([**D2D1 \_ EXTEND \_ MODE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode)) y el modo de interpolación ([**D2D1 \_ BITMAP \_ INTERPOLATION \_ MODE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_bitmap_interpolation_mode)) del pincel de mapa de bits y, a continuación, llame al método [**CreateBitmapBrush**](id2d1rendertarget-createbitmapbrush.md) para crear un pincel, como se muestra en el código siguiente.
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

 

 