---
title: Cómo crear un pincel de color sólido
description: Muestra cómo crear un pincel de color sólido mediante Direct2D.
ms.assetid: 70700b82-2294-46be-b1c0-fc89def441e2
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: bc6fbf5df42386f5e0e5a843a1906d36d4fc8c71
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995337"
---
# <a name="how-to-create-a-solid-color-brush"></a><span data-ttu-id="76b0f-103">Cómo crear un pincel de color sólido</span><span class="sxs-lookup"><span data-stu-id="76b0f-103">How to Create a Solid Color Brush</span></span>

<span data-ttu-id="76b0f-104">Para crear un pincel de color sólido, use el método [**ID2DRenderTarget:: CreateSolidColorBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) y especifique el color con el que desea pintar.</span><span class="sxs-lookup"><span data-stu-id="76b0f-104">To create a solid color brush, use the [**ID2DRenderTarget::CreateSolidColorBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) method and specify the color with which you want to paint.</span></span> <span data-ttu-id="76b0f-105">Algunas de las sobrecargas de **CreateSolidColorBrush** también permiten especificar la opacidad del pincel.</span><span class="sxs-lookup"><span data-stu-id="76b0f-105">Some of the **CreateSolidColorBrush** overloads also enable you to specify the opacity of the brush.</span></span>

<span data-ttu-id="76b0f-106">En el código siguiente se muestra cómo crear un pincel sólido amarillo-verde para rellenar un cuadrado y un pincel negro sólido para dibujar el contorno del cuadrado.</span><span class="sxs-lookup"><span data-stu-id="76b0f-106">The following code shows how to create a solid yellow-green brush to fill a square, and a solid black brush to draw the outline of the square.</span></span> <span data-ttu-id="76b0f-107">El código genera el resultado que se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="76b0f-107">The code produces the output shown in the following illustration.</span></span>

![Ilustración de un rectángulo relleno con un color amarillo amarillo opaco](images/brushes-ovw-solidcolor.png)

1.  <span data-ttu-id="76b0f-109">Declare dos punteros [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) : uno para pintar negro y otro para pintar amarillo amarillo.</span><span class="sxs-lookup"><span data-stu-id="76b0f-109">Declare two [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) pointers: one for painting black and one for painting yellow green.</span></span>
    ```C++
        ID2D1SolidColorBrush *m_pBlackBrush;
        ID2D1SolidColorBrush *m_pYellowGreenBrush;
    ```

    

2.  <span data-ttu-id="76b0f-110">Llame al método [**CreateSolidColorBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) para crear los pinceles:</span><span class="sxs-lookup"><span data-stu-id="76b0f-110">Call the [**CreateSolidColorBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) method to create the brushes:</span></span>
    ```C++
    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateSolidColorBrush(
            D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
            &m_pBlackBrush
            );
    }

    // Create a solid color brush with its rgb value 0x9ACD32.
    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateSolidColorBrush(
            D2D1::ColorF(D2D1::ColorF(0x9ACD32, 1.0f)),  
            &m_pYellowGreenBrush
            );
    }
    ```

    

3.  <span data-ttu-id="76b0f-111">Llame al método [**FillRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f__id2d1brush)) para pintar el interior del rectángulo con el pincel verde amarillo y el método [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) para pintar el contorno del rectángulo con el pincel negro:</span><span class="sxs-lookup"><span data-stu-id="76b0f-111">Call the [**FillRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f__id2d1brush)) method to paint the interior of the rectangle with the yellow green brush and the [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) method to paint the outline of the rectangle with the black brush:</span></span>
    ```C++
    m_pRenderTarget->FillRectangle(&rcBrushRect, m_pYellowGreenBrush);
    m_pRenderTarget->DrawRectangle(&rcBrushRect, m_pBlackBrush, 1, NULL);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="76b0f-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="76b0f-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76b0f-113">Referencia de Direct2D</span><span class="sxs-lookup"><span data-stu-id="76b0f-113">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 