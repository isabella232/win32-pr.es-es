---
title: Información general sobre las máscaras de opacidad
description: 'En este tema se describe cómo usar mapas de bits y pinceles para definir máscaras de opacidad. Contiene las siguientes secciones:'
ms.assetid: 869821b0-6ebe-46c2-aab6-93177d8a92c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49a4757a30247da465e0ae5226bd923219e3e665
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104551860"
---
# <a name="opacity-masks-overview"></a><span data-ttu-id="bfe08-104">Información general sobre las máscaras de opacidad</span><span class="sxs-lookup"><span data-stu-id="bfe08-104">Opacity Masks Overview</span></span>

<span data-ttu-id="bfe08-105">En este tema se describe cómo usar mapas de bits y pinceles para definir máscaras de opacidad.</span><span class="sxs-lookup"><span data-stu-id="bfe08-105">This topic describes how to use bitmaps and brushes to define opacity masks.</span></span> <span data-ttu-id="bfe08-106">Contiene las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="bfe08-106">It contains the following sections.</span></span>

-   [<span data-ttu-id="bfe08-107">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="bfe08-107">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="bfe08-108">¿Qué es una máscara de opacidad?</span><span class="sxs-lookup"><span data-stu-id="bfe08-108">What Is an Opacity Mask?</span></span>](#what-is-an-opacity-mask)
-   [<span data-ttu-id="bfe08-109">Usar un mapa de bits como máscara de opacidad con el método FillOpacityMask</span><span class="sxs-lookup"><span data-stu-id="bfe08-109">Use a Bitmap as an Opacity Mask with the FillOpacityMask Method</span></span>](#use-a-bitmap-as-an-opacity-mask-with-the-fillopacitymask-method)
-   [<span data-ttu-id="bfe08-110">Usar un pincel como máscara de opacidad con el método FillGeometry</span><span class="sxs-lookup"><span data-stu-id="bfe08-110">Use a Brush as an Opacity Mask with the FillGeometry Method</span></span>](#use-a-brush-as-an-opacity-mask-with-the-fillgeometry-method)
    -   [<span data-ttu-id="bfe08-111">Usar un pincel de degradado lineal como máscara de opacidad</span><span class="sxs-lookup"><span data-stu-id="bfe08-111">Use an Linear Gradient Brush as an Opacity Mask</span></span>](#use-an-linear-gradient-brush-as-an-opacity-mask)
    -   [<span data-ttu-id="bfe08-112">Usar un pincel de degradado radial como máscara de opacidad</span><span class="sxs-lookup"><span data-stu-id="bfe08-112">Use a Radial Gradient Brush as an Opacity Mask</span></span>](#use-a-radial-gradient-brush-as-an-opacity-mask)
-   [<span data-ttu-id="bfe08-113">Aplicar una máscara de opacidad a una capa</span><span class="sxs-lookup"><span data-stu-id="bfe08-113">Apply an Opacity Mask to a Layer</span></span>](#apply-an-opacity-mask-to-a-layer)
-   [<span data-ttu-id="bfe08-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bfe08-114">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="bfe08-115">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="bfe08-115">Prerequisites</span></span>

<span data-ttu-id="bfe08-116">En esta información general se supone que está familiarizado con las operaciones básicas de dibujo de Direct2D, como se describe en el tutorial [creación de una aplicación de Direct2d simple](direct2d-quickstart.md) .</span><span class="sxs-lookup"><span data-stu-id="bfe08-116">This overview assumes that you are familiar with basic Direct2D drawing operations, as described in the [Creating a Simple Direct2D Application](direct2d-quickstart.md) walkthrough.</span></span> <span data-ttu-id="bfe08-117">También debe estar familiarizado con los distintos tipos de pinceles, tal y como se describe en la [información general de los pinceles](direct2d-brushes-overview.md).</span><span class="sxs-lookup"><span data-stu-id="bfe08-117">You should also be familiar with the different types of brushes, as described in the [Brushes Overview](direct2d-brushes-overview.md).</span></span>

## <a name="what-is-an-opacity-mask"></a><span data-ttu-id="bfe08-118">¿Qué es una máscara de opacidad?</span><span class="sxs-lookup"><span data-stu-id="bfe08-118">What Is an Opacity Mask?</span></span>

<span data-ttu-id="bfe08-119">Una máscara de opacidad es una máscara, descrita por un pincel o mapa de bits, que se aplica a otro objeto para hacer que ese objeto sea parcial o completamente transparente.</span><span class="sxs-lookup"><span data-stu-id="bfe08-119">An opacity mask is a mask, described by a brush or bitmap, that is applied to another object to make that object partially or completely transparent.</span></span> <span data-ttu-id="bfe08-120">Una máscara de opacidad usa información de canal alfa para especificar cómo se mezclan los píxeles de origen del objeto en el destino final de destino.</span><span class="sxs-lookup"><span data-stu-id="bfe08-120">An opacity mask uses alpha channel information to specify how the source pixels of the object are blended into the final destination target.</span></span> <span data-ttu-id="bfe08-121">Las partes transparentes de la máscara indican las áreas en las que se oculta la imagen subyacente, mientras que las partes opacas de la máscara indican dónde está visible el objeto con máscara.</span><span class="sxs-lookup"><span data-stu-id="bfe08-121">The transparent portions of the mask indicate the areas where the underlying image is hidden, whereas the opaque portions of the mask indicate where the masked object is visible.</span></span>

<span data-ttu-id="bfe08-122">Hay varias maneras de aplicar una máscara de opacidad:</span><span class="sxs-lookup"><span data-stu-id="bfe08-122">There are several ways to apply an opacity mask:</span></span>

-   <span data-ttu-id="bfe08-123">Use el método [**ID2D1RenderTarget:: FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) .</span><span class="sxs-lookup"><span data-stu-id="bfe08-123">Use the [**ID2D1RenderTarget::FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) method.</span></span> <span data-ttu-id="bfe08-124">El método **FillOpacityMask** pinta una región rectangular de un destino de representación y, a continuación, aplica una máscara de opacidad, definida por un mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="bfe08-124">The **FillOpacityMask** method paints a rectangular region of a render target and then applies an opacity mask, defined by a bitmap.</span></span> <span data-ttu-id="bfe08-125">Use este método cuando la máscara de opacidad sea un mapa de bits y desee rellenar una región rectangular.</span><span class="sxs-lookup"><span data-stu-id="bfe08-125">Use this method when your opacity mask is a bitmap and you want to fill a rectangular region.</span></span>
-   <span data-ttu-id="bfe08-126">Use el método [**ID2D1RenderTarget:: FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) .</span><span class="sxs-lookup"><span data-stu-id="bfe08-126">Use the [**ID2D1RenderTarget::FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method.</span></span> <span data-ttu-id="bfe08-127">El método **FillGeometry** pinta el interior de Geometry con el [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)especificado y, a continuación, aplica una máscara de opacidad, definida por un pincel.</span><span class="sxs-lookup"><span data-stu-id="bfe08-127">The **FillGeometry** method paints the interior of geometry with the specified [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), then applies an opacity mask, defined by a brush.</span></span> <span data-ttu-id="bfe08-128">Utilice este método cuando desee aplicar una máscara de opacidad a una geometría o desee usar un pincel como máscara de opacidad.</span><span class="sxs-lookup"><span data-stu-id="bfe08-128">Use this method when you want to apply an opacity mask to a geometry or you want to use a brush as an opacity mask.</span></span>
-   <span data-ttu-id="bfe08-129">Use un [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) para aplicar una máscara de opacidad.</span><span class="sxs-lookup"><span data-stu-id="bfe08-129">Use an [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) to apply an opacity mask.</span></span> <span data-ttu-id="bfe08-130">Use este enfoque cuando desee aplicar una máscara de opacidad a un grupo de contenido de dibujo, no solo a una sola forma o imagen.</span><span class="sxs-lookup"><span data-stu-id="bfe08-130">Use this approach when you want to apply an opacity mask to a group of drawing content, not just a single shape or image.</span></span> <span data-ttu-id="bfe08-131">Para obtener más información, consulte la [información general sobre capas](direct2d-layers-overview.md).</span><span class="sxs-lookup"><span data-stu-id="bfe08-131">For details, see the [Layers Overview](direct2d-layers-overview.md).</span></span>

## <a name="use-a-bitmap-as-an-opacity-mask-with-the-fillopacitymask-method"></a><span data-ttu-id="bfe08-132">Usar un mapa de bits como máscara de opacidad con el método FillOpacityMask</span><span class="sxs-lookup"><span data-stu-id="bfe08-132">Use a Bitmap as an Opacity Mask with the FillOpacityMask Method</span></span>

<span data-ttu-id="bfe08-133">El método [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) pinta una región rectangular de un destino de representación y, a continuación, aplica una máscara de opacidad, definida por un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).</span><span class="sxs-lookup"><span data-stu-id="bfe08-133">The [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) method paints a rectangular region of a render target and then applies an opacity mask, defined by an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).</span></span> <span data-ttu-id="bfe08-134">Use este método cuando tenga un mapa de bits que desee usar como máscara de opacidad para una región rectangular.</span><span class="sxs-lookup"><span data-stu-id="bfe08-134">Use this method when you have a bitmap that you want to use as an opacity mask for a rectangular region.</span></span>

<span data-ttu-id="bfe08-135">En el diagrama siguiente se muestra un efecto de aplicar la máscara de opacidad (un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) con una imagen de una flor) a un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) con una imagen de una planta Fern.</span><span class="sxs-lookup"><span data-stu-id="bfe08-135">The following diagram shows an effect of applying the opacity mask (an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) with an image of a flower) to an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) with an image of a fern plant.</span></span> <span data-ttu-id="bfe08-136">La imagen resultante es un mapa de bits de una planta recortada para la forma flor.</span><span class="sxs-lookup"><span data-stu-id="bfe08-136">The resulting image is a bitmap of a plant clipped to the flower shape.</span></span>

![diagrama de un mapa de bits de flor usado como máscara de opacidad en una imagen de una planta de Fern](images/brushes-ovw-bitmapopacity.png)

<span data-ttu-id="bfe08-138">En los siguientes ejemplos de código se muestra cómo se logra esto.</span><span class="sxs-lookup"><span data-stu-id="bfe08-138">The following code examples shows how this is accomplished.</span></span>

<span data-ttu-id="bfe08-139">En el primer ejemplo se carga el siguiente mapa de bits, *m \_ pBitmapMask*, para su uso como máscara de mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="bfe08-139">The first example loads the following bitmap, *m\_pBitmapMask*, for use as a bitmap mask.</span></span> <span data-ttu-id="bfe08-140">En la ilustración siguiente se muestra el resultado que se genera.</span><span class="sxs-lookup"><span data-stu-id="bfe08-140">The following illustration shows the output that is produced.</span></span> <span data-ttu-id="bfe08-141">Tenga en cuenta que, aunque la parte opaca del mapa de bits aparece en negro, la información de color del mapa de bits no tiene ningún efecto en la máscara de opacidad; solo se utiliza la información de opacidad de cada píxel del mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="bfe08-141">Note that, although the opaque portion of the bitmap appears black, the color information in the bitmap has no effect on the opacity mask; only the opacity information of each pixel in the bitmap is used.</span></span> <span data-ttu-id="bfe08-142">Los píxeles totalmente opacos de este mapa de bits se han coloreado de negro solo con fines ilustrativos.</span><span class="sxs-lookup"><span data-stu-id="bfe08-142">The fully opaque pixels in this bitmap have been colored black for illustrative purposes only.</span></span>

![Ilustración de la máscara de mapa de bits de flor](images/bitmapmask.png)

<span data-ttu-id="bfe08-144">En este ejemplo, el [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) se carga mediante un método auxiliar, LoadResourceBitmap, que se define en otra parte del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="bfe08-144">In this example, the [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) is loaded by a helper method, LoadResourceBitmap, defined elsewhere in the sample.</span></span>


```C++
            if (SUCCEEDED(hr))
            {
                hr = LoadResourceBitmap(
                    m_pRenderTarget,
                    m_pWICFactory,
                    L"BitmapMask",
                    L"Image",
                    &m_pBitmapMask
                    );
            }
```



<span data-ttu-id="bfe08-145">En el ejemplo siguiente se define el pincel, *m \_ pFernBitmapBrush*, al que se aplica la máscara de opacidad.</span><span class="sxs-lookup"><span data-stu-id="bfe08-145">The next example defines the brush, *m\_pFernBitmapBrush*, to which the opacity mask is applied.</span></span> <span data-ttu-id="bfe08-146">En este ejemplo se usa un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) que contiene una imagen de un Fern, pero en su lugar podría usar [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)o [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) .</span><span class="sxs-lookup"><span data-stu-id="bfe08-146">This example uses an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) that contains an image of a fern, but you could use an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), or [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) instead.</span></span> <span data-ttu-id="bfe08-147">En la ilustración siguiente se muestra el resultado que se genera.</span><span class="sxs-lookup"><span data-stu-id="bfe08-147">The following illustration shows the output that is produced.</span></span>

