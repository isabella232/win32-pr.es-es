---
title: Representar mediante Direct2D
description: Direct2D proporciona métodos para representar texto con formato descrito por solo un IDWriteTextFormat o un IDWriteTextLayout en una superficie de Direct2D.
ms.assetid: 4acd1aee-98bf-4ca3-b4dc-b73c96c6ca63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58af17e15bcb9bd52461a2da3110982fb04e4c0a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078293"
---
# <a name="render-using-direct2d"></a><span data-ttu-id="dfce5-103">Representar mediante Direct2D</span><span class="sxs-lookup"><span data-stu-id="dfce5-103">Render Using Direct2D</span></span>

<span data-ttu-id="dfce5-104">Direct2D proporciona métodos para representar texto con formato descrito por solo un [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) o un [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) en una superficie de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="dfce5-104">Direct2D provides methods for rendering either text with formatting described by only an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) or an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) to a Direct2D surface.</span></span>

## <a name="rendering-text-described-by-idwritetextformat"></a><span data-ttu-id="dfce5-105">Representación de texto que describe IDWriteTextFormat</span><span class="sxs-lookup"><span data-stu-id="dfce5-105">Rendering Text Described by IDWriteTextFormat</span></span>

<span data-ttu-id="dfce5-106">Para representar una cadena mediante un objeto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) para describir el formato de la cadena completa, use el método [**rawtext de ID2D1RenderTarget::D**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) proporcionado por [Direct2D](../direct2d/direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="dfce5-106">To render a string using an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object to describe the formatting for the entire string, use the [**ID2D1RenderTarget::DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) method provided by [Direct2D](../direct2d/direct2d-portal.md).</span></span>

1.  <span data-ttu-id="dfce5-107">Defina el área del diseño de texto recuperando las dimensiones del área de representación y cree un rectángulo de [Direct2D](../direct2d/direct2d-portal.md) que tenga las mismas dimensiones.</span><span class="sxs-lookup"><span data-stu-id="dfce5-107">Define the area for the text layout by retrieving the dimensions of the rendering area, and create a [Direct2D](../direct2d/direct2d-portal.md) rectangle that has the same dimensions.</span></span>
    ```C++
    D2D1_RECT_F layoutRect = D2D1::RectF(
        static_cast<FLOAT>(rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.top) / dpiScaleY_,
        static_cast<FLOAT>(rc.right - rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.bottom - rc.top) / dpiScaleY_
        );
    
    ```

    

2.  <span data-ttu-id="dfce5-108">Use el método [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) y el objeto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) para representar texto en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="dfce5-108">Use the [**ID2D1RenderTarget::DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) method and the [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object to render text to the screen.</span></span> <span data-ttu-id="dfce5-109">El método **ID2D1RenderTarget::D rawtext** toma los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="dfce5-109">The **ID2D1RenderTarget::DrawText** method takes the following parameters:</span></span>
    -   <span data-ttu-id="dfce5-110">Cadena que se va a representar.</span><span class="sxs-lookup"><span data-stu-id="dfce5-110">A string to render.</span></span>
    -   <span data-ttu-id="dfce5-111">Puntero a una interfaz [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) .</span><span class="sxs-lookup"><span data-stu-id="dfce5-111">A pointer to an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface.</span></span>
    -   <span data-ttu-id="dfce5-112">Rectángulo de diseño de [Direct2D](../direct2d/direct2d-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="dfce5-112">A [Direct2D](../direct2d/direct2d-portal.md) layout rectangle.</span></span>
    -   <span data-ttu-id="dfce5-113">Puntero a una interfaz que expone [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush).</span><span class="sxs-lookup"><span data-stu-id="dfce5-113">A pointer to an interface that exposes [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush).</span></span>

    ```C++
    pRT_->DrawText(
        wszText_,        // The string to render.
        cTextLength_,    // The string's length.
        pTextFormat_,    // The text format.
        layoutRect,       // The region of the window where the text will be rendered.
        pBlackBrush_     // The brush used to draw the text.
        );
    
    ```

    

## <a name="rendering-a-idwritetext-layout-object"></a><span data-ttu-id="dfce5-114">Representar un objeto de diseño de IDWriteText</span><span class="sxs-lookup"><span data-stu-id="dfce5-114">Rendering a IDWriteText Layout Object</span></span>

<span data-ttu-id="dfce5-115">Para dibujar el texto con la configuración de diseño de texto especificada por el objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) , cambie el código del método MultiformattedText::D rawtext para usar [**IDWriteTextLayout::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout).</span><span class="sxs-lookup"><span data-stu-id="dfce5-115">To draw the text with the text layout settings specified by the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object, change the code in the MultiformattedText::DrawText method to use [**IDWriteTextLayout::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout).</span></span>

1.  <span data-ttu-id="dfce5-116">Delcare una variable de [**D2D1 \_ Point \_ 2F**](../direct2d/d2d1-point-2f.md) y establézcala en el punto superior izquierdo de la ventana.</span><span class="sxs-lookup"><span data-stu-id="dfce5-116">Delcare a [**D2D1\_POINT\_2F**](../direct2d/d2d1-point-2f.md) variable and set it to the upper-left point of the window.</span></span>
    ```C++
    D2D1_POINT_2F origin = D2D1::Point2F(
        static_cast<FLOAT>(rc.left / dpiScaleX_),
        static_cast<FLOAT>(rc.top / dpiScaleY_)
        );
    
    ```

    

2.  <span data-ttu-id="dfce5-117">Dibuje el texto en la pantalla llamando al método [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) del destino de representación de [Direct2D](../direct2d/direct2d-portal.md) y pasando el puntero [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="dfce5-117">Draw the text to the screen by calling the [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) method of the [Direct2D](../direct2d/direct2d-portal.md) render target and passing the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) pointer.</span></span>
    ```C++
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    
    ```

    

 

 