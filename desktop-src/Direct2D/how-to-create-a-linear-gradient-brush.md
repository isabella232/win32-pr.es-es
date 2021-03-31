---
title: Cómo crear un pincel de degradado lineal
description: Muestra cómo crear un pincel de degradado lineal mediante Direct2D.
ms.assetid: 3cf5acc6-2f17-49d4-aca5-a84a846d1749
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 3a50a6e3ab421e2275644051ed647d5c4501f8e0
ms.sourcegitcommit: 015fb35e736a235d3c9becff1f6832a0965b4303
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "103904970"
---
# <a name="how-to-create-a-linear-gradient-brush"></a><span data-ttu-id="c8c5a-103">Cómo crear un pincel de degradado lineal</span><span class="sxs-lookup"><span data-stu-id="c8c5a-103">How to Create a Linear Gradient Brush</span></span>

<span data-ttu-id="c8c5a-104">Para crear un pincel de degradado lineal, use el método [**CreateLinearGradientBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) y especifique las propiedades de pincel de degradado lineal y la colección de delimitadores de degradado.</span><span class="sxs-lookup"><span data-stu-id="c8c5a-104">To create a linear gradient brush, use the [**CreateLinearGradientBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) method and specify the linear gradient brush properties and the gradient stop collection.</span></span> <span data-ttu-id="c8c5a-105">Algunas sobrecargas le permiten especificar las propiedades del pincel.</span><span class="sxs-lookup"><span data-stu-id="c8c5a-105">Some overloads enable you to specify the brush properties.</span></span> <span data-ttu-id="c8c5a-106">En el código siguiente se muestra cómo crear un pincel de degradado lineal para rellenar un cuadrado y un pincel negro sólido para dibujar el contorno del cuadrado.</span><span class="sxs-lookup"><span data-stu-id="c8c5a-106">The following code shows how to create a linear gradient brush to fill a square, and a solid black brush to draw the outline of the square.</span></span>

<span data-ttu-id="c8c5a-107">El código genera el resultado que se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="c8c5a-107">The code produces the output shown in the following illustration.</span></span>

![Ilustración de un cuadrado relleno con un pincel de degradado lineal](images/brushes-ovw-lineargradient.png)

1.  <span data-ttu-id="c8c5a-109">Declare una variable de tipo [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).</span><span class="sxs-lookup"><span data-stu-id="c8c5a-109">Declare a variable of type [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).</span></span>
    ```C++
        ID2D1LinearGradientBrush *m_pLinearGradientBrush;
    ```

    

2.  <span data-ttu-id="c8c5a-110">Use el método [**ID2D1RenderTarget:: CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_id2d1gradientstopcollection)) para crear la colección [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) con una matriz declarada de estructuras de [**\_ \_ detención de degradado de D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop) , como se muestra en el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="c8c5a-110">Use the [**ID2D1RenderTarget::CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_id2d1gradientstopcollection)) method to create the [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) collection with a declared array of [**D2D1\_GRADIENT\_STOP**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop) structures, as shown in the following code.</span></span>
    > [!Note]  
    > <span data-ttu-id="c8c5a-111">A partir de Windows 8, puede usar el método [**ID2D1DeviceContext:: CreateGradientStopCollection**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-creategradientstopcollection) para crear una colección [**ID2D1GradientStopCollection1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1gradientstopcollection1) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="c8c5a-111">Starting with Windows 8, you can use the [**ID2D1DeviceContext::CreateGradientStopCollection**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-creategradientstopcollection) method to create a [**ID2D1GradientStopCollection1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1gradientstopcollection1) collection instead.</span></span> <span data-ttu-id="c8c5a-112">Esta interfaz agrega degradados de alto color y la interpolación de degradados en colores rectos o prmultiplied.</span><span class="sxs-lookup"><span data-stu-id="c8c5a-112">This interface adds high-color gradients and the interpolation of gradients in either straight or prmultiplied colors.</span></span> <span data-ttu-id="c8c5a-113">Vea la página **ID2DDeviceContext:: CreateGradientStopCollection** para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="c8c5a-113">See the **ID2DDeviceContext::CreateGradientStopCollection** page for more information.</span></span>

     

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

    

3.  <span data-ttu-id="c8c5a-114">Use [**ID2D1RenderTarget:: CreateLinearGradientBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) para crear un pincel de degradado lineal, rellene el cuadrado con el pincel y dibuje el cuadrado con el pincel de color negro.</span><span class="sxs-lookup"><span data-stu-id="c8c5a-114">Use the [**ID2D1RenderTarget::CreateLinearGradientBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) to create a linear gradient brush, fill the square with the brush, and draw the square with the black color brush.</span></span>
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

    

## <a name="related-topics"></a><span data-ttu-id="c8c5a-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c8c5a-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8c5a-116">Referencia de Direct2D</span><span class="sxs-lookup"><span data-stu-id="c8c5a-116">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 
