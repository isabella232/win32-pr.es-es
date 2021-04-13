---
title: Cómo crear un pincel de degradado radial
description: Muestra cómo crear un pincel de degradado radial mediante Direct2D.
ms.assetid: 663743c9-16e9-4e3a-90b2-883ef0b8d5cf
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: fe3509a80f80132f4a5e5d65f62476be1cac61d1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104271284"
---
# <a name="how-to-create-a-radial-gradient-brush"></a><span data-ttu-id="7c437-103">Cómo crear un pincel de degradado radial</span><span class="sxs-lookup"><span data-stu-id="7c437-103">How to Create a Radial Gradient Brush</span></span>

<span data-ttu-id="7c437-104">Para crear un pincel de degradado radial, use el método [**ID2DRenderTarget:: CreateRadialGradientBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush)) y especifique las propiedades de pincel de degradado radial y la colección de delimitadores de degradado.</span><span class="sxs-lookup"><span data-stu-id="7c437-104">To create a radial gradient brush, use the [**ID2DRenderTarget::CreateRadialGradientBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush)) method and specify the radial gradient brush properties and the gradient stop collection.</span></span> <span data-ttu-id="7c437-105">Algunas sobrecargas le permiten especificar las propiedades del pincel.</span><span class="sxs-lookup"><span data-stu-id="7c437-105">Some overloads enable you to specify the brush properties.</span></span> <span data-ttu-id="7c437-106">En el código siguiente se muestra cómo crear un pincel de degradado radial para rellenar un círculo y un pincel negro sólido para dibujar el contorno del círculo.</span><span class="sxs-lookup"><span data-stu-id="7c437-106">The following code shows how to create a radial gradient brush to fill a circle, and a solid black brush to draw the outline of the circle.</span></span>

<span data-ttu-id="7c437-107">El código genera el resultado que se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="7c437-107">The code produces the output shown in the following illustration.</span></span>

![Ilustración de un círculo relleno con un pincel de degradado radial](images/brushes-ovw-radials.png)

1.  <span data-ttu-id="7c437-109">Declare una variable de tipo [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush).</span><span class="sxs-lookup"><span data-stu-id="7c437-109">Declare a variable of type [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush).</span></span>
    ```C++
        ID2D1RadialGradientBrush *m_pRadialGradientBrush;
    ```

    

2.  <span data-ttu-id="7c437-110">Cree una matriz de estructuras de [**\_ \_ detención de degradado D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop) para colocar en la colección de delimitadores de degradado.</span><span class="sxs-lookup"><span data-stu-id="7c437-110">Create an array of [**D2D1\_GRADIENT\_STOP**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop) structures to put in the gradient stop collection.</span></span> <span data-ttu-id="7c437-111">La estructura de **\_ \_ detención de degradado D2D1** contiene la posición y el color de un delimitador de degradado.</span><span class="sxs-lookup"><span data-stu-id="7c437-111">The **D2D1\_GRADIENT\_STOP** structure contains the position and color of a gradient stop.</span></span> <span data-ttu-id="7c437-112">La posición indica la posición relativa del delimitador de degradado en el pincel.</span><span class="sxs-lookup"><span data-stu-id="7c437-112">The position indicates the relative position of the gradient stop in the brush.</span></span> <span data-ttu-id="7c437-113">El valor está en el intervalo \[ 0.0 f, 1.0 f \] , tal y como se muestra en el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="7c437-113">The value is in the range \[0.0f, 1.0f\], as shown in the following code.</span></span>

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

    

3.  <span data-ttu-id="7c437-114">Use el método [**ID2D1RenderTarget:: CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) para crear la colección [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) a partir de una matriz declarada previamente de estructuras de [**\_ \_ detención de degradado de D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop) .</span><span class="sxs-lookup"><span data-stu-id="7c437-114">Use the [**ID2D1RenderTarget::CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) method to create the [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) collection from a previously declared array of [**D2D1\_GRADIENT\_STOP**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop) structures.</span></span> <span data-ttu-id="7c437-115">A continuación, use [**CreateRadialGradientBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush)) para crear un pincel de degradado radial.</span><span class="sxs-lookup"><span data-stu-id="7c437-115">Then, Use the [**CreateRadialGradientBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush)) to create a radial gradient brush.</span></span>

    > [!Note]  
    > <span data-ttu-id="7c437-116">A partir de Windows 8, puede usar el método [**ID2D1DeviceContext:: CreateGradientStopCollection**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-creategradientstopcollection) para crear una colección [**ID2D1GradientStopCollection1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1gradientstopcollection1) en lugar del método [**ID2D1RenderTarget:: CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) .</span><span class="sxs-lookup"><span data-stu-id="7c437-116">Starting with Windows 8, you can use the [**ID2D1DeviceContext::CreateGradientStopCollection**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-creategradientstopcollection) method to create a [**ID2D1GradientStopCollection1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1gradientstopcollection1) collection instead of the [**ID2D1RenderTarget::CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) method.</span></span> <span data-ttu-id="7c437-117">Esta interfaz agrega degradados de alto color y la interpolación de degradados en colores rectos o prmultiplied.</span><span class="sxs-lookup"><span data-stu-id="7c437-117">This interface adds high-color gradients and the interpolation of gradients in either straight or prmultiplied colors.</span></span> <span data-ttu-id="7c437-118">Vea la página **ID2DDeviceContext:: CreateGradientStopCollection** para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="7c437-118">See the **ID2DDeviceContext::CreateGradientStopCollection** page for more information.</span></span>

     

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

    

## <a name="related-topics"></a><span data-ttu-id="7c437-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7c437-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c437-120">Referencia de Direct2D</span><span class="sxs-lookup"><span data-stu-id="7c437-120">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 