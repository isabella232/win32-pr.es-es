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
# <a name="how-to-apply-effects-to-primitives"></a>Cómo aplicar efectos a primitivos

En este tema se muestra cómo aplicar una serie de efectos a los primitivos de [Direct2D](./direct2d-portal.md) y de [DirectWrite](direct2d-and-directwrite.md) .

Puede usar la [API de efectos de direct2d](effects-overview.md) para aplicar gráficos de efectos a primitivas representadas por [Direct2D](./direct2d-portal.md) a una imagen. El ejemplo siguiente tiene dos rectángulos redondeados y el texto "Direct2D". Use Direct2D para dibujar los rectángulos y [DirectWrite](direct2d-and-directwrite.md) para dibujar el texto.

![rectángulos con el texto "direct2d" dentro de.](images/direct2d-rounded.png)

Con los [efectos de Direct2D](effects-overview.md), puede hacer que esta imagen tenga el aspecto de la siguiente imagen. Aplique el [desenfoque gausiano](gaussian-blur.md), [iluminación especular de punto](specular-lighting.md), [compuesto aritmético](arithmetic-composite.md)y efectos [compuestos](composite.md) a los primitivos 2D para crear la imagen aquí.

![se aplican rectángulos con el texto "direct2d" dentro de unos pocos efectos.](images/direct2d-svg.png)

Después de representar los rectángulos y el texto en una superficie intermedia, puede usarlo como entrada para los objetos [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) en el gráfico de imagen.

En este ejemplo, establezca la imagen original como la entrada del [efecto de desenfoque gausiano](gaussian-blur.md) y, a continuación, establezca la salida del desenfoque como entrada para el [efecto de iluminación especular de punto](specular-lighting.md). El resultado de este efecto se compone dos veces con la imagen original para obtener la imagen final que se representa en la ventana.

Este es un diagrama del gráfico de imágenes.

![diagrama del gráfico de efectos.](images/effect-graph.png)

Este gráfico de efectos consta de cuatro objetos [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) , cada uno de los cuales representa un efecto integrado diferente. Puede crear y conectar efectos personalizados de la misma manera, después de registrarlos mediante [**ID1D1Factory1:: RegisterEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring). Aquí el código crea los efectos, establece las propiedades y conecta el gráfico de efectos mostrado anteriormente.

1.  Cree el efecto [Desenfoque gaussiano](gaussian-blur.md) mediante el método [**ID2D1DeviceContext:: CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) y especifique el CLSID adecuado. Los CLSID de los efectos integrados se definen en d2d1effects. h. A continuación, establezca la desviación estándar del desenfoque mediante el método [**ID2D1Effect:: SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) .

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

    

    El efecto [Desenfoque gaussiano](gaussian-blur.md) desenfoca todos los canales de la imagen, incluido el canal alfa.

2.  Cree el efecto de [iluminación especular](point-specular.md) y establezca las propiedades. La posición de la luz es un vector de 3 valores de punto flotante, por lo que debe declararlo como una variable independiente y pasarlo al método [**SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) .

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

    

    El efecto de [luz especular](point-specular.md) usa el canal alfa de la entrada para crear un mapa de alto para la iluminación.

3.  Hay dos efectos compuestos diferentes en los que puede usar el efecto [compuesto](composite.md) y el [compuesto aritmético](arithmetic-composite.md). Este gráfico de efectos usa ambos.

    Cree el efecto [compuesto](composite.md) y establezca el modo en el \_ origen del modo compuesto D2D1 \_ \_ \_ en, que genera la intersección de las imágenes de origen y de destino.

    El efecto [compuesto aritmético](arithmetic-composite.md) compone las dos imágenes de entrada en función de una fórmula definida por el World Wide Web Consortium (W3C) para el estándar de gráficos vectoriales escalables (SVG). Cree un compuesto aritmético y establezca los coeficientes para la fórmula.

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

    

    Aquí se muestran los coeficientes para el efecto [compuesto aritmético](arithmetic-composite.md) .

    ```C++
    D2D1_VECTOR_4F sc_arithmeticCoefficients   = D2D1::Vector4F(0.0f, 1.0f, 1.0f, 0.0f);
    ```

    

    En este gráfico de efectos, los dos efectos compuestos toman la salida de los demás efectos y la superficie intermedia como entradas y los compone.

4.  Por último, conecte los efectos para formar el gráfico estableciendo las entradas en las imágenes y los mapas de bits adecuados.

    El primer efecto, [Desenfoque gaussiano](gaussian-blur.md), recibe su entrada de la superficie intermedia a la que representaba los primitivos. La entrada se establece mediante el método [**ID2D1Effect:: SetInput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput) y se especifica el índice de un objeto [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) . Los efectos de desenfoque gaussiano y de [iluminación especular](point-specular.md) tienen una sola entrada. El efecto de iluminación especular usa el canal alfa borroso del desenfoque gaussiano

    Los efectos compuestos [compuestos](composite.md) y [aritméticos](arithmetic-composite.md) tienen varias entradas. Para asegurarse de que las imágenes se colocan en el orden correcto, debe especificar el índice correcto para cada imagen de entrada.

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

    

5.  Pase el objeto de efecto [compuesto aritmético](arithmetic-composite.md) al método [**ID2DDeviceContext::D rawimage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) y procese y dibuje el resultado del gráfico.

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

    

 

 