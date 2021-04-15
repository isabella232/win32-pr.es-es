---
title: Efecto Desenfoque gaussiano
description: Use el efecto Desenfoque gaussiano para crear un desenfoque basado en la función gaussiano en toda la imagen de entrada.
ms.assetid: 6B8C9A0A-81D6-4CC2-B30B-995D4C2E59FC
keywords:
- Desenfoque gaussiano
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfbe8b309a498315e389be45d382eca3ee1b98ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104560581"
---
# <a name="gaussian-blur-effect"></a><span data-ttu-id="80f54-104">Efecto Desenfoque gaussiano</span><span class="sxs-lookup"><span data-stu-id="80f54-104">Gaussian blur effect</span></span>

<span data-ttu-id="80f54-105">Use el efecto Desenfoque gaussiano para crear un desenfoque basado en la función gaussiano en toda la imagen de entrada.</span><span class="sxs-lookup"><span data-stu-id="80f54-105">Use the Gaussian blur effect to create a blur based on the Gaussian function over the entire input image.</span></span>

<span data-ttu-id="80f54-106">Puede usar este efecto para crear iluminaciones y sombras paralelas y usar el efecto [compuesto](composite.md) para aplicar el resultado a la imagen original.</span><span class="sxs-lookup"><span data-stu-id="80f54-106">You can use this effect to create glows and drop shadows and use the [composite](composite.md) effect to apply the result to the original image.</span></span> <span data-ttu-id="80f54-107">Resulta útil en el procesamiento fotográfico para filtros como resaltados y sombras.</span><span class="sxs-lookup"><span data-stu-id="80f54-107">It is useful in photo processing for filters like highlights and shadows.</span></span> <span data-ttu-id="80f54-108">Puede usar la salida de este efecto para la entrada en efectos de iluminación, como la [iluminación especular](specular-lighting.md) o los efectos de [luz difusa](diffuse-lighting.md) , ya que el canal alfa está borroso, y los efectos de iluminación usan el canal alfa para determinar la geometría de la superficie como un mapa de alto.</span><span class="sxs-lookup"><span data-stu-id="80f54-108">You can use the output of this effect for input into lighting effects, like the [Specular Lighting](specular-lighting.md) or [Diffuse Lighting](diffuse-lighting.md) effects, because the alpha channel is blurred, too and lighting effects use the alpha channel to determine surface geometry as a height map.</span></span>

<span data-ttu-id="80f54-109">Este efecto lo usa el efecto de [sombra](drop-shadow.md) integrado.</span><span class="sxs-lookup"><span data-stu-id="80f54-109">This effect is used by the built-in [Shadow](drop-shadow.md) effect.</span></span>

<span data-ttu-id="80f54-110">El CLSID para este efecto es CLSID \_ D2D1GaussianBlur.</span><span class="sxs-lookup"><span data-stu-id="80f54-110">The CLSID for this effect is CLSID\_D2D1GaussianBlur.</span></span>

