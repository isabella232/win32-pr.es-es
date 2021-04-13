---
title: Cómo aplicar efectos a primitivos
description: En este tema se muestra cómo aplicar una serie de efectos a los primitivos de Direct2D y de DirectWrite.
ms.assetid: 9782C22E-5D4C-494D-A0B1-19474C2CA900
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aafb171c20c567d1fbd6385d23cc3b2925efc154
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421133"
---
# <a name="how-to-apply-effects-to-primitives"></a><span data-ttu-id="2f710-103">Cómo aplicar efectos a primitivos</span><span class="sxs-lookup"><span data-stu-id="2f710-103">How to Apply Effects to Primitives</span></span>

<span data-ttu-id="2f710-104">En este tema se muestra cómo aplicar una serie de efectos a los primitivos de [Direct2D](./direct2d-portal.md) y de [DirectWrite](direct2d-and-directwrite.md) .</span><span class="sxs-lookup"><span data-stu-id="2f710-104">This topic shows how to apply a series of effect to [Direct2D](./direct2d-portal.md) and [DirectWrite](direct2d-and-directwrite.md) primitives.</span></span>

<span data-ttu-id="2f710-105">Puede usar la [API de efectos de direct2d](effects-overview.md) para aplicar gráficos de efectos a primitivas representadas por [Direct2D](./direct2d-portal.md) a una imagen.</span><span class="sxs-lookup"><span data-stu-id="2f710-105">You can use the [Direct2D effects API](effects-overview.md) to apply effect graphs to primitives rendered by [Direct2D](./direct2d-portal.md) to an image.</span></span> <span data-ttu-id="2f710-106">El ejemplo siguiente tiene dos rectángulos redondeados y el texto "Direct2D".</span><span class="sxs-lookup"><span data-stu-id="2f710-106">The example here has two rounded rectangles and the text "Direct2D".</span></span> <span data-ttu-id="2f710-107">Use Direct2D para dibujar los rectángulos y [DirectWrite](direct2d-and-directwrite.md) para dibujar el texto.</span><span class="sxs-lookup"><span data-stu-id="2f710-107">Use Direct2D to draw the rectangles and [DirectWrite](direct2d-and-directwrite.md) to draw the text.</span></span>

![rectángulos con el texto "direct2d" dentro de.](images/direct2d-rounded.png)

<span data-ttu-id="2f710-109">Con los [efectos de Direct2D](effects-overview.md), puede hacer que esta imagen tenga el aspecto de la siguiente imagen.</span><span class="sxs-lookup"><span data-stu-id="2f710-109">Using [Direct2D effects](effects-overview.md), you can make this image look like the next image.</span></span> <span data-ttu-id="2f710-110">Aplique el [desenfoque gausiano](gaussian-blur.md), [iluminación especular de punto](specular-lighting.md), [compuesto aritmético](arithmetic-composite.md)y efectos [compuestos](composite.md) a los primitivos 2D para crear la imagen aquí.</span><span class="sxs-lookup"><span data-stu-id="2f710-110">Apply the [Gaussian Blur](gaussian-blur.md), [Point Specular Lighting](specular-lighting.md), [Arithmetic Composite](arithmetic-composite.md), and [Composite](composite.md) effects to the 2D primitives to create the image here.</span></span>

![se aplican rectángulos con el texto "direct2d" dentro de unos pocos efectos.](images/direct2d-svg.png)

<span data-ttu-id="2f710-112">Después de representar los rectángulos y el texto en una superficie intermedia, puede usarlo como entrada para los objetos [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) en el gráfico de imagen.</span><span class="sxs-lookup"><span data-stu-id="2f710-112">After you render the rectangles and text to a intermediate surface, you can use this as input for [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) objects in the image graph.</span></span>

<span data-ttu-id="2f710-113">En este ejemplo, establezca la imagen original como la entrada del [efecto de desenfoque gausiano](gaussian-blur.md) y, a continuación, establezca la salida del desenfoque como entrada para el [efecto de iluminación especular de punto](specular-lighting.md).</span><span class="sxs-lookup"><span data-stu-id="2f710-113">In this example, set the original image as the input to the [Gaussian Blur effect](gaussian-blur.md) and then set the output of the blur as the input for the [Point Specular Lighting effect](specular-lighting.md).</span></span> <span data-ttu-id="2f710-114">El resultado de este efecto se compone dos veces con la imagen original para obtener la imagen final que se representa en la ventana.</span><span class="sxs-lookup"><span data-stu-id="2f710-114">The result of this effect is then composited with the original image twice to get the final image that is rendered to the window.</span></span>

