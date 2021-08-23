---
title: Cómo crear un pincel de degradado radial
description: Muestra cómo crear un pincel de degradado radial mediante Direct2D.
ms.assetid: 663743c9-16e9-4e3a-90b2-883ef0b8d5cf
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 1932dc6506c625332d61f4e549ae2dd169060731bfbea344f64c3aa826540ae0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569275"
---
# <a name="how-to-create-a-radial-gradient-brush"></a>Cómo crear un pincel de degradado radial

Para crear un pincel de degradado radial, use el método [**ID2DRenderTarget::CreateRadialGradientBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush)) y especifique las propiedades del pincel de degradado radial y la colección de detenciones de degradado. Algunas sobrecargas permiten especificar las propiedades del pincel. En el código siguiente se muestra cómo crear un pincel de degradado radial para rellenar un círculo y un pincel negro sólido para dibujar el contorno del círculo.

El código genera la salida que se muestra en la ilustración siguiente.

![ilustración de un círculo relleno con un pincel de degradado radial](images/brushes-ovw-radials.png)

1.  Declare una variable de tipo [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush).
    ```C++
        ID2D1RadialGradientBrush *m_pRadialGradientBrush;
    ```

    

2.  Cree una matriz de estructuras [**\_ GRADIENT \_ STOP de D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop) para colocarla en la colección de detenciones de degradado. La **estructura GRADIENT \_ \_ STOP de D2D1** contiene la posición y el color de un delimitador de degradado. La posición indica la posición relativa del delimitador de degradado en el pincel. El valor está en el \[ intervalo 0.0f, 1.0f \] , como se muestra en el código siguiente.

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

    

3.  Use el [**método ID2D1RenderTarget::CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) para crear la colección [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) a partir de una matriz declarada previamente de estructuras GRADIENT STOP de [**D2D1. \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop) A continuación, use [**CreateRadialGradientBrush para**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush)) crear un pincel de degradado radial.

    > [!Note]  
    > A partir de Windows 8, puede usar el método [**ID2D1DeviceContext::CreateGradientStopCollection**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-creategradientstopcollection) para crear una colección [**ID2D1GradientStopCollection1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1gradientstopcollection1) en lugar del método [**ID2D1RenderTarget::CreateGradientStopCollection.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) Esta interfaz agrega degradados de alto color y la interpolación de degradados en colores rectas o prmultiplicados. Consulte la **página ID2DDeviceContext::CreateGradientStopCollection** para obtener más información.

     

    ```C++
    // The center of the gradient is in the center of the box.
    // The gradient origin offset was set to zero(0, 0) or center in this case.
    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateRadialGradientBrush(
            D2D1::RadialGradientBrushProperties(
                D2D1::Point2F(75, 75),
                D2D1::Point2F(0, 0),
                75,
                75),
            pGradientStops,
            &m_pRadialGradientBrush
            );
    }
    ```

    

    ```C++
    m_pRenderTarget->FillEllipse(ellipse, m_pRadialGradientBrush);
    m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 1, NULL);
    ```

    

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de Direct2D](reference.md)
</dt> </dl>

 

 