-   [<span data-ttu-id="80f54-111">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="80f54-111">Example image</span></span>](#example-image)
-   [<span data-ttu-id="80f54-112">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="80f54-112">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="80f54-113">Modos de optimización</span><span class="sxs-lookup"><span data-stu-id="80f54-113">Optimization modes</span></span>](#optimization-modes)
-   [<span data-ttu-id="80f54-114">Modos de borde</span><span class="sxs-lookup"><span data-stu-id="80f54-114">Border modes</span></span>](#border-modes)
-   [<span data-ttu-id="80f54-115">Mapa de bits de salida</span><span class="sxs-lookup"><span data-stu-id="80f54-115">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="80f54-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80f54-116">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="80f54-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="80f54-117">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="80f54-118">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="80f54-118">Example image</span></span>



| <span data-ttu-id="80f54-119">Antes</span><span class="sxs-lookup"><span data-stu-id="80f54-119">Before</span></span>                                                       |
|--------------------------------------------------------------|
| ![imagen anterior al efecto.](images/default-before.jpg)   |
| <span data-ttu-id="80f54-121">Después</span><span class="sxs-lookup"><span data-stu-id="80f54-121">After</span></span>                                                        |
| ![la imagen después de la transformación.](images/1-gaussianblur.png) |



 


```C++
ComPtr<ID2D1Effect> gaussianBlurEffect;
m_d2dContext->CreateEffect(CLSID_D2D1GaussianBlur, &gaussianBlurEffect);

gaussianBlurEffect->SetInput(0, bitmap);
gaussianBlurEffect->SetValue(D2D1_GAUSSIANBLUR_PROP_STANDARD_DEVIATION, 3.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(gaussianBlurEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="80f54-123">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="80f54-123">Effect properties</span></span>



| <span data-ttu-id="80f54-124">Enumeración de índice y nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="80f54-124">Display name and index enumeration</span></span>                                                    | <span data-ttu-id="80f54-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="80f54-125">Description</span></span>                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80f54-126">StandardDeviation</span><span class="sxs-lookup"><span data-stu-id="80f54-126">StandardDeviation</span></span><br/> <span data-ttu-id="80f54-127">\_ \_ \_ Desviación estándar de la D2D1 GAUSSIANBLUR \_</span><span class="sxs-lookup"><span data-stu-id="80f54-127">D2D1\_GAUSSIANBLUR\_PROP\_STANDARD\_DEVIATION</span></span><br/> | <span data-ttu-id="80f54-128">Cantidad de desenfoque que se va a aplicar a la imagen.</span><span class="sxs-lookup"><span data-stu-id="80f54-128">The amount of blur to be applied to the image.</span></span> <span data-ttu-id="80f54-129">Puede calcular el radio de desenfoque del kernel multiplicando la desviación estándar por 3.</span><span class="sxs-lookup"><span data-stu-id="80f54-129">You can compute the blur radius of the kernel by multiplying the standard deviation by 3.</span></span> <span data-ttu-id="80f54-130">Las unidades de la desviación estándar y el radio de desenfoque son DIP.</span><span class="sxs-lookup"><span data-stu-id="80f54-130">The units of both the standard deviation and blur radius are DIPs.</span></span> <span data-ttu-id="80f54-131">Un valor de cero DIP deshabilita este efecto por completo.</span><span class="sxs-lookup"><span data-stu-id="80f54-131">A value of zero DIPs disables this effect entirely.</span></span> <span data-ttu-id="80f54-132">El tipo es FLOAT.</span><span class="sxs-lookup"><span data-stu-id="80f54-132">The type is FLOAT.</span></span><br/> <span data-ttu-id="80f54-133">El valor predeterminado es 3.0 f.</span><span class="sxs-lookup"><span data-stu-id="80f54-133">The default value is 3.0f.</span></span><br/> |
| <span data-ttu-id="80f54-134">Optimization</span><span class="sxs-lookup"><span data-stu-id="80f54-134">Optimization</span></span><br/> <span data-ttu-id="80f54-135">Optimización de D2D1 \_ GAUSSIANBLUR \_ \_</span><span class="sxs-lookup"><span data-stu-id="80f54-135">D2D1\_GAUSSIANBLUR\_PROP\_OPTIMIZATION</span></span><br/>             | <span data-ttu-id="80f54-136">Modo de optimización.</span><span class="sxs-lookup"><span data-stu-id="80f54-136">The optimization mode.</span></span> <span data-ttu-id="80f54-137">Vea [modos de optimización](#optimization-modes) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="80f54-137">See [Optimization modes](#optimization-modes) for more info.</span></span> <span data-ttu-id="80f54-138">El tipo es D2D1 \_ GAUSSIANBLUR \_ Optimization.</span><span class="sxs-lookup"><span data-stu-id="80f54-138">The type is D2D1\_GAUSSIANBLUR\_OPTIMIZATION.</span></span><br/> <span data-ttu-id="80f54-139">El valor predeterminado es D2D1 \_ GAUSSIANBLUR \_ optimizado de optimización \_ .</span><span class="sxs-lookup"><span data-stu-id="80f54-139">The default value is D2D1\_GAUSSIANBLUR\_OPTIMIZATION\_BALANCED.</span></span><br/>                                                                                                            |
| <span data-ttu-id="80f54-140">BorderMode</span><span class="sxs-lookup"><span data-stu-id="80f54-140">BorderMode</span></span><br/> <span data-ttu-id="80f54-141">D2D1 \_ GAUSSIANBLUR \_ \_ modo de borde \_ de la Prop</span><span class="sxs-lookup"><span data-stu-id="80f54-141">D2D1\_GAUSSIANBLUR\_PROP\_BORDER\_MODE</span></span><br/>               | <span data-ttu-id="80f54-142">El modo que se usa para calcular el borde de la imagen, es decir, es flexible o difícil.</span><span class="sxs-lookup"><span data-stu-id="80f54-142">The mode used to calculate the border of the image, soft or hard.</span></span> <span data-ttu-id="80f54-143">Vea [modos de borde](#border-modes) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="80f54-143">See [Border modes](#border-modes) for more info.</span></span> <br/> <span data-ttu-id="80f54-144">El tipo es D2D1 \_ GAUSSIANBLUR \_ Border \_ mode.</span><span class="sxs-lookup"><span data-stu-id="80f54-144">The type is D2D1\_GAUSSIANBLUR\_BORDER\_MODE.</span></span><br/> <span data-ttu-id="80f54-145">El valor predeterminado es D2D1 \_ Border \_ Mode \_ .</span><span class="sxs-lookup"><span data-stu-id="80f54-145">The default value is D2D1\_BORDER\_MODE\_SOFT.</span></span><br/>                                                                                   |



 

## <a name="optimization-modes"></a><span data-ttu-id="80f54-146">Modos de optimización</span><span class="sxs-lookup"><span data-stu-id="80f54-146">Optimization modes</span></span>



| <span data-ttu-id="80f54-147">Nombre</span><span class="sxs-lookup"><span data-stu-id="80f54-147">Name</span></span>                                          | <span data-ttu-id="80f54-148">Descripción</span><span class="sxs-lookup"><span data-stu-id="80f54-148">Description</span></span>                                                                                                                           |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80f54-149">Velocidad de optimización de D2D1 \_ DIRECTIONALBLUR \_ \_</span><span class="sxs-lookup"><span data-stu-id="80f54-149">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_SPEED</span></span>    | <span data-ttu-id="80f54-150">Aplica las optimizaciones internas, como el escalado previo en radios relativamente pequeños.</span><span class="sxs-lookup"><span data-stu-id="80f54-150">Applies internal optimizations such as pre-scaling at relatively small radii.</span></span> <span data-ttu-id="80f54-151">Utiliza el filtrado lineal.</span><span class="sxs-lookup"><span data-stu-id="80f54-151">Uses linear filtering.</span></span>                                  |
| <span data-ttu-id="80f54-152">Optimización de D2D1 \_ DIRECTIONALBLUR \_ \_ equilibrada</span><span class="sxs-lookup"><span data-stu-id="80f54-152">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_BALANCED</span></span> | <span data-ttu-id="80f54-153">Usa los mismos umbrales de optimización que el modo de velocidad, pero utiliza el filtrado trilineal.</span><span class="sxs-lookup"><span data-stu-id="80f54-153">Uses the same optimization thresholds as Speed mode, but uses trilinear filtering.</span></span>                                                    |
| <span data-ttu-id="80f54-154">Calidad de optimización de D2D1 \_ DIRECTIONALBLUR \_ \_</span><span class="sxs-lookup"><span data-stu-id="80f54-154">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_QUALITY</span></span>  | <span data-ttu-id="80f54-155">Solo usa optimizaciones internas con radios de desenfoque grandes, donde es menos probable que las aproximaciones sean visibles.</span><span class="sxs-lookup"><span data-stu-id="80f54-155">Only uses internal optimizations with large blur radii, where approximations are less likely to be visible.</span></span> <span data-ttu-id="80f54-156">Utiliza el filtrado trilineal.</span><span class="sxs-lookup"><span data-stu-id="80f54-156">Uses trilinear filtering.</span></span> |



 

## <a name="border-modes"></a><span data-ttu-id="80f54-157">Modos de borde</span><span class="sxs-lookup"><span data-stu-id="80f54-157">Border modes</span></span>



| <span data-ttu-id="80f54-158">Nombre</span><span class="sxs-lookup"><span data-stu-id="80f54-158">Name</span></span>                     | <span data-ttu-id="80f54-159">Descripción</span><span class="sxs-lookup"><span data-stu-id="80f54-159">Description</span></span>                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80f54-160">D2D1 \_ modo de borde \_ \_ flexible</span><span class="sxs-lookup"><span data-stu-id="80f54-160">D2D1\_BORDER\_MODE\_SOFT</span></span> | <span data-ttu-id="80f54-161">El efecto rellena la imagen con píxeles negros transparentes cuando aplica el kernel de desenfoque, lo que da lugar a un borde flexible.</span><span class="sxs-lookup"><span data-stu-id="80f54-161">The effect pads the image with transparent black pixels as it applies the blur kernel, resulting in a soft edge.</span></span> <br/>                                                                                             |
| <span data-ttu-id="80f54-162">D2D1 \_ del \_ modo de borde \_</span><span class="sxs-lookup"><span data-stu-id="80f54-162">D2D1\_BORDER\_MODE\_HARD</span></span> | <span data-ttu-id="80f54-163">El efecto fija la salida al tamaño de la imagen de entrada.</span><span class="sxs-lookup"><span data-stu-id="80f54-163">The effect clamps the output to the size of the input image.</span></span> <span data-ttu-id="80f54-164">Cuando el efecto aplica el kernel de desenfoque, extiende la imagen de entrada con una transformación de borde de tipo de reflejo para las muestras fuera de los límites de entrada.</span><span class="sxs-lookup"><span data-stu-id="80f54-164">When the effect applies the blur kernel, it extends the input image with a mirror-type border transform for samples outside of the input bounds.</span></span><br/> |



 

## <a name="output-bitmap"></a><span data-ttu-id="80f54-165">Mapa de bits de salida</span><span class="sxs-lookup"><span data-stu-id="80f54-165">Output bitmap</span></span>

<span data-ttu-id="80f54-166">La salida de este efecto puede ser mayor que el mapa de bits de entrada basado en el radio de desenfoque y el modo de borde.</span><span class="sxs-lookup"><span data-stu-id="80f54-166">The output of this effect can be larger than the input bitmap based on the blur radius and the border mode.</span></span> <span data-ttu-id="80f54-167">Si el modo de borde se establece en el \_ modo de borde D2D1 \_ \_ , aumenta el tamaño del mapa de bits de salida en función del tamaño del kernel de desenfoque, representado en píxeles.</span><span class="sxs-lookup"><span data-stu-id="80f54-167">If the border mode is set to D2D1\_BORDER\_MODE\_SOFT the s ize of the output bitmap increases by the size of the blur kernel, represented in pixels.</span></span> <span data-ttu-id="80f54-168">En esta tabla se proporciona una ecuación que se puede usar para calcular el mapa de bits de salida.</span><span class="sxs-lookup"><span data-stu-id="80f54-168">This table provides an equation that you can use to compute the output bitmap.</span></span>

`Output bitmap growth (X and Y) = StandardDeviation  (DIPs)*6*((User DPI)/96)`

<span data-ttu-id="80f54-169">Por lo tanto, si el tamaño de la imagen aumenta en 10 píxeles en cada dirección, la esquina superior izquierda de la imagen se ubicará en (-5,-5), mientras que la parte inferior derecha estará en (105, 105).</span><span class="sxs-lookup"><span data-stu-id="80f54-169">So, if the image size increases by 10 pixels in each direction the upper left corner of the image will be located at (-5, -5) while the lower right will be at (105, 105).</span></span>

## <a name="requirements"></a><span data-ttu-id="80f54-170">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80f54-170">Requirements</span></span>



| <span data-ttu-id="80f54-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="80f54-171">Requirement</span></span> | <span data-ttu-id="80f54-172">Value</span><span class="sxs-lookup"><span data-stu-id="80f54-172">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="80f54-173">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="80f54-173">Minimum supported client</span></span> | <span data-ttu-id="80f54-174">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="80f54-174">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="80f54-175">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="80f54-175">Minimum supported server</span></span> | <span data-ttu-id="80f54-176">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="80f54-176">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="80f54-177">Encabezado</span><span class="sxs-lookup"><span data-stu-id="80f54-177">Header</span></span>                   | <span data-ttu-id="80f54-178">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="80f54-178">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="80f54-179">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="80f54-179">Library</span></span>                  | <span data-ttu-id="80f54-180">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="80f54-180">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="80f54-181">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="80f54-181">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80f54-182">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="80f54-182">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