![Ilustración del mapa de bits utilizado por el pincel de mapa de bits](images/fern.png)


```C++
            if (SUCCEEDED(hr))
            {
                D2D1_BITMAP_BRUSH_PROPERTIES propertiesXClampYClamp = 
                    D2D1::BitmapBrushProperties(
                    D2D1_EXTEND_MODE_CLAMP,
                    D2D1_EXTEND_MODE_CLAMP,
                    D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR
                    );
                hr = m_pRenderTarget->CreateBitmapBrush(
                    m_pFernBitmap,
                    propertiesXClampYClamp,
                    &m_pFernBitmapBrush
                    );


            }
```





<span data-ttu-id="bfe08-149">Ahora que la máscara de opacidad y el pincel están definidos, puede usar el método [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) en el método de representación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="bfe08-149">Now that opacity mask and the brush are defined, you can use the [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) method in your application's rendering method.</span></span> <span data-ttu-id="bfe08-150">Cuando se llama al método **FillOpacityMask** , se debe especificar el tipo de máscara de opacidad que se está usando: **D2D1 de máscara de opacidad de \_ \_ \_ \_ metagráfico**, **D2D1 de contenido de máscara de \_ opacidad \_ \_ \_ \_ natural** y **D2D1 de contenido de máscara de \_ opacidad \_ \_ \_ \_ \_ compatible con GDI**.</span><span class="sxs-lookup"><span data-stu-id="bfe08-150">When you call the **FillOpacityMask** method, you must specify the type of opacity mask you are using: **D2D1\_OPACITY\_MASK\_CONTENT\_GRAPHICS**, **D2D1\_OPACITY\_MASK\_CONTENT\_TEXT\_NATURAL**, and **D2D1\_OPACITY\_MASK\_CONTENT\_TEXT\_GDI\_COMPATIBLE**.</span></span> <span data-ttu-id="bfe08-151">Para ver los significados de estos tres tipos, consulte [**D2D1 \_ OPACITY \_ Mask \_ Content**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content).</span><span class="sxs-lookup"><span data-stu-id="bfe08-151">For the meanings of these three types, see [**D2D1\_OPACITY\_MASK\_CONTENT**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content).</span></span>

