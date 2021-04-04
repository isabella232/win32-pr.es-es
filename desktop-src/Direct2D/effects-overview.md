---
title: Efectos (Direct2D)
description: Información general sobre los efectos de Direct2D.
ms.assetid: 1446BDA9-AD4C-472C-8F1D-82ABC1880E13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dd29a4b2968e91bd0d516a74ec01538f69821bb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078119"
---
# <a name="effects"></a><span data-ttu-id="58b24-103">Efectos</span><span class="sxs-lookup"><span data-stu-id="58b24-103">Effects</span></span>

## <a name="what-are-direct2d-effects"></a><span data-ttu-id="58b24-104">¿Qué son los efectos de Direct2D?</span><span class="sxs-lookup"><span data-stu-id="58b24-104">What are Direct2D effects?</span></span>

<span data-ttu-id="58b24-105">Puede usar Direct2D para aplicar uno o más efectos de alta calidad a una imagen o a un conjunto de imágenes.</span><span class="sxs-lookup"><span data-stu-id="58b24-105">You can use Direct2D to apply one or more high quality effects to an image or a set of images.</span></span> <span data-ttu-id="58b24-106">Las API de efectos se basan en [Direct3D 11](/windows/desktop/direct3d11/direct3d-11-features) y aprovechan las características de GPU para el procesamiento de imágenes.</span><span class="sxs-lookup"><span data-stu-id="58b24-106">The effects APIs are built on [Direct3D 11](/windows/desktop/direct3d11/direct3d-11-features) and take advantage of GPU features for image processing.</span></span> <span data-ttu-id="58b24-107">Puede encadenar efectos en un gráfico de efectos y componer o combinar el resultado de los efectos.</span><span class="sxs-lookup"><span data-stu-id="58b24-107">You can chain effects in an effect graph and compose or blend the output of effects.</span></span>

<span data-ttu-id="58b24-108">Un efecto de Direct2D realiza una tarea de creación de imágenes, como cambiar el brillo, dessaturar una imagen o crear una sombra paralela.</span><span class="sxs-lookup"><span data-stu-id="58b24-108">A Direct2D effect performs an imaging task, like changing brightness, de-saturating an image, or creating a drop shadow.</span></span> <span data-ttu-id="58b24-109">Los efectos pueden aceptar cero o más imágenes de entrada, exponer varias propiedades que controlan su funcionamiento y generar una sola imagen de salida.</span><span class="sxs-lookup"><span data-stu-id="58b24-109">Effects can accept zero or more input images, expose multiple properties that control their operation, and generate a single output image.</span></span>

<span data-ttu-id="58b24-110">Cada efecto crea un gráfico de transformación interno formado por transformaciones individuales.</span><span class="sxs-lookup"><span data-stu-id="58b24-110">Each effect creates an internal transform graph made up of individual transforms.</span></span> <span data-ttu-id="58b24-111">Cada transformación representa una operación de una sola imagen.</span><span class="sxs-lookup"><span data-stu-id="58b24-111">Each transform represents a single image operation.</span></span> <span data-ttu-id="58b24-112">El propósito principal de una transformación es hospedar los sombreadores que se ejecutan para cada píxel de salida.</span><span class="sxs-lookup"><span data-stu-id="58b24-112">The main purpose of a transform is to house the shaders that are executed for each output pixel.</span></span> <span data-ttu-id="58b24-113">Estos sombreadores pueden incluir sombreadores de píxeles, sombreadores de vértices, la fase de combinación de una GPU y sombreadores de cálculo.</span><span class="sxs-lookup"><span data-stu-id="58b24-113">These shaders can include pixel shaders, vertex shaders, the blend stage of a GPU, and compute shaders.</span></span>

