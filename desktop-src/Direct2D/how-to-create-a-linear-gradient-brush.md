---
title: Cómo crear un pincel de degradado lineal
description: Muestra cómo crear un pincel de degradado lineal mediante Direct2D.
ms.assetid: 3cf5acc6-2f17-49d4-aca5-a84a846d1749
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 0c9223eb561ecc391014bc4a89c86a634181bec6d1e3917866aeef2723f1510a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119259544"
---
# <a name="how-to-create-a-linear-gradient-brush"></a>Cómo crear un pincel de degradado lineal

Para crear un pincel de degradado lineal, use el [**método CreateLinearGradientBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) y especifique las propiedades del pincel de degradado lineal y la colección de detenciones de degradado. Algunas sobrecargas permiten especificar las propiedades del pincel. En el código siguiente se muestra cómo crear un pincel de degradado lineal para rellenar un cuadrado y un pincel negro sólido para dibujar el contorno del cuadrado.

El código genera la salida que se muestra en la ilustración siguiente.

![ilustración de un cuadrado relleno con un pincel de degradado lineal](images/brushes-ovw-lineargradient.png)

1.  Declare una variable de tipo [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).
    ```C++
        ID2D1LinearGradientBrush *m_pLinearGradientBrush;
    ```

    

2.  Use el método [**ID2D1RenderTarget::CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_id2d1gradientstopcollection)) para crear la colección [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) con una matriz declarada de estructuras GRADIENT STOP de [**D2D1, \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop) como se muestra en el código siguiente.
    > [!Note]  
    > A partir Windows 8, puede usar el método [**ID2D1DeviceContext::CreateGradientStopCollection**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-creategradientstopcollection) para crear una [**colección ID2D1GradientStopCollection1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1gradientstopcollection1) en su lugar. Esta interfaz agrega degradados de alto color y la interpolación de degradados en colores rectas o prmultiplicados. Consulte la **página ID2DDeviceContext::CreateGradientStopCollection** para obtener más información.

     

    ```C++
    // Create an array of gradient stops to put in the gradient stop
    // collection that will be used in the gradient brush.
    ID2D1GradientStopCollection *pGradientStops = NULL;

    D2D1_GRADIENT_STOP gradientStops[2];
    gradientStops[0].color = D2D1::ColorF(D2D1::ColorF::Yellow, 1);
    gradientStops[0].position = 0.0f;
    gradientStops[1].color = D2D1::ColorF(D2D1::ColorF::ForestGreen, 1);
    gradientStops[1].position = 1.0f;
    // Create the ID2D1GradientStopCollection from a previously
    // declared array of D2D1_GRADIENT_STOP structs.
    hr = m_pRenderTarget->CreateGradientStopCollection(
        gradientStops,
        2,
        D2D1_GAMMA_2_2,
        D2D1_EXTEND_MODE_CLAMP,
        &pGradientStops
        );
    ```

    

3.  Use [**ID2D1RenderTarget::CreateLinearGradientBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) para crear un pincel de degradado lineal, rellenar el cuadrado con el pincel y dibujar el cuadrado con el pincel de color negro.
    ```C++
    // The line that determines the direction of the gradient starts at
    // the upper-left corner of the square and ends at the lower-right corner.

    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateLinearGradientBrush(
            D2D1::LinearGradientBrushProperties(
                D2D1::Point2F(0, 0),
                D2D1::Point2F(150, 150)),
            pGradientStops,
            &m_pLinearGradientBrush
            );
    }
    ```

    

    ```C++
    m_pRenderTarget->FillRectangle(&rcBrushRect, m_pLinearGradientBrush);
    m_pRenderTarget->DrawRectangle(&rcBrushRect, m_pBlackBrush, 1, NULL);
    ```

    

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de Direct2D](reference.md)
</dt> </dl>

 

 
