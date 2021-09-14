---
title: Efectos (Direct2D)
description: Información general sobre los efectos de Direct2D.
ms.assetid: 1446BDA9-AD4C-472C-8F1D-82ABC1880E13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dd29a4b2968e91bd0d516a74ec01538f69821bb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127163294"
---
# <a name="effects"></a>Efectos

## <a name="what-are-direct2d-effects"></a>¿Qué son los efectos de Direct2D?

Puede usar Direct2D para aplicar uno o varios efectos de alta calidad a una imagen o un conjunto de imágenes. Las API de efectos se basa en [Direct3D 11](/windows/desktop/direct3d11/direct3d-11-features) y aprovechan las características de GPU para el procesamiento de imágenes. Puede encadenar efectos en un gráfico de efectos y componer o combinar la salida de los efectos.

Un efecto de Direct2D realiza una tarea de creación de imágenes, como cambiar el brillo, desa saturar una imagen o crear una sombra paralela. Los efectos pueden aceptar cero o más imágenes de entrada, exponer varias propiedades que controlan su operación y generar una sola imagen de salida.

Cada efecto crea un gráfico de transformación interno que se realiza con transformaciones individuales. Cada transformación representa una única operación de imagen. El propósito principal de una transformación es hospedar los sombreadores que se ejecutan para cada píxel de salida. Estos sombreadores pueden incluir sombreadores de píxeles, sombreadores de vértices, la fase de mezcla de una GPU y sombreadores de proceso.

Tanto los [efectos integrados de Direct2D](./direct2d-portal.md) [](built-in-effects.md) como los efectos personalizados que puede hacer con la API de efectos [personalizados](custom-effects.md) funcionan de esta manera.

Hay una variedad de [efectos integrados de](built-in-effects.md) categorías como las que se encuentran aquí. Consulte la [sección Efectos integrados](built-in-effects.md) para obtener una lista completa.

-   [Filtros](built-in-effects.md)
-   [Composición y combinación](built-in-effects.md)
-   [Transparencia](built-in-effects.md)
-   [Color](built-in-effects.md)
-   [Iluminación y stylizing](built-in-effects.md)
-   [Transformación y escalado](built-in-effects.md)
-   [Sources](built-in-effects.md)

Puede aplicar efectos a cualquier mapa de bits, incluidas: imágenes cargadas por el componente de creación de imágenes [de Windows (WIC),](/windows/desktop/wic/-wic-api)primitivas dibujadas por [Direct2D,](./direct2d-portal.md)texto [de DirectWrite](/windows/desktop/DirectWrite/direct-write-portal)o escenas representados por [Direct3D.](/windows/desktop/direct3d10/d3d10-graphics)

Con los efectos de Direct2D puede escribir sus propios efectos que puede usar para las aplicaciones. Un marco de efectos personalizado le permite usar características de GPU como sombreadores de píxeles, sombreadores de vértices y la unidad de combinación. También puede incluir otros efectos integrados o personalizados en el efecto personalizado. El marco para crear efectos personalizados es el mismo que se usó para crear los efectos integrados de [Direct2D.](./direct2d-portal.md) La [API de creación de efectos de Direct2D](custom-effects.md) proporciona un conjunto de interfaces para crear y registrar efectos.

### <a name="more-effects-topics"></a>Temas sobre más efectos

En el resto de este tema se explican los aspectos básicos de los efectos de Direct2D, como aplicar un efecto a una imagen. La tabla aquí tiene vínculos a temas adicionales sobre los efectos.

| Tema                                                                                                                    | Descripción                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Vinculación del sombreador de efectos](effect-shader-linking.md)<br/>                                                            | Direct2D usa una optimización denominada vinculación del sombreador de efectos que combina los pases de representación de grafos de varios efectos en un solo paso.<br/>                                               |
| [Efectos personalizados](custom-effects.md)<br/>                                                                          | Muestra cómo escribir sus propios efectos personalizados mediante HLSL estándar.<br/>                                                                                                                |
| [Carga de una imagen en efectos de Direct2D mediante FilePicker](load-a-id2d1image-using-the-filepicker.md)<br/> | Muestra cómo usar [**Windows::Storage::P ickers::FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) para cargar una imagen en efectos de Direct2D.<br/>                                      |
| [Cómo guardar el contenido de Direct2D en un archivo de imagen](save-direct2d-content-to-an-image-file.md)<br/>                   | En este tema se muestra cómo usar [**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) para guardar contenido en forma de [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) en un archivo de imagen codificado como JPEG.<br/> |
| [Cómo aplicar efectos a primitivas](how-to-apply-effects-to-primitives.md)<br/>                                  | En este tema se muestra cómo aplicar una serie de efectos a [Direct2D](./direct2d-portal.md) [y DirectWrite](direct2d-and-directwrite.md) primitivos.<br/>                           |
| [Controlar la precisión y el recorte numérico en gráficos de efecto](precision-and-clipping-in-effect-graphs.md)<br/>  | Las aplicaciones que representan efectos mediante Direct2D deben tener cuidado para lograr el nivel deseado de calidad y predictibilidad con respecto a la precisión numérica. <br/>                    |

