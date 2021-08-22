---
title: Cómo crear un pincel de color sólido
description: Muestra cómo crear un pincel de color sólido mediante Direct2D.
ms.assetid: 70700b82-2294-46be-b1c0-fc89def441e2
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 395652a33f8541a825bab9f2ababcceb4b31d7c8d46458a08148e63c85b2afff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119259464"
---
# <a name="how-to-create-a-solid-color-brush"></a>Cómo crear un pincel de color sólido

Para crear un pincel de color sólido, use el método [**ID2DRenderTarget::CreateSolidColorBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) y especifique el color con el que desea pintar. Algunas de las **sobrecargas CreateSolidColorBrush** también permiten especificar la opacidad del pincel.

El código siguiente muestra cómo crear un pincel amarillo-verde sólido para rellenar un cuadrado y un pincel negro sólido para dibujar el contorno del cuadrado. El código genera la salida que se muestra en la ilustración siguiente.

![ilustración de un rectángulo relleno con un color amarillo-verde sólido](images/brushes-ovw-solidcolor.png)

1.  Declare dos [**punteros ID2D1SolidColorBrush:**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) uno para pintar negro y otro para pintar verde amarillo.
    ```C++
        ID2D1SolidColorBrush *m_pBlackBrush;
        ID2D1SolidColorBrush *m_pYellowGreenBrush;
    ```

    

2.  Llame al [**método CreateSolidColorBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) para crear los pinceles:
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

    

3.  Llame al [**método FillRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f__id2d1brush)) para pintar el interior del rectángulo con el pincel verde amarillo y el método [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) para pintar el contorno del rectángulo con el pincel negro:
    ```C++
    m_pRenderTarget->FillRectangle(&rcBrushRect, m_pYellowGreenBrush);
    m_pRenderTarget->DrawRectangle(&rcBrushRect, m_pBlackBrush, 1, NULL);
    ```

    

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de Direct2D](reference.md)
</dt> </dl>

 

 