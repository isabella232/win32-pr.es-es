---
title: Cómo aplicar efectos a primitivas
description: En este tema se muestra cómo aplicar una serie de efectos a Direct2D y DirectWrite primitivos.
ms.assetid: 9782C22E-5D4C-494D-A0B1-19474C2CA900
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c17cbf1efe17d1c23c90382f3b95fb41e33946a93935b0be02fc5b41f314a8c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569600"
---
# <a name="how-to-apply-effects-to-primitives"></a>Cómo aplicar efectos a primitivas

En este tema se muestra cómo aplicar una serie de efectos a [Direct2D](./direct2d-portal.md) [y DirectWrite](direct2d-and-directwrite.md) primitivos.

Puede usar la [API de efectos de Direct2D](effects-overview.md) para aplicar gráficos de efecto a primitivos representados por [Direct2D](./direct2d-portal.md) a una imagen. El ejemplo aquí tiene dos rectángulos redondeados y el texto "Direct2D". Use Direct2D para dibujar los rectángulos [y DirectWrite](direct2d-and-directwrite.md) para dibujar el texto.

![rectángulos con el texto "direct2d" dentro de .](images/direct2d-rounded.png)

Con [los efectos de Direct2D,](effects-overview.md)puede hacer que esta imagen se parezca a la siguiente imagen. Aplique los [](composite.md) [Desenfoque gausiano](gaussian-blur.md), Iluminación [especular](specular-lighting.md)de punto, Compuesto aritmético y Compuesto a las primitivas 2D para crear la imagen aquí. [](arithmetic-composite.md)

![rectángulos con el texto "direct2d" dentro después de aplicar varios efectos.](images/direct2d-svg.png)

Después de representar los rectángulos y el texto en una superficie intermedia, puede usarlo como entrada para los objetos [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) en el gráfico de imágenes.

En este ejemplo, establezca la imagen original como entrada en el efecto [Desenfoque gausiano y, a](gaussian-blur.md) continuación, establezca la salida del desenfoque como entrada para el efecto de iluminación [especular de punto](specular-lighting.md). El resultado de este efecto se compone de la imagen original dos veces para obtener la imagen final que se representa en la ventana.

Este es un diagrama del gráfico de imágenes.

![diagrama del gráfico de efectos.](images/effect-graph.png)

Este gráfico de efectos consta de cuatro [**objetos ID2D1Effect,**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) cada uno de los que representa un efecto integrado diferente. Puede crear y conectar efectos personalizados de la misma manera, después de registrarlos mediante [**ID1D1Factory1::RegisterEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring). El código aquí crea los efectos, establece las propiedades y conecta el gráfico de efectos mostrado anteriormente.

1.  Cree el [efecto de desenfoque gaussiano](gaussian-blur.md) mediante el [**método ID2D1DeviceContext::CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) y especifique el CLSID adecuado. Los CLID para los efectos integrados se definen en d2d1effects.h. A continuación, establezca la desviación estándar del desenfoque mediante el [**método ID2D1Effect::SetValue.**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32))

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

    

    El [efecto de desenfoque gaussiano](gaussian-blur.md) desenfoca todos los canales de la imagen, incluido el canal alfa.

2.  Cree el [efecto de iluminación especular](point-specular.md) y establezca las propiedades. La posición de la luz es un vector de 3 valores de punto flotante, por lo que debe declararla como una variable independiente y pasarla al [**método SetValue.**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32))

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

    

    El [efecto de iluminación especular](point-specular.md) usa el canal alfa de la entrada para crear un mapa de altura para la iluminación.

3.  Hay dos efectos compuestos diferentes que puede usar el [efecto compuesto](composite.md) y el compuesto [aritmético](arithmetic-composite.md). Este gráfico de efectos usa ambos.

    Cree el [efecto compuesto](composite.md) y establezca el modo en D2D1 COMPOSITE MODE SOURCE IN, que genera la intersección de las imágenes de origen \_ y \_ \_ \_ destino.

    El [efecto compuesto](arithmetic-composite.md) aritmético compone las dos imágenes de entrada en función de una fórmula definida por el World Wide Web Consortium (W3C) para el estándar de gráficos vectoriales escalables (SVG). Cree un compuesto aritmético y establezca los coeficientes de la fórmula.

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

    

    Aquí se muestran los coeficientes para el [efecto compuesto](arithmetic-composite.md) aritmético.

    ```C++
    D2D1_VECTOR_4F sc_arithmeticCoefficients   = D2D1::Vector4F(0.0f, 1.0f, 1.0f, 0.0f);
    ```

    

    En este gráfico de efectos, ambos efectos compuestos toman la salida de los demás efectos y la superficie intermedia como entradas y los compone.

4.  Por último, conecte los efectos para formar el gráfico estableciendo las entradas en las imágenes y mapas de bits adecuados.

    El primer efecto, [desenfoque gaussiano,](gaussian-blur.md)recibe su entrada de la superficie intermedia en la que se representaron los primitivos. La entrada se establece mediante el [**método ID2D1Effect::SetInput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput) y se especifica el índice de [**un objeto ID2D1Image.**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) Los efectos de desenfoque gaussiano [y de iluminación especular](point-specular.md) solo tienen una entrada. El efecto de iluminación especular usa el canal alfa desenfocado del desenfoque gaussiano.

    Los [efectos compuestos](composite.md) [y aritméticos](arithmetic-composite.md) compuestos tienen varias entradas. Para asegurarse de que las imágenes se reúnen en el orden correcto, debe especificar el índice correcto para cada imagen de entrada.

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

    

5.  Pase el [objeto de](arithmetic-composite.md) efecto compuesto aritmético al [**método ID2DDeviceContext::D rawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) y procesa y dibuja la salida del gráfico.

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

    

 

 