## <a name="applying-an-effect-to-an-image"></a>Aplicar un efecto a una imagen

Puede usar la API de efectos de Direct2D para aplicar transformaciones a las imágenes.

> [!Note]  
> En este ejemplo se supone que ya tiene objetos [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) [e IWICBitmapSource](/windows/desktop/wic/-wic-imp-iwicbitmapsource) creados. Para obtener más información sobre cómo crear estos objetos, vea Carga de una imagen en efectos de [Direct2D mediante FilePicker](load-a-id2d1image-using-the-filepicker.md) y [Dispositivos y contextos de dispositivo.](devices-and-device-contexts.md)

 

1.  Declare una variable [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) y, [a](bitmap-source.md) continuación, cree un efecto de origen de mapa de bits mediante el [**método ID2DDeviceContext::CreateEffect.**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect)

    ```C++
        ComPtr<ID2D1Effect> bitmapSourceEffect;

        DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1BitmapSource, &bitmapSourceEffect));
    ```

    

2.  Establezca la propiedad BitmapSource en el origen de mapa de bits de WIC mediante [**id2D1Effect::SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)).

    ```C++
            DX::ThrowIfFailed(m_bitmapSourceEffect->SetValue(D2D1_BITMAPSOURCE_PROP_WIC_BITMAP_SOURCE, m_wicBitmapSource.Get()));
    ```

    

3.  Declare una [**variable ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) y cree el [efecto de desenfoque gaussiano.](gaussian-blur.md)

    ```C++
        ComPtr<ID2D1Effect> gaussianBlurEffect;

        DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1GaussianBlur, &gaussianBlurEffect));
    ```

    

4.  Establezca la entrada para recibir la imagen del efecto de origen del mapa de bits. Establezca la cantidad de desenfoque [**del método SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) y la propiedad de desviación estándar.

    ```C++
        gaussianBlurEffect->SetInputEffect(0, bitmapSourceEffect.Get());

        DX::ThrowIfFailed(gaussianBlurEffect->SetValue(D2D1_GAUSSIANBLUR_PROP_STANDARD_DEVIATION, 6.0f));
    ```

    

5.  Use el contexto del dispositivo para dibujar la salida de la imagen resultante.

    ```C++
        m_d2dContext->BeginDraw();

        m_d2dContext->Clear(D2D1::ColorF(D2D1::ColorF::CornflowerBlue));

        // Draw the blurred image.
        m_d2dContext->DrawImage(gaussianBlurEffect.Get());

        HRESULT hr = m_d2dContext->EndDraw();
    ```

    

    Se debe llamar al método [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) entre las llamadas [**ID2DDeviceContext::BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) y [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) como otras operaciones de representación de Direct2D. **DrawImage** puede tomar una imagen o la salida de un efecto y representarla en la superficie de destino.

## <a name="spatial-transforms"></a>Transformaciones espaciales

Direct2D proporciona efectos integrados que pueden transformar imágenes en espacio 2D y 3D, así como escalado. Los efectos de escala y transformación ofrecen varios niveles de calidad como: vecino más próximo, lineal, cúbico, lineal de varias muestras, anisotropico y cúbico de alta calidad.

> [!Note]  
> El modo anisotropico genera mapas MIP al escalar, pero si establece la propiedad **Cached** en true en los efectos que se introducen en la transformación, los mapas mipmap no se generarán cada vez para imágenes lo suficientemente pequeñas.

 


```C++
ComPtr<ID2D1Effect> affineTransformEffect;
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D12DAffineTransform, &affineTransformEffect));

affineTransformEffect->SetInput(0, bitmap.Get());

D2D1_MATRIX_3X2_F matrix = D2D1::Matrix3x2F(0.9f, -0.1f,  0.1f, 0.9f, 8.0f, 45.0f);
DX::ThrowIfFailed(affineTransformEffect->SetValue(D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX, matrix));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(affineTransformEffect.Get());
m_d2dContext->EndDraw();
```