<span data-ttu-id="58b24-114">Tanto los [](./direct2d-portal.md) [efectos integrados de](built-in-effects.md) Direct2D como los efectos personalizados que puede hacer con la [API de efectos personalizados](custom-effects.md) funcionan de esta manera.</span><span class="sxs-lookup"><span data-stu-id="58b24-114">Both the [Direct2D](./direct2d-portal.md) [built-in effects](built-in-effects.md) and custom effects you can make using the [custom effects API](custom-effects.md) work this way.</span></span>

<span data-ttu-id="58b24-115">Hay una serie de [efectos integrados](built-in-effects.md) de categorías como los que se incluyen aquí.</span><span class="sxs-lookup"><span data-stu-id="58b24-115">There are a range of [built-in effects](built-in-effects.md) from categories like the ones here.</span></span> <span data-ttu-id="58b24-116">Vea la sección [efectos integrados](built-in-effects.md) para obtener una lista completa.</span><span class="sxs-lookup"><span data-stu-id="58b24-116">See the [Built-in Effects](built-in-effects.md) section for a full list.</span></span>

-   [<span data-ttu-id="58b24-117">Filtros</span><span class="sxs-lookup"><span data-stu-id="58b24-117">Filtering</span></span>](built-in-effects.md)
-   [<span data-ttu-id="58b24-118">Composición y combinación</span><span class="sxs-lookup"><span data-stu-id="58b24-118">Composition and Blending</span></span>](built-in-effects.md)
-   [<span data-ttu-id="58b24-119">Transparencia</span><span class="sxs-lookup"><span data-stu-id="58b24-119">Transparency</span></span>](built-in-effects.md)
-   [<span data-ttu-id="58b24-120">Color</span><span class="sxs-lookup"><span data-stu-id="58b24-120">Color</span></span>](built-in-effects.md)
-   [<span data-ttu-id="58b24-121">Iluminación y Estilizamiento</span><span class="sxs-lookup"><span data-stu-id="58b24-121">Lighting and Stylizing</span></span>](built-in-effects.md)
-   [<span data-ttu-id="58b24-122">Transformación y escalado</span><span class="sxs-lookup"><span data-stu-id="58b24-122">Transforming and Scaling</span></span>](built-in-effects.md)
-   [<span data-ttu-id="58b24-123">Sources</span><span class="sxs-lookup"><span data-stu-id="58b24-123">Sources</span></span>](built-in-effects.md)

<span data-ttu-id="58b24-124">Puede aplicar efectos a cualquier mapa de bits, como imágenes cargadas por el [componente de creación de imágenes de Windows (WIC)](/windows/desktop/wic/-wic-api), primitivas dibujadas por [Direct2D](./direct2d-portal.md), texto de [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal)o escenas representadas por [Direct3D](/windows/desktop/direct3d10/d3d10-graphics).</span><span class="sxs-lookup"><span data-stu-id="58b24-124">You can apply effects to any bitmap, including: images loaded by the [Windows Imaging Component (WIC)](/windows/desktop/wic/-wic-api), primitives drawn by [Direct2D](./direct2d-portal.md), text from [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal), or scenes rendered by [Direct3D](/windows/desktop/direct3d10/d3d10-graphics).</span></span>