<span data-ttu-id="2f710-115">Este es un diagrama del gráfico de imágenes.</span><span class="sxs-lookup"><span data-stu-id="2f710-115">Here is a diagram of the image graph.</span></span>

![diagrama del gráfico de efectos.](images/effect-graph.png)

<span data-ttu-id="2f710-117">Este gráfico de efectos consta de cuatro objetos [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) , cada uno de los cuales representa un efecto integrado diferente.</span><span class="sxs-lookup"><span data-stu-id="2f710-117">This effect graph consists of four [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) objects, each representing a different built-in effect.</span></span> <span data-ttu-id="2f710-118">Puede crear y conectar efectos personalizados de la misma manera, después de registrarlos mediante [**ID1D1Factory1:: RegisterEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring).</span><span class="sxs-lookup"><span data-stu-id="2f710-118">You can create and connect custom effects in the same way, after you register them using [**ID1D1Factory1::RegisterEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring).</span></span> <span data-ttu-id="2f710-119">Aquí el código crea los efectos, establece las propiedades y conecta el gráfico de efectos mostrado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="2f710-119">The code here creates the effects, sets the properties, and connects the effect graph shown earlier.</span></span>

1.  <span data-ttu-id="2f710-120">Cree el efecto [Desenfoque gaussiano](gaussian-blur.md) mediante el método [**ID2D1DeviceContext:: CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) y especifique el CLSID adecuado.</span><span class="sxs-lookup"><span data-stu-id="2f710-120">Create the [Gaussian blur](gaussian-blur.md) effect using the [**ID2D1DeviceContext::CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) method and specifying the proper CLSID.</span></span> <span data-ttu-id="2f710-121">Los CLSID de los efectos integrados se definen en d2d1effects. h.</span><span class="sxs-lookup"><span data-stu-id="2f710-121">The CLSIDs for the built-in effects are defined in d2d1effects.h.</span></span> <span data-ttu-id="2f710-122">A continuación, establezca la desviación estándar del desenfoque mediante el método [**ID2D1Effect:: SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) .</span><span class="sxs-lookup"><span data-stu-id="2f710-122">You then set the standard deviation of the blur using the [**ID2D1Effect::SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) method.</span></span>

    ```C++
    // Create the Gaussian Blur Effect
    DX::ThrowIfFailed(
        m_d2dContext->CreateEffect(CLSID_D2D1GaussianBlur, &gaussianBlurEffect)
        );

    // Set the blur amount
    DX::ThrowIfFailed(
        gaussianBlurEffect->SetValue(D2D1_GAUSSIANBLUR_PROP_STANDARD_DEVIATION, sc_gaussianBlurStDev)
        );
    ```

    

    <span data-ttu-id="2f710-123">El efecto [Desenfoque gaussiano](gaussian-blur.md) desenfoca todos los canales de la imagen, incluido el canal alfa.</span><span class="sxs-lookup"><span data-stu-id="2f710-123">The [Gaussian blur](gaussian-blur.md) effect blurs all of the channels of the image, including the alpha channel.</span></span>