Este uso del efecto de transformación afín 2D gira ligeramente el mapa de bits en sentido contrario a las agujas del reloj.



| Antes                                                            |
|-------------------------------------------------------------------|
| ![Efecto afín 2d antes de la imagen.](images/default-before.jpg)      |
| Después                                                             |
| ![Efecto de affine 2d después de la imagen.](images/21-2daffinetransform.png) |



 

## <a name="compositing-images"></a>Crear imágenes

Algunos efectos aceptan varias entradas y las componen en una imagen resultante.

Los efectos compuestos y aritméticos compuestos integrados proporcionan varios modos. Para más información, consulte el [tema compuesto.](composite.md) El [efecto blend](blend.md) tiene una variedad de modos acelerados de GPU disponibles.


```C++
ComPtr<ID2D1Effect> compositeEffect;
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect));

compositeEffect->SetInput(0, bitmap.Get());
compositeEffect->SetInput(1, bitmapTwo.Get());

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



El efecto compuesto combina imágenes de varias maneras diferentes según el modo que especifique.

## <a name="pixel-adjustments"></a>Ajustes de píxeles

Hay algunos efectos integrados de Direct2D que le permiten modificar los datos de píxeles. Por ejemplo, el efecto de matriz de colores se puede usar para cambiar el color de una imagen.


```C++
ComPtr<ID2D1Effect> colorMatrixEffect;
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1ColorMatrix, &colorMatrixEffect));

colorMatrixEffect->SetInput(0, bitmap.Get());

D2D1_MATRIX_5X4_F matrix = D2D1::Matrix5x4F(0, 0, 1, 0,   0, 1, 0, 0,   1, 0, 0, 0,   0, 0, 0, 1,   0, 0, 0, 0);
DX::ThrowIfFailed(colorMatrixEffect->SetValue(D2D1_COLORMATRIX_PROP_COLOR_MATRIX, matrix));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(colorMatrixEffect.Get());
m_d2dContext->EndDraw();
```



Este código toma la imagen y modifica el color como se muestra aquí en las imágenes de ejemplo.



| Antes                                                          |
|-----------------------------------------------------------------|
| ![efecto de matriz de colores antes de la imagen.](images/default-before.jpg) |
| Después                                                           |
| ![efecto de matriz de colores después de la imagen.](images/15-colormatrix.png)  |



 

Consulte la [sección efectos integrados de color](how-to-create-a-solid-color-brush.md) para obtener más información.

## <a name="building-effect-graphs"></a>Creación de gráficos de efecto

Puede encadenar efectos juntos para transformar imágenes. Por ejemplo, el código aquí aplica una sombra y una transformación 2D y, a continuación, compone los resultados juntos.


```C++
ComPtr<ID2D1Effect> shadowEffect;
ComPtr<ID2D1Effect> affineTransformEffect;
ComPtr<ID2D1Effect> compositeEffect;

DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1Shadow, &shadowEffect));
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D12DAffineTransform, &affineTransformEffect));
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect));

shadowEffect->SetInput(0, bitmap.Get());
affineTransformEffect->SetInputEffect(0, shadowEffect.Get());

D2D1_MATRIX_3X2_F matrix = D2D1::Matrix3x2F::Translation(20, 20));

affineTransformEffect->SetValue(D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX, matrix);

compositeEffect->SetInputEffect(0, affineTransformEffect.Get());
compositeEffect->SetInput(1, bitmap.Get());

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



Este es el resultado.

![salida del efecto de sombra.](images/effect-overview-shadow.png)

Los efectos [**toman objetos ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) como entrada. Puede usar un [**id2D1Bitmap porque**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) la interfaz se deriva de **ID2D1Image**. También puede usar [**ID2D1Effect::GetOutput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-getoutput) para obtener la salida de un objeto [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) como **ID2D1Image** o usar el método **SetInputEffect,** que convierte la salida automáticamente. En la mayoría de los casos, un gráfico de efectos consta de objetos **ID2D1Effect** directamente encadenados, lo que facilita la aplicación de varios efectos a una imagen para crear objetos visuales atractivos.

Consulte [Cómo aplicar efectos a primitivas](how-to-apply-effects-to-primitives.md) para obtener más información.

## <a name="related-topics"></a>Temas relacionados

[Ejemplo de efectos de imagen básicos de Direct2D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20basic%20image%20effects%20sample)

[Efectos integrados](built-in-effects.md)