<span data-ttu-id="58b24-125">Con efectos de Direct2D, puede escribir sus propios efectos que puede usar para las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="58b24-125">With Direct2D effects you can write your own effects that you can use for your applications.</span></span> <span data-ttu-id="58b24-126">Un marco de efecto personalizado le permite usar características de GPU como sombreadores de píxeles, sombreadores de vértices y la unidad de fusión.</span><span class="sxs-lookup"><span data-stu-id="58b24-126">A custom effect framework allows you to use GPU features such as pixel shaders, vertex shaders, and the blending unit.</span></span> <span data-ttu-id="58b24-127">También puede incluir otros efectos integrados o personalizados en su efecto personalizado.</span><span class="sxs-lookup"><span data-stu-id="58b24-127">You can also include other built-in or custom effects in your custom effect.</span></span> <span data-ttu-id="58b24-128">El marco para crear efectos personalizados es el mismo que se usó para crear los efectos integrados de [Direct2D](./direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="58b24-128">The framework for building custom effects is the same one that was used to create the built-in effects of [Direct2D](./direct2d-portal.md).</span></span> <span data-ttu-id="58b24-129">La [API de autor del efecto de Direct2D](custom-effects.md) proporciona un conjunto de interfaces para crear y registrar efectos.</span><span class="sxs-lookup"><span data-stu-id="58b24-129">The [Direct2D effect author API](custom-effects.md) provides a set of interfaces to create and register effects.</span></span>

### <a name="more-effects-topics"></a><span data-ttu-id="58b24-130">Temas de más efectos</span><span class="sxs-lookup"><span data-stu-id="58b24-130">More effects topics</span></span>

<span data-ttu-id="58b24-131">En el resto de este tema se explican los aspectos básicos de los efectos de Direct2D, como aplicar un efecto a una imagen.</span><span class="sxs-lookup"><span data-stu-id="58b24-131">The rest of this topic explains the basics of Direct2D effects, like applying an effect to an image.</span></span> <span data-ttu-id="58b24-132">La tabla siguiente contiene vínculos a temas adicionales sobre los efectos.</span><span class="sxs-lookup"><span data-stu-id="58b24-132">The table here has links to additional topics about effects.</span></span>

| <span data-ttu-id="58b24-133">Tema</span><span class="sxs-lookup"><span data-stu-id="58b24-133">Topic</span></span>                                                                                                                    | <span data-ttu-id="58b24-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="58b24-134">Description</span></span>                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="58b24-135">Vinculación del sombreador de efectos</span><span class="sxs-lookup"><span data-stu-id="58b24-135">Effect Shader Linking</span></span>](effect-shader-linking.md)<br/>                                                            | <span data-ttu-id="58b24-136">Direct2D usa una optimización denominada vinculación de sombreador de efectos que combina varios pasos de representación de gráficos de efectos en un solo paso.</span><span class="sxs-lookup"><span data-stu-id="58b24-136">Direct2D uses an optimization called effect shader linking which combines multiple effect graph rendering passes into a single pass.</span></span><br/>                                               |
| [<span data-ttu-id="58b24-137">Efectos personalizados</span><span class="sxs-lookup"><span data-stu-id="58b24-137">Custom effects</span></span>](custom-effects.md)<br/>                                                                          | <span data-ttu-id="58b24-138">Muestra cómo escribir sus propios efectos personalizados mediante HLSL estándar.</span><span class="sxs-lookup"><span data-stu-id="58b24-138">Shows you how to write your own custom effects using standard HLSL.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="58b24-139">Cómo cargar una imagen en los efectos de Direct2D mediante FilePicker</span><span class="sxs-lookup"><span data-stu-id="58b24-139">How to load an image into Direct2D Effects using the FilePicker</span></span>](load-a-id2d1image-using-the-filepicker.md)<br/> | <span data-ttu-id="58b24-140">Muestra cómo usar [**Windows:: Storage::P ickers:: FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) para cargar una imagen en efectos de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="58b24-140">Shows how to use the [**Windows::Storage::Pickers::FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) to load an image into Direct2D effects.</span></span><br/>                                      |
| [<span data-ttu-id="58b24-141">Cómo guardar el contenido de Direct2D en un archivo de imagen</span><span class="sxs-lookup"><span data-stu-id="58b24-141">How to save Direct2D content to an image file</span></span>](save-direct2d-content-to-an-image-file.md)<br/>                   | <span data-ttu-id="58b24-142">En este tema se muestra cómo usar [**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) para guardar contenido en forma de [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) en un archivo de imagen codificado, como JPEG.</span><span class="sxs-lookup"><span data-stu-id="58b24-142">This topic shows how to use [**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) to save content in the form of an [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) to an encoded image file such as JPEG.</span></span><br/> |
| [<span data-ttu-id="58b24-143">Cómo aplicar efectos a primitivos</span><span class="sxs-lookup"><span data-stu-id="58b24-143">How to Apply Effects to Primitives</span></span>](how-to-apply-effects-to-primitives.md)<br/>                                  | <span data-ttu-id="58b24-144">En este tema se muestra cómo aplicar una serie de efectos a los primitivos de [Direct2D](./direct2d-portal.md) y de [DirectWrite](direct2d-and-directwrite.md) .</span><span class="sxs-lookup"><span data-stu-id="58b24-144">This topic shows how to apply a series of effect to [Direct2D](./direct2d-portal.md) and [DirectWrite](direct2d-and-directwrite.md) primitives.</span></span><br/>                           |
| [<span data-ttu-id="58b24-145">Controlar el recorte numérico y de precisión en los gráficos de efectos</span><span class="sxs-lookup"><span data-stu-id="58b24-145">Controlling Precision and Numerical Clipping in Effect Graphs</span></span>](precision-and-clipping-in-effect-graphs.md)<br/>  | <span data-ttu-id="58b24-146">Las aplicaciones que representan efectos mediante Direct2D deben tener cuidado para lograr el nivel deseado de calidad y previsibilidad con respecto a la precisión numérica.</span><span class="sxs-lookup"><span data-stu-id="58b24-146">Applications that render effects using Direct2D must take care to achieve the desired level of quality and predictability with respect to numerical precision.</span></span> <br/>                    |