2.  <span data-ttu-id="2f710-124">Cree el efecto de [iluminación especular](point-specular.md) y establezca las propiedades.</span><span class="sxs-lookup"><span data-stu-id="2f710-124">Create the [specular lighting](point-specular.md) effect and set the properties.</span></span> <span data-ttu-id="2f710-125">La posición de la luz es un vector de 3 valores de punto flotante, por lo que debe declararlo como una variable independiente y pasarlo al método [**SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) .</span><span class="sxs-lookup"><span data-stu-id="2f710-125">The position of the light is a vector of 3 floating point values, so you must declare it as a separate variable and pass it to the [**SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) method.</span></span>

    ```C++
    // Create the Specular Lighting Effect
    DX::ThrowIfFailed(
        m_d2dContext->CreateEffect(CLSID_D2D1PointSpecular, &specularLightingEffect)
        );

    DX::ThrowIfFailed(
        specularLightingEffect->SetValue(D2D1_POINTSPECULAR_PROP_LIGHT_POSITION, sc_specularLightPosition)
        );

    DX::ThrowIfFailed(
        specularLightingEffect->SetValue(D2D1_POINTSPECULAR_PROP_SPECULAR_EXPONENT, sc_specularExponent)
        );

    DX::ThrowIfFailed(
        specularLightingEffect->SetValue(D2D1_POINTSPECULAR_PROP_SURFACE_SCALE, sc_specularSurfaceScale)
        );

    DX::ThrowIfFailed(
        specularLightingEffect->SetValue(D2D1_POINTSPECULAR_PROP_SPECULAR_CONSTANT, sc_specularConstant)
        );
    ```

    

    <span data-ttu-id="2f710-126">El efecto de [luz especular](point-specular.md) usa el canal alfa de la entrada para crear un mapa de alto para la iluminación.</span><span class="sxs-lookup"><span data-stu-id="2f710-126">The [specular lighting](point-specular.md) effect uses the alpha channel of the input to create a height map for the lighting.</span></span>

3.  <span data-ttu-id="2f710-127">Hay dos efectos compuestos diferentes en los que puede usar el efecto [compuesto](composite.md) y el [compuesto aritmético](arithmetic-composite.md).</span><span class="sxs-lookup"><span data-stu-id="2f710-127">There are two different composite effects that you can use the [composite](composite.md) effect and the [arithmetic composite](arithmetic-composite.md).</span></span> <span data-ttu-id="2f710-128">Este gráfico de efectos usa ambos.</span><span class="sxs-lookup"><span data-stu-id="2f710-128">This effect graph uses both.</span></span>

    <span data-ttu-id="2f710-129">Cree el efecto [compuesto](composite.md) y establezca el modo en el \_ origen del modo compuesto D2D1 \_ \_ \_ en, que genera la intersección de las imágenes de origen y de destino.</span><span class="sxs-lookup"><span data-stu-id="2f710-129">Create the [composite](composite.md) effect and set the mode to D2D1\_COMPOSITE\_MODE\_SOURCE\_IN, which outputs the intersection of the source and destination images.</span></span>

    <span data-ttu-id="2f710-130">El efecto [compuesto aritmético](arithmetic-composite.md) compone las dos imágenes de entrada en función de una fórmula definida por el World Wide Web Consortium (W3C) para el estándar de gráficos vectoriales escalables (SVG).</span><span class="sxs-lookup"><span data-stu-id="2f710-130">The [arithmetic composite](arithmetic-composite.md) effect composes the two input images based on a formula defined by the World Wide Web Consortium (W3C) for the Scalable Vector Graphics (SVG) standard.</span></span> <span data-ttu-id="2f710-131">Cree un compuesto aritmético y establezca los coeficientes para la fórmula.</span><span class="sxs-lookup"><span data-stu-id="2f710-131">Create arithmetic composite and set the coefficients for the formula.</span></span>

    ```C++
    // Create the Composite Effects
    DX::ThrowIfFailed(
        m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect)
        );

    DX::ThrowIfFailed(
        compositeEffect->SetValue(D2D1_COMPOSITE_PROP_MODE, D2D1_COMPOSITE_MODE_SOURCE_IN)
        );

    DX::ThrowIfFailed(
        m_d2dContext->CreateEffect(CLSID_D2D1ArithmeticComposite, &m_arithmeticCompositeEffect)
        );

    DX::ThrowIfFailed(
        m_arithmeticCompositeEffect->SetValue(D2D1_ARITHMETICCOMPOSITE_PROP_COEFFICIENTS, sc_arithmeticCoefficients)
        );
    ```

    

    <span data-ttu-id="2f710-132">Aquí se muestran los coeficientes para el efecto [compuesto aritmético](arithmetic-composite.md) .</span><span class="sxs-lookup"><span data-stu-id="2f710-132">The coefficients for the [arithmetic composite](arithmetic-composite.md) effect are shown here.</span></span>

    ```C++
    D2D1_VECTOR_4F sc_arithmeticCoefficients   = D2D1::Vector4F(0.0f, 1.0f, 1.0f, 0.0f);
    ```

    

    <span data-ttu-id="2f710-133">En este gráfico de efectos, los dos efectos compuestos toman la salida de los demás efectos y la superficie intermedia como entradas y los compone.</span><span class="sxs-lookup"><span data-stu-id="2f710-133">In this effect graph, both of the composite effects take the output of the other effects and the intermediate surface as inputs and composites them.</span></span>

