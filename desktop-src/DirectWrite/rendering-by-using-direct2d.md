---
title: Representación mediante Direct2D
description: Direct2D proporciona métodos para representar texto con formato descrito solo por un IDWriteTextFormat o un IDWriteTextLayout en una superficie de Direct2D.
ms.assetid: 4acd1aee-98bf-4ca3-b4dc-b73c96c6ca63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ad297a8fdf2078c966989baf5e81c69cf515427340f8de8d073035fcf98f434
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048485"
---
# <a name="render-using-direct2d"></a>Representación mediante Direct2D

Direct2D proporciona métodos para representar texto con formato descrito solo por [**un IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) o [**un IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) en una superficie de Direct2D.

## <a name="rendering-text-described-by-idwritetextformat"></a>Representación de texto descrito por IDWriteTextFormat

Para representar una cadena mediante un objeto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) para describir el formato de toda la cadena, use el método [**ID2D1RenderTarget::D rawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) proporcionado por [Direct2D.](../direct2d/direct2d-portal.md)

1.  Para definir el área del diseño de texto, recupere las dimensiones del área de representación y cree un rectángulo [de Direct2D](../direct2d/direct2d-portal.md) que tenga las mismas dimensiones.
    ```C++
    D2D1_RECT_F layoutRect = D2D1::RectF(
        static_cast<FLOAT>(rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.top) / dpiScaleY_,
        static_cast<FLOAT>(rc.right - rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.bottom - rc.top) / dpiScaleY_
        );
    
    ```

    

2.  Use el [**método ID2D1RenderTarget::D rawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) y el objeto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) para representar texto en la pantalla. El **método ID2D1RenderTarget::D rawText** toma los parámetros siguientes:
    -   Cadena que se representará.
    -   Puntero a una [**interfaz IDWriteTextFormat.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)
    -   Rectángulo [de diseño de Direct2D.](../direct2d/direct2d-portal.md)
    -   Puntero a una interfaz que expone [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush).

    ```C++
    pRT_->DrawText(
        wszText_,        // The string to render.
        cTextLength_,    // The string's length.
        pTextFormat_,    // The text format.
        layoutRect,       // The region of the window where the text will be rendered.
        pBlackBrush_     // The brush used to draw the text.
        );
    
    ```

    

## <a name="rendering-a-idwritetext-layout-object"></a>Representación de un objeto de diseño IDWriteText

Para dibujar el texto con la configuración de diseño de texto especificada por el objeto [**IDWriteTextLayout,**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) cambie el código del método MultiformattedText::D rawText para usar [**IDWriteTextLayout::D rawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout).

1.  Delcare a [**D2D1 \_ POINT \_ 2F**](../direct2d/d2d1-point-2f.md) variable and set it to the upper-left point of the window.
    ```C++
    D2D1_POINT_2F origin = D2D1::Point2F(
        static_cast<FLOAT>(rc.left / dpiScaleX_),
        static_cast<FLOAT>(rc.top / dpiScaleY_)
        );
    
    ```

    

2.  Dibuje el texto en la pantalla llamando al método [**ID2D1RenderTarget::D rawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) del destino de representación de [Direct2D](../direct2d/direct2d-portal.md) y pasando el puntero [**IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
    ```C++
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    
    ```

    

 

 