## <a name="applying-an-effect-to-an-image"></a><span data-ttu-id="58b24-147">Aplicar un efecto a una imagen</span><span class="sxs-lookup"><span data-stu-id="58b24-147">Applying an effect to an image</span></span>

<span data-ttu-id="58b24-148">Puede usar la API de efectos de Direct2D para aplicar transformaciones a las imágenes.</span><span class="sxs-lookup"><span data-stu-id="58b24-148">You can use the Direct2D effects API to apply transforms to images.</span></span>

> [!Note]  
> <span data-ttu-id="58b24-149">En este ejemplo se da por supuesto que ya se han creado los objetos [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) y [IWICBitmapSource](/windows/desktop/wic/-wic-imp-iwicbitmapsource) .</span><span class="sxs-lookup"><span data-stu-id="58b24-149">This example assumes that you already have [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) and [IWICBitmapSource](/windows/desktop/wic/-wic-imp-iwicbitmapsource) objects created.</span></span> <span data-ttu-id="58b24-150">Para obtener más información sobre la creación de estos objetos, vea [Cómo cargar una imagen en los efectos de Direct2D mediante FilePicker y los](load-a-id2d1image-using-the-filepicker.md) [dispositivos y contextos de dispositivo](devices-and-device-contexts.md).</span><span class="sxs-lookup"><span data-stu-id="58b24-150">For more information on creating these objects see [How to load an image into Direct2D effects using the FilePicker](load-a-id2d1image-using-the-filepicker.md) and [Devices and Device Contexts](devices-and-device-contexts.md).</span></span>

 

1.  <span data-ttu-id="58b24-151">Declare una variable [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) y, a continuación, cree un efecto de [origen de mapa de bits](bitmap-source.md) con el método [**ID2DDeviceContext:: CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) .</span><span class="sxs-lookup"><span data-stu-id="58b24-151">Declare an [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) variable and then create a [bitmap source](bitmap-source.md) effect using the [**ID2DDeviceContext::CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) method.</span></span>

    ```C++
        ComPtr<ID2D1Effect> bitmapSourceEffect;

        DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1BitmapSource, &bitmapSourceEffect));
    ```

    

2.  <span data-ttu-id="58b24-152">Establezca la propiedad BitmapSource en el origen de mapa de bits de WIC mediante [**ID2D1Effect:: SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)).</span><span class="sxs-lookup"><span data-stu-id="58b24-152">Set the BitmapSource property to the WIC bitmap source using the [**ID2D1Effect::SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)).</span></span>

    ```C++
            DX::ThrowIfFailed(m_bitmapSourceEffect->SetValue(D2D1_BITMAPSOURCE_PROP_WIC_BITMAP_SOURCE, m_wicBitmapSource.Get()));
    ```

    