4.  <span data-ttu-id="2f710-134">Por último, conecte los efectos para formar el gráfico estableciendo las entradas en las imágenes y los mapas de bits adecuados.</span><span class="sxs-lookup"><span data-stu-id="2f710-134">Finally, you connect the effects to form the graph by setting the inputs to the proper images and bitmaps.</span></span>

    <span data-ttu-id="2f710-135">El primer efecto, [Desenfoque gaussiano](gaussian-blur.md), recibe su entrada de la superficie intermedia a la que representaba los primitivos.</span><span class="sxs-lookup"><span data-stu-id="2f710-135">The first effect, [Gaussian blur](gaussian-blur.md), receives its input from the intermediate surface that you rendered the primitives to.</span></span> <span data-ttu-id="2f710-136">La entrada se establece mediante el método [**ID2D1Effect:: SetInput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput) y se especifica el índice de un objeto [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) .</span><span class="sxs-lookup"><span data-stu-id="2f710-136">You set the input using the [**ID2D1Effect::SetInput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput) method and specifying the index of an [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) object.</span></span> <span data-ttu-id="2f710-137">Los efectos de desenfoque gaussiano y de [iluminación especular](point-specular.md) tienen una sola entrada.</span><span class="sxs-lookup"><span data-stu-id="2f710-137">The Gaussian blur and [specular lighting](point-specular.md) effects have only a single input.</span></span> <span data-ttu-id="2f710-138">El efecto de iluminación especular usa el canal alfa borroso del desenfoque gaussiano</span><span class="sxs-lookup"><span data-stu-id="2f710-138">The specular lighting effect uses the blurred alpha channel of the Gaussian blur</span></span>

    <span data-ttu-id="2f710-139">Los efectos compuestos [compuestos](composite.md) y [aritméticos](arithmetic-composite.md) tienen varias entradas.</span><span class="sxs-lookup"><span data-stu-id="2f710-139">The [composite](composite.md) and [arithmetic composite](arithmetic-composite.md) effects have multiple inputs.</span></span> <span data-ttu-id="2f710-140">Para asegurarse de que las imágenes se colocan en el orden correcto, debe especificar el índice correcto para cada imagen de entrada.</span><span class="sxs-lookup"><span data-stu-id="2f710-140">To make sure the images are put together in the right order, you must specify the correct index for each input image.</span></span>

    ```C++
    // Connect the graph.
    // Apply a blur effect to the original image.
    gaussianBlurEffect->SetInput(0, m_inputImage.Get());

    // Apply a specular lighting effect to the result.
    specularLightingEffect->SetInputEffect(0, gaussianBlurEffect.Get());

    // Compose the original bitmap under the output from lighting and blur.
    compositeEffect->SetInput(0, m_inputImage.Get());
    compositeEffect->SetInputEffect(1, specularLightingEffect.Get());

    // Compose the original bitmap under the output from lighting and blur.
    m_arithmeticCompositeEffect->SetInput(0, m_inputImage.Get());
    m_arithmeticCompositeEffect->SetInputEffect(1, compositeEffect.Get());
    ```

    

5.  <span data-ttu-id="2f710-141">Pase el objeto de efecto [compuesto aritmético](arithmetic-composite.md) al método [**ID2DDeviceContext::D rawimage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) y procese y dibuje el resultado del gráfico.</span><span class="sxs-lookup"><span data-stu-id="2f710-141">Pass the [arithmetic composite](arithmetic-composite.md) effect object into the [**ID2DDeviceContext::DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) method and it processes and draws the output of the graph.</span></span>

    ```C++
        // Draw the output of the effects graph.
        m_d2dContext->DrawImage(
            m_arithmeticCompositeEffect.Get(),
            D2D1::Point2F(
                (size.width - sc_inputBitmapSize.width) / 2,
                (size.height - sc_inputBitmapSize.height) / 2 + sc_offset
                )
            );
    ```

    

 

 