> [!Note]  
> <span data-ttu-id="bfe08-152">A partir de Windows 8, el contenido de la [**\_ máscara de opacidad \_ \_ D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content) no es necesario.</span><span class="sxs-lookup"><span data-stu-id="bfe08-152">Starting with Windows 8, the [**D2D1\_OPACITY\_MASK\_CONTENT**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content) is not required.</span></span> <span data-ttu-id="bfe08-153">Vea el método [**ID2D1DeviceContext:: FillOpacityMask**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-fillopacitymask(id2d1bitmap_id2d1brush_constd2d1_rect_f_constd2d1_rect_f)) , que no tiene ningún parámetro de **contenido de \_ \_ máscara \_ de opacidad D2D1** .</span><span class="sxs-lookup"><span data-stu-id="bfe08-153">See the [**ID2D1DeviceContext::FillOpacityMask**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-fillopacitymask(id2d1bitmap_id2d1brush_constd2d1_rect_f_constd2d1_rect_f)) method, which has no **D2D1\_OPACITY\_MASK\_CONTENT** parameter.</span></span>

 

<span data-ttu-id="bfe08-154">En el ejemplo siguiente se establece el modo de suavizado de contorno del destino de representación en el modo antialias [**D2D1 con \_ \_ \_ alias**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode) , de modo que la máscara de opacidad funcione correctamente.</span><span class="sxs-lookup"><span data-stu-id="bfe08-154">The next example sets the render target's antialiasing mode to [**D2D1\_ANTIALIAS\_MODE\_ALIASED**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode) so that the opacity mask will work properly.</span></span> <span data-ttu-id="bfe08-155">Después, llama al método [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) y le pasa la máscara de opacidad (*m \_ pBitmapMask*), el pincel al que se aplica la máscara de opacidad (*m \_ pFernBitmapBrush*), el tipo de contenido dentro de la máscara de opacidad ([**\_ \_ \_ \_ gráficos de contenido de máscara de opacidad D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content)) y el área que se va a pintar.</span><span class="sxs-lookup"><span data-stu-id="bfe08-155">It then calls the [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) method and passes it the opacity mask (*m\_pBitmapMask*), the brush to which the opacity mask is applied (*m\_pFernBitmapBrush*), the type of content inside the opacity mask ([**D2D1\_OPACITY\_MASK\_CONTENT\_GRAPHICS**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content)), and the area to paint.</span></span> <span data-ttu-id="bfe08-156">En la ilustración siguiente se muestra el resultado que se genera.</span><span class="sxs-lookup"><span data-stu-id="bfe08-156">The following illustration shows the output that is produced.</span></span>

![Ilustración de la imagen de la planta Fern con una máscara de opacidad aplicada](images/opacitymaskoutput.png)


```C++
        D2D1_RECT_F rcBrushRect = D2D1::RectF(5, 5, 155, 155);


        // D2D1_ANTIALIAS_MODE_ALIASED must be set for FillOpacityMask to function properly
        m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_ALIASED);
        m_pRenderTarget->FillOpacityMask(
            m_pBitmapMask,
            m_pFernBitmapBrush,
            D2D1_OPACITY_MASK_CONTENT_GRAPHICS,
            &rcBrushRect
            );
        m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_PER_PRIMITIVE);
```





<span data-ttu-id="bfe08-158">El código se ha omitido en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="bfe08-158">Code has been omitted from this example.</span></span>

## <a name="use-a-brush-as-an-opacity-mask-with-the-fillgeometry-method"></a><span data-ttu-id="bfe08-159">Usar un pincel como máscara de opacidad con el método FillGeometry</span><span class="sxs-lookup"><span data-stu-id="bfe08-159">Use a Brush as an Opacity Mask with the FillGeometry Method</span></span>

<span data-ttu-id="bfe08-160">En la sección anterior se describe cómo usar [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) como máscara de opacidad.</span><span class="sxs-lookup"><span data-stu-id="bfe08-160">The preceding section described how to use an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) as an opacity mask.</span></span> <span data-ttu-id="bfe08-161">Direct2D también proporciona el método [**ID2D1RenderTarget:: FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) , que permite especificar opcionalmente Brush como máscara de opacidad al rellenar una [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry).</span><span class="sxs-lookup"><span data-stu-id="bfe08-161">Direct2D also provides the [**ID2D1RenderTarget::FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method, which enables you to optionally specify brush as an opacity mask when you fill an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry).</span></span> <span data-ttu-id="bfe08-162">Esto le permite crear máscaras de opacidad a partir de degradados (mediante [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) o [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)) y mapas de bits (mediante **ID2D1Bitmap**).</span><span class="sxs-lookup"><span data-stu-id="bfe08-162">This enables you to create opacity masks from gradients (using [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) or [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)) and bitmaps (using **ID2D1Bitmap**).</span></span>

<span data-ttu-id="bfe08-163">El método [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) toma tres parámetros:</span><span class="sxs-lookup"><span data-stu-id="bfe08-163">The [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method takes three parameters:</span></span>

-   <span data-ttu-id="bfe08-164">El primer parámetro, un [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry), define la forma que se va a pintar.</span><span class="sxs-lookup"><span data-stu-id="bfe08-164">The first parameter, an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry), defines the shape to paint.</span></span>
-   <span data-ttu-id="bfe08-165">El segundo parámetro, un [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush), especifica el pincel que se usa para pintar la geometría.</span><span class="sxs-lookup"><span data-stu-id="bfe08-165">The second parameter, an [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush), specifies the brush used to paint the geometry.</span></span> <span data-ttu-id="bfe08-166">Este parámetro debe ser un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) que tenga los modos x-e y Extend establecidos en la [**\_ abrazadera del \_ modo \_ Extend de D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode).</span><span class="sxs-lookup"><span data-stu-id="bfe08-166">This parameter must be an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) that has its x- and y-extend modes set to [**D2D1\_EXTEND\_MODE\_CLAMP**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode).</span></span>
-   <span data-ttu-id="bfe08-167">El tercer parámetro, un [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush), especifica un pincel que se va a usar como máscara de opacidad.</span><span class="sxs-lookup"><span data-stu-id="bfe08-167">The third parameter, an [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush), specifies a brush to use as the opacity mask.</span></span> <span data-ttu-id="bfe08-168">Este pincel puede ser [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)o [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).</span><span class="sxs-lookup"><span data-stu-id="bfe08-168">This brush may be an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush), or an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).</span></span> <span data-ttu-id="bfe08-169">(Técnicamente, se puede usar un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), pero si se usa un pincel de color sólido como máscara de opacidad, no se generan resultados interesantes).</span><span class="sxs-lookup"><span data-stu-id="bfe08-169">(Technically, you may use an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), but using a solid color brush as an opacity mask doesn't produce interesting results.)</span></span>

<span data-ttu-id="bfe08-170">En las secciones siguientes se describe cómo usar los objetos [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) y [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) como máscaras de opacidad.</span><span class="sxs-lookup"><span data-stu-id="bfe08-170">The following sections describe how to use [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) and [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) objects as opacity masks.</span></span>

### <a name="use-an-linear-gradient-brush-as-an-opacity-mask"></a><span data-ttu-id="bfe08-171">Usar un pincel de degradado lineal como máscara de opacidad</span><span class="sxs-lookup"><span data-stu-id="bfe08-171">Use an Linear Gradient Brush as an Opacity Mask</span></span>

<span data-ttu-id="bfe08-172">En el diagrama siguiente se muestra el efecto de aplicar un pincel de degradado lineal a un rectángulo que se rellena con un mapa de bits de flores.</span><span class="sxs-lookup"><span data-stu-id="bfe08-172">The following diagram shows the effect of applying a linear gradient brush to a rectangle that is filled with a bitmap of flowers.</span></span>