3.  <span data-ttu-id="58b24-153">Declare una variable [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) y, a continuación, cree el efecto [Desenfoque gaussiano](gaussian-blur.md) .</span><span class="sxs-lookup"><span data-stu-id="58b24-153">Declare an [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) variable and then create the [gaussian blur](gaussian-blur.md) effect.</span></span>

    ```C++
        ComPtr<ID2D1Effect> gaussianBlurEffect;

        DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1GaussianBlur, &gaussianBlurEffect));
    ```

    

4.  <span data-ttu-id="58b24-154">Establezca la entrada para recibir la imagen del efecto de origen del mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="58b24-154">Set the input to receive the image from the bitmap source effect.</span></span> <span data-ttu-id="58b24-155">Establezca la cantidad de desenfoque en el método [**SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) y la propiedad desviación estándar.</span><span class="sxs-lookup"><span data-stu-id="58b24-155">Set the blur amount the [**SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) method and the standard deviation property.</span></span>

    ```C++
        gaussianBlurEffect->SetInputEffect(0, bitmapSourceEffect.Get());

        DX::ThrowIfFailed(gaussianBlurEffect->SetValue(D2D1_GAUSSIANBLUR_PROP_STANDARD_DEVIATION, 6.0f));
    ```

    

5.  <span data-ttu-id="58b24-156">Use el contexto de dispositivo para dibujar el resultado de la imagen resultante.</span><span class="sxs-lookup"><span data-stu-id="58b24-156">Use the device context to draw the resulting image output.</span></span>

    ```C++
        m_d2dContext->BeginDraw();

        m_d2dContext->Clear(D2D1::ColorF(D2D1::ColorF::CornflowerBlue));

        // Draw the blurred image.
        m_d2dContext->DrawImage(gaussianBlurEffect.Get());

        HRESULT hr = m_d2dContext->EndDraw();
    ```

    

    <span data-ttu-id="58b24-157">Se debe llamar al método [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) entre las llamadas a [**ID2DDeviceContext:: BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) y [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) como otras operaciones de representación en Direct2D.</span><span class="sxs-lookup"><span data-stu-id="58b24-157">The [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) method must be called between the [**ID2DDeviceContext::BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) and [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) calls like other Direct2D render operations.</span></span> <span data-ttu-id="58b24-158">**DrawImage** puede tomar una imagen o la salida de un efecto y representarla en la superficie de destino.</span><span class="sxs-lookup"><span data-stu-id="58b24-158">**DrawImage** can take an image or the output of an effect and render it to the target surface.</span></span>

## <a name="spatial-transforms"></a><span data-ttu-id="58b24-159">Transformaciones espaciales</span><span class="sxs-lookup"><span data-stu-id="58b24-159">Spatial Transforms</span></span>

<span data-ttu-id="58b24-160">Direct2D proporciona efectos integrados que pueden transformar imágenes en el espacio 2D y 3D, así como el escalado.</span><span class="sxs-lookup"><span data-stu-id="58b24-160">Direct2D provides built-in effects that can transform images in 2D and 3D space, as well as scaling.</span></span> <span data-ttu-id="58b24-161">Los efectos de escala y transformación ofrecen diversos niveles de calidad como el vecino más cercano, lineal, cúbica, Multimuestra lineal, anisotrópico y cúbico de alta calidad.</span><span class="sxs-lookup"><span data-stu-id="58b24-161">The scale and transform effects offer various quality levels like: nearest neighbor, linear, cubic, multi-sample linear, anisotropic, and high quality cubic.</span></span>

> [!Note]  
> <span data-ttu-id="58b24-162">El modo anisotrópico genera mapas MIP al escalar; sin embargo, si establece la propiedad **Cached** en true en los efectos que son la entrada en la transformación, los mapas MIP no se generarán cada vez para imágenes suficientemente pequeñas.</span><span class="sxs-lookup"><span data-stu-id="58b24-162">Anisotropic mode generates mipmaps when scaling, however, if you set the **Cached** property to true on the effects that are input to the transform the mipmaps won't be generated every time for sufficiently small images.</span></span>

 


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



<span data-ttu-id="58b24-163">Este uso del efecto de transformación afín 2D gira ligeramente el mapa de bits en sentido contrario a las agujas del reloj.</span><span class="sxs-lookup"><span data-stu-id="58b24-163">This use of the 2D affine transform effect rotates the bitmap counterclockwise slightly.</span></span>



| <span data-ttu-id="58b24-164">Antes</span><span class="sxs-lookup"><span data-stu-id="58b24-164">Before</span></span>                                                            |
|-------------------------------------------------------------------|
| ![efecto afín 2D antes de la imagen.](images/default-before.jpg)      |
| <span data-ttu-id="58b24-166">Después</span><span class="sxs-lookup"><span data-stu-id="58b24-166">After</span></span>                                                             |
| ![efecto afín 2D después de la imagen.](images/21-2daffinetransform.png) |



 

## <a name="compositing-images"></a><span data-ttu-id="58b24-168">Composición de imágenes</span><span class="sxs-lookup"><span data-stu-id="58b24-168">Compositing images</span></span>

<span data-ttu-id="58b24-169">Algunos efectos aceptan varias entradas y las componen en una imagen resultante.</span><span class="sxs-lookup"><span data-stu-id="58b24-169">Some effects accept multiple inputs and composite them into one resulting image.</span></span>

<span data-ttu-id="58b24-170">Los efectos compuestos compuestos y aritméticos integrados proporcionan varios modos. para obtener más información, vea el tema [compuesto](composite.md) .</span><span class="sxs-lookup"><span data-stu-id="58b24-170">The built-in composite and arithmetic composite effects provide various modes, for more info see the [composite](composite.md) topic.</span></span> <span data-ttu-id="58b24-171">El efecto de [mezcla](blend.md) tiene una variedad de modos acelerados de GPU disponibles.</span><span class="sxs-lookup"><span data-stu-id="58b24-171">The [blend](blend.md) effect has a variety of GPU accelerated modes available.</span></span>


```C++
ComPtr<ID2D1Effect> compositeEffect;
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect));

compositeEffect->SetInput(0, bitmap.Get());
compositeEffect->SetInput(1, bitmapTwo.Get());

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="58b24-172">El efecto compuesto combina imágenes de varias maneras diferentes según el modo especificado.</span><span class="sxs-lookup"><span data-stu-id="58b24-172">The composite effect combines images in various different ways according to the mode you specify.</span></span>

## <a name="pixel-adjustments"></a><span data-ttu-id="58b24-173">Ajustes de píxeles</span><span class="sxs-lookup"><span data-stu-id="58b24-173">Pixel adjustments</span></span>

<span data-ttu-id="58b24-174">Hay algunos efectos de Direct2D integrados que permiten modificar los datos de píxeles.</span><span class="sxs-lookup"><span data-stu-id="58b24-174">There are a few built-in Direct2D effects that allow you to alter the pixel data.</span></span> <span data-ttu-id="58b24-175">Por ejemplo, el efecto de la matriz de colores se puede usar para cambiar el color de una imagen.</span><span class="sxs-lookup"><span data-stu-id="58b24-175">For example, the color matrix effect can be used to change the color of an image.</span></span>


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



<span data-ttu-id="58b24-176">Este código toma la imagen y modifica el color tal y como se muestra en las imágenes de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="58b24-176">This code takes the image and alters the color as shown in the example images here.</span></span>



| <span data-ttu-id="58b24-177">Antes</span><span class="sxs-lookup"><span data-stu-id="58b24-177">Before</span></span>                                                          |
|-----------------------------------------------------------------|
| ![efecto de la matriz de colores antes de la imagen.](images/default-before.jpg) |
| <span data-ttu-id="58b24-179">Después</span><span class="sxs-lookup"><span data-stu-id="58b24-179">After</span></span>                                                           |
| ![efecto de la matriz de colores después de la imagen.](images/15-colormatrix.png)  |



 

<span data-ttu-id="58b24-181">Vea la sección [efectos integrados de color](how-to-create-a-solid-color-brush.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="58b24-181">See the [color built-in effects](how-to-create-a-solid-color-brush.md) section for more info.</span></span>

## <a name="building-effect-graphs"></a><span data-ttu-id="58b24-182">Crear gráficos de efectos</span><span class="sxs-lookup"><span data-stu-id="58b24-182">Building effect graphs</span></span>

<span data-ttu-id="58b24-183">Puede encadenar efectos juntos para transformar imágenes.</span><span class="sxs-lookup"><span data-stu-id="58b24-183">You can chain effects together to transform images.</span></span> <span data-ttu-id="58b24-184">Por ejemplo, el código que se muestra aquí aplica una sombra y una transformación 2D y, a continuación, compone los resultados juntos.</span><span class="sxs-lookup"><span data-stu-id="58b24-184">For example, the code here applies a shadow and a 2D transform, then composites the results together.</span></span>


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



<span data-ttu-id="58b24-185">Este es el resultado.</span><span class="sxs-lookup"><span data-stu-id="58b24-185">Here is the result.</span></span>

![salida de efecto de sombra.](images/effect-overview-shadow.png)

<span data-ttu-id="58b24-187">Los efectos toman los objetos [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) como entrada.</span><span class="sxs-lookup"><span data-stu-id="58b24-187">Effects take [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) objects as input.</span></span> <span data-ttu-id="58b24-188">Puede usar un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) porque la interfaz se deriva de **ID2D1Image**.</span><span class="sxs-lookup"><span data-stu-id="58b24-188">You can use an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) because the interface is derived from **ID2D1Image**.</span></span> <span data-ttu-id="58b24-189">También puede usar [**ID2D1Effect:: GetOutput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-getoutput) para obtener la salida de un objeto [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) como **ID2D1Image** o usar el método **SetInputEffect** , que convierte la salida por usted.</span><span class="sxs-lookup"><span data-stu-id="58b24-189">You can also use the [**ID2D1Effect::GetOutput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-getoutput) to get the output of an [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) object as an **ID2D1Image** or use the **SetInputEffect** method, which converts the output for you.</span></span> <span data-ttu-id="58b24-190">En la mayoría de los casos, un gráfico de efectos está formado por objetos **ID2D1Effect** directamente encadenados, lo que facilita la aplicación de varios efectos a una imagen para crear objetos visuales atractivos.</span><span class="sxs-lookup"><span data-stu-id="58b24-190">In most cases an effect graph consists of **ID2D1Effect** objects directly chained together, which makes it easy to apply multiple effects to an image to create compelling visuals.</span></span>

<span data-ttu-id="58b24-191">Vea [Cómo aplicar efectos a primitivos](how-to-apply-effects-to-primitives.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="58b24-191">See [How to apply effects to primitives](how-to-apply-effects-to-primitives.md) for more info.</span></span>

## <a name="related-topics"></a><span data-ttu-id="58b24-192">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="58b24-192">Related topics</span></span>

[<span data-ttu-id="58b24-193">Ejemplo de efectos de imagen básicos de Direct2D</span><span class="sxs-lookup"><span data-stu-id="58b24-193">Direct2D basic image effects sample</span></span>](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20basic%20image%20effects%20sample)

[<span data-ttu-id="58b24-194">Efectos integrados</span><span class="sxs-lookup"><span data-stu-id="58b24-194">Built-in Effects</span></span>](built-in-effects.md)