![diagrama de un mapa de bits de flores con un pincel de degradado lineal aplicado](images/brushes-ovw-lineargradient-opacitymask.png)

<span data-ttu-id="bfe08-174">En los pasos siguientes se describe cómo volver a crear este efecto.</span><span class="sxs-lookup"><span data-stu-id="bfe08-174">The steps that follow describe how to re-create this effect.</span></span>

1.  <span data-ttu-id="bfe08-175">Defina el contenido que se va a enmascarar.</span><span class="sxs-lookup"><span data-stu-id="bfe08-175">Define the content to be masked.</span></span> <span data-ttu-id="bfe08-176">En el ejemplo siguiente se crea un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), *m \_ pLinearFadeFlowersBitmap*.</span><span class="sxs-lookup"><span data-stu-id="bfe08-176">The following example creates an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), *m\_pLinearFadeFlowersBitmap*.</span></span> <span data-ttu-id="bfe08-177">El modo Extend x-e y-for *m \_ pLinearFadeFlowersBitmap* se establecen en [**la \_ \_ \_ abrazadera del modo Extend de D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode) para que se pueda usar con una máscara de opacidad mediante el método [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) .</span><span class="sxs-lookup"><span data-stu-id="bfe08-177">The extend mode x- and y- for *m\_pLinearFadeFlowersBitmap* are set to [**D2D1\_EXTEND\_MODE\_CLAMP**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode) so that it can be used with an opacity mask by the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method.</span></span>

    ```cpp
    if (SUCCEEDED(hr))
    {
        // Create the bitmap to be used by the bitmap brush.
        hr = LoadResourceBitmap(
            m_pRenderTarget,
            m_pWICFactory,
            L"LinearFadeFlowers",
            L"Image",
            &m_pLinearFadeFlowersBitmap
            );
    }
 
    if (SUCCEEDED(hr))
        {
            D2D1_BITMAP_BRUSH_PROPERTIES propertiesXClampYClamp = 
                D2D1::BitmapBrushProperties(
                D2D1_EXTEND_MODE_CLAMP,
                D2D1_EXTEND_MODE_CLAMP,
                D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR
                );
    ```

    <span codelanguage="ManagedCPlusPlus"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="bfe08-178">C++</span><span class="sxs-lookup"><span data-stu-id="bfe08-178">C++</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>                if (SUCCEEDED(hr))
                    {
                        hr = m_pRenderTarget->CreateBitmapBrush(
                            m_pLinearFadeFlowersBitmap,
                            propertiesXClampYClamp,
                            &m_pLinearFadeFlowersBitmapBrush
                            );
                    }</code></pre></td>
    </tr>
    </tbody>
    </table>

    <span codelanguage="ManagedCPlusPlus"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="bfe08-179">C++</span><span class="sxs-lookup"><span data-stu-id="bfe08-179">C++</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>            }</code></pre></td>
    </tr>
    </tbody>
    </table>

    

2.  <span data-ttu-id="bfe08-180">Defina la máscara de opacidad.</span><span class="sxs-lookup"><span data-stu-id="bfe08-180">Define the opacity mask.</span></span> <span data-ttu-id="bfe08-181">En el ejemplo de código siguiente se crea un pincel de degradado lineal diagonal (*m \_ pLinearGradientBrush*) que se atenúa desde el negro totalmente opaco en la posición 0 hasta el blanco completamente transparente en la posición 1.</span><span class="sxs-lookup"><span data-stu-id="bfe08-181">The next code example creates a diagonal linear gradient brush (*m\_pLinearGradientBrush*) that fades from fully opaque black at position 0 to completely transparent white at position 1.</span></span>
```C++
                if (SUCCEEDED(hr))
                {
                    ID2D1GradientStopCollection *pGradientStops = NULL;

                    static const D2D1_GRADIENT_STOP gradientStops[] =
                    {
                        {   0.f,  D2D1::ColorF(D2D1::ColorF::Black, 1.0f)  },
                        {   1.f,  D2D1::ColorF(D2D1::ColorF::White, 0.0f)  },
                    };

                    hr = m_pRenderTarget->CreateGradientStopCollection(
                        gradientStops,
                        2,
                        &pGradientStops);


                    if (SUCCEEDED(hr))
                    {
                        hr = m_pRenderTarget->CreateLinearGradientBrush(
                            D2D1::LinearGradientBrushProperties(
                                D2D1::Point2F(0, 0),
                                D2D1::Point2F(150, 150)),
                            pGradientStops,
                            &m_pLinearGradientBrush);
                    }

    
                pGradientStops->Release();
                }
```



    

3.  <span data-ttu-id="bfe08-182">Use el método [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) .</span><span class="sxs-lookup"><span data-stu-id="bfe08-182">Use the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method.</span></span> <span data-ttu-id="bfe08-183">En el ejemplo final se usa el método **FillGeometry** para el pincel de contenido para rellenar un [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) (*m \_ pRectGeo*) con un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) (*m \_ pLinearFadeFlowersBitmap*) y se aplica una máscara de opacidad (*m \_ pLinearGradientBrush*).</span><span class="sxs-lookup"><span data-stu-id="bfe08-183">The final example uses the **FillGeometry** method to the content brush to fill a [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) (*m\_pRectGeo*) with an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) (*m\_pLinearFadeFlowersBitmap*) and applies an opacity mask (*m\_pLinearGradientBrush*).</span></span>
```C++
            m_pRenderTarget->FillGeometry(
                m_pRectGeo, 
                m_pLinearFadeFlowersBitmapBrush, 
                m_pLinearGradientBrush
                );
```

    

<span data-ttu-id="bfe08-184">El código se ha omitido en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="bfe08-184">Code has been omitted from this example.</span></span>

### <a name="use-a-radial-gradient-brush-as-an-opacity-mask"></a><span data-ttu-id="bfe08-185">Usar un pincel de degradado radial como máscara de opacidad</span><span class="sxs-lookup"><span data-stu-id="bfe08-185">Use a Radial Gradient Brush as an Opacity Mask</span></span>

<span data-ttu-id="bfe08-186">En el diagrama siguiente se muestra el efecto visual de aplicar un pincel de degradado radial a un rectángulo que se rellena con un mapa de bits de follaje.</span><span class="sxs-lookup"><span data-stu-id="bfe08-186">The following diagram shows the visual effect of applying a radial gradient brush to a rectangle that is filled with a bitmap of foliage.</span></span>

![diagrama de un mapa de bits de follaje con un pincel de degradado radial aplicado](images/brushes-ovw-radialgradient-opacitymask.png)

<span data-ttu-id="bfe08-188">En el primer ejemplo se crea un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), *m \_ pRadialFadeFlowersBitmapBrush*.</span><span class="sxs-lookup"><span data-stu-id="bfe08-188">The first example creates an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), *m\_pRadialFadeFlowersBitmapBrush*.</span></span> <span data-ttu-id="bfe08-189">Para que se pueda usar con una máscara de opacidad mediante el método [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) , el modo Extend x-e y-for *m \_ PRadialFadeFlowersBitmapBrush* se establecen en [**D2D1 \_ Extend \_ Mode \_ Clamp**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode).</span><span class="sxs-lookup"><span data-stu-id="bfe08-189">So that it can be used with an opacity mask by the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method, the extend mode x- and y- for *m\_pRadialFadeFlowersBitmapBrush* are set to [**D2D1\_EXTEND\_MODE\_CLAMP**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode).</span></span>


```C++
            if (SUCCEEDED(hr))
            {
                // Create the bitmap to be used by the bitmap brush.
                hr = LoadResourceBitmap(
                    m_pRenderTarget,
                    m_pWICFactory,
                    L"RadialFadeFlowers",
                    L"Image",
                    &m_pRadialFadeFlowersBitmap
                    );
            }


            if (SUCCEEDED(hr))
            {
                D2D1_BITMAP_BRUSH_PROPERTIES propertiesXClampYClamp = 
                    D2D1::BitmapBrushProperties(
                    D2D1_EXTEND_MODE_CLAMP,
                    D2D1_EXTEND_MODE_CLAMP,
                    D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR
                    );
```



<span codelanguage="ManagedCPlusPlus"></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bfe08-190">C++</span><span class="sxs-lookup"><span data-stu-id="bfe08-190">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>                if (SUCCEEDED(hr))
                {
                    hr = m_pRenderTarget->CreateBitmapBrush(
                        m_pLinearFadeFlowersBitmap,
                        propertiesXClampYClamp,
                        &m_pLinearFadeFlowersBitmapBrush
                        );
                }</code></pre></td>
</tr>
</tbody>
</table>

<span codelanguage="ManagedCPlusPlus"></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bfe08-191">C++</span><span class="sxs-lookup"><span data-stu-id="bfe08-191">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>            }</code></pre></td>
</tr>
</tbody>
</table>



<span data-ttu-id="bfe08-192">En el ejemplo siguiente se define el pincel de degradado radial que se usará como máscara de opacidad.</span><span class="sxs-lookup"><span data-stu-id="bfe08-192">The next example defines the radial gradient brush that will be used as the opacity mask.</span></span>


```C++
            if (SUCCEEDED(hr))
            {
                ID2D1GradientStopCollection *pGradientStops = NULL;

                static const D2D1_GRADIENT_STOP gradientStops[] =
                {
                    {   0.f,  D2D1::ColorF(D2D1::ColorF::Black, 1.0f)  },
                    {   1.f,  D2D1::ColorF(D2D1::ColorF::White, 0.0f)  },
                };

                hr = m_pRenderTarget->CreateGradientStopCollection(
                    gradientStops,
                    2,
                    &pGradientStops);




                if (SUCCEEDED(hr))
                {
                    hr = m_pRenderTarget->CreateRadialGradientBrush(
                        D2D1::RadialGradientBrushProperties(
                            D2D1::Point2F(75, 75),
                            D2D1::Point2F(0, 0),
                            75,
                            75),
                        pGradientStops,
                        &m_pRadialGradientBrush);
                }
                pGradientStops->Release();
            }
```





<span data-ttu-id="bfe08-193">En el ejemplo de código final se usa [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) (*m \_ pRadialFadeFlowersBitmapBrush*) y la máscara de opacidad (*m \_ PRadialGradientBrush*) para rellenar una [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) (*m \_ pRectGeo*).</span><span class="sxs-lookup"><span data-stu-id="bfe08-193">The final code example uses the [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) (*m\_pRadialFadeFlowersBitmapBrush*) and the opacity mask (*m\_pRadialGradientBrush*) to fill an [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) (*m\_pRectGeo*).</span></span>


```C++
        m_pRenderTarget->FillGeometry(
            m_pRectGeo,
            m_pRadialFadeFlowersBitmapBrush, 
            m_pRadialGradientBrush
            );
```



<span data-ttu-id="bfe08-194">El código se ha omitido en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="bfe08-194">Code has been omitted from this example.</span></span>

## <a name="apply-an-opacity-mask-to-a-layer"></a><span data-ttu-id="bfe08-195">Aplicar una máscara de opacidad a una capa</span><span class="sxs-lookup"><span data-stu-id="bfe08-195">Apply an Opacity Mask to a Layer</span></span>

<span data-ttu-id="bfe08-196">Al llamar a [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) para enviar un [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) a un destino de representación, puede usar la estructura de [**\_ \_ parámetros de capa D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) para aplicar un pincel como máscara de opacidad.</span><span class="sxs-lookup"><span data-stu-id="bfe08-196">When you call [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) to push an [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) onto an render target, you can use the [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structure to apply a brush as an opacity mask.</span></span> <span data-ttu-id="bfe08-197">En el ejemplo de código siguiente se usa un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) como máscara de opacidad.</span><span class="sxs-lookup"><span data-stu-id="bfe08-197">The following code example uses an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) as an opacity mask.</span></span>


```C++
HRESULT DemoApp::RenderWithLayerWithOpacityMask(ID2D1RenderTarget *pRT)
{   

    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 250));

        // Push the layer with the content bounds.
        pRT->PushLayer(
            D2D1::LayerParameters(
                D2D1::InfiniteRect(),
                NULL,
                D2D1_ANTIALIAS_MODE_PER_PRIMITIVE,
                D2D1::IdentityMatrix(),
                1.0,
                m_pRadialGradientBrush,
                D2D1_LAYER_OPTIONS_NONE),
            pLayer
            );

        pRT->DrawBitmap(m_pBambooBitmap, D2D1::RectF(0, 0, 190, 127));

        pRT->FillRectangle(
            D2D1::RectF(25.f, 25.f, 50.f, 50.f), 
            m_pSolidColorBrush
            );
        pRT->FillRectangle(
            D2D1::RectF(50.f, 50.f, 75.f, 75.f),
            m_pSolidColorBrush
            ); 
        pRT->FillRectangle(
            D2D1::RectF(75.f, 75.f, 100.f, 100.f),
            m_pSolidColorBrush
            );    
 
        pRT->PopLayer();
    }
    SafeRelease(&pLayer);
   
    return hr;
    
}
```



<span data-ttu-id="bfe08-198">Para obtener más información acerca del uso de capas, consulte la [información general sobre capas](direct2d-layers-overview.md).</span><span class="sxs-lookup"><span data-stu-id="bfe08-198">For more information about using layers, see the [Layers Overview](direct2d-layers-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bfe08-199">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bfe08-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bfe08-200">Información general sobre los pinceles</span><span class="sxs-lookup"><span data-stu-id="bfe08-200">Brushes Overview</span></span>](direct2d-brushes-overview.md)
</dt> <dt>

[<span data-ttu-id="bfe08-201">Información general sobre capas</span><span class="sxs-lookup"><span data-stu-id="bfe08-201">Layers Overview</span></span>](direct2d-layers-overview.md)
</dt> </dl>

 

 