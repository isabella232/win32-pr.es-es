---
title: Efecto de sombra
description: Use el efecto de sombra para generar una sombra a partir del canal alfa de una imagen.
ms.assetid: 53525584-10CF-46C2-9400-C4FB225D4693
keywords:
- efecto de sombra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c42fd8755078dd79f2b01b623b1839785beb3c3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359680"
---
# <a name="shadow-effect"></a><span data-ttu-id="e3f4c-104">Efecto de sombra</span><span class="sxs-lookup"><span data-stu-id="e3f4c-104">Shadow effect</span></span>

<span data-ttu-id="e3f4c-105">Use el efecto de sombra para generar una sombra a partir del canal alfa de una imagen.</span><span class="sxs-lookup"><span data-stu-id="e3f4c-105">Use the shadow effect to generate a shadow from the alpha channel of an image.</span></span> <span data-ttu-id="e3f4c-106">La sombra es más opaca para los valores alfa más altos y más transparente para los valores alfa más bajos.</span><span class="sxs-lookup"><span data-stu-id="e3f4c-106">The shadow is more opaque for higher alpha values and more transparent for lower alpha values.</span></span> <span data-ttu-id="e3f4c-107">Puede establecer la cantidad de desenfoque y el color de la sombra.</span><span class="sxs-lookup"><span data-stu-id="e3f4c-107">You can set the amount of blur and the color of the shadow.</span></span>

-   [<span data-ttu-id="e3f4c-108">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="e3f4c-108">Example image</span></span>](#example-image)
-   [<span data-ttu-id="e3f4c-109">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="e3f4c-109">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="e3f4c-110">Modos de optimización</span><span class="sxs-lookup"><span data-stu-id="e3f4c-110">Optimization modes</span></span>](#optimization-modes)
-   [<span data-ttu-id="e3f4c-111">Mapa de bits de salida</span><span class="sxs-lookup"><span data-stu-id="e3f4c-111">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="e3f4c-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3f4c-112">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="e3f4c-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e3f4c-113">Related topics</span></span>](#related-topics)

<span data-ttu-id="e3f4c-114">El CLSID para este efecto es CLSID \_ D2D1Shadow.</span><span class="sxs-lookup"><span data-stu-id="e3f4c-114">The CLSID for this effect is CLSID\_D2D1Shadow.</span></span>

## <a name="example-image"></a><span data-ttu-id="e3f4c-115">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="e3f4c-115">Example image</span></span>

<span data-ttu-id="e3f4c-116">En el ejemplo siguiente se muestra la salida del efecto de sombra que se traslada hacia abajo y hacia la derecha con la imagen de origen compuesta en la ubicación original.</span><span class="sxs-lookup"><span data-stu-id="e3f4c-116">The example here shows the output of the shadow effect translated down and right with the source image composited over it in the original location.</span></span> <span data-ttu-id="e3f4c-117">El efecto de sombra solo produce la sombra.</span><span class="sxs-lookup"><span data-stu-id="e3f4c-117">The shadow effect only outputs the shadow.</span></span>



| <span data-ttu-id="e3f4c-118">Antes</span><span class="sxs-lookup"><span data-stu-id="e3f4c-118">Before</span></span>                                                  |
|---------------------------------------------------------|
| ![imagen anterior al efecto.](images/8-crop.png)      |
| <span data-ttu-id="e3f4c-120">Después</span><span class="sxs-lookup"><span data-stu-id="e3f4c-120">After</span></span>                                                   |
| ![la imagen después de la transformación.](images/25-shadow.png) |



 


```C++
ComPtr<ID2D1Effect> shadowEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Shadow, &shadowEffect);

shadowEffect->SetInput(0, bitmap);

// Shadow is composited on top of a white surface to show opacity.
ComPtr<ID2D1Effect> floodEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Flood, &floodEffect);

floodEffect->SetValue(D2D1_FLOOD_PROP_COLOR, D2D1::Vector4F(1.0f, 1.0f, 1.0f, 1.0f));

ComPtr<ID2D1Effect> affineTransformEffect;
m_d2dContext->CreateEffect(CLSID_D2D12DAffineTransform, &affineTransformEffect);

affineTransformEffect->SetInputEffect(0, shadowEffect.Get());

D2D1_MATRIX_3X2_F matrix = D2D1::Matrix3x2F::Translation(20, 20));

affineTransformEffect->SetValue(D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX, matrix);

ComPtr<ID2D1Effect> compositeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect);

compositeEffect->SetInputEffect(0, floodEffect.Get());
compositeEffect->SetInputEffect(1, affineTransformEffect.Get());
compositeEffect->SetInput(2, bitmap);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="e3f4c-122">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="e3f4c-122">Effect properties</span></span>



| <span data-ttu-id="e3f4c-123">Enumeración de índice y nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="e3f4c-123">Display name and index enumeration</span></span>                                                        | <span data-ttu-id="e3f4c-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3f4c-124">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3f4c-125">BlurStandardDeviation</span><span class="sxs-lookup"><span data-stu-id="e3f4c-125">BlurStandardDeviation</span></span><br/> <span data-ttu-id="e3f4c-126">\_ \_ \_ Desviación estándar de desenfoque de \_ la instantánea D2D1 \_</span><span class="sxs-lookup"><span data-stu-id="e3f4c-126">D2D1\_SHADOW\_PROP\_BLUR\_STANDARD\_DEVIATION</span></span><br/> | <span data-ttu-id="e3f4c-127">Cantidad de desenfoque que se va a aplicar al canal alfa de la imagen.</span><span class="sxs-lookup"><span data-stu-id="e3f4c-127">The amount of blur to be applied to the alpha channel of the image.</span></span> <span data-ttu-id="e3f4c-128">Puede calcular el radio de desenfoque del kernel multiplicando la desviación estándar por 3.</span><span class="sxs-lookup"><span data-stu-id="e3f4c-128">You can compute the blur radius of the kernel by multiplying the standard deviation by 3.</span></span> <span data-ttu-id="e3f4c-129">Las unidades de la desviación estándar y el radio de desenfoque son DIP.</span><span class="sxs-lookup"><span data-stu-id="e3f4c-129">The units of both the standard deviation and blur radius are DIPs.</span></span><br/> <span data-ttu-id="e3f4c-130">Esta propiedad es igual que la propiedad [desenfoque gausiano](gaussian-blur.md) desviación estándar.</span><span class="sxs-lookup"><span data-stu-id="e3f4c-130">This property is the same as the [Gaussian Blur](gaussian-blur.md) standard deviation property.</span></span> <br/> <span data-ttu-id="e3f4c-131">El tipo es FLOAT.</span><span class="sxs-lookup"><span data-stu-id="e3f4c-131">The type is FLOAT.</span></span><br/> <span data-ttu-id="e3f4c-132">El valor predeterminado es 3.0 f.</span><span class="sxs-lookup"><span data-stu-id="e3f4c-132">The default value is 3.0f.</span></span><br/> |
| <span data-ttu-id="e3f4c-133">Color</span><span class="sxs-lookup"><span data-stu-id="e3f4c-133">Color</span></span><br/> <span data-ttu-id="e3f4c-134">COLOR de la instantánea de D2D1 \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="e3f4c-134">D2D1\_SHADOW\_PROP\_COLOR</span></span><br/>                                     | <span data-ttu-id="e3f4c-135">Color de la sombra paralela.</span><span class="sxs-lookup"><span data-stu-id="e3f4c-135">The color of the drop shadow.</span></span> <span data-ttu-id="e3f4c-136">Esta propiedad es un D2D1 \_ Vector \_ 4F definido como: (R, G, B, a).</span><span class="sxs-lookup"><span data-stu-id="e3f4c-136">This property is a D2D1\_VECTOR\_4F defined as: (R, G, B, A).</span></span> <span data-ttu-id="e3f4c-137">Debe especificar este color en alfa recto.</span><span class="sxs-lookup"><span data-stu-id="e3f4c-137">You must specify this color in straight alpha.</span></span><br/> <span data-ttu-id="e3f4c-138">El tipo es D2D1 \_ Vector \_ 4F.</span><span class="sxs-lookup"><span data-stu-id="e3f4c-138">The type is D2D1\_VECTOR\_4F.</span></span><br/> <span data-ttu-id="e3f4c-139">El valor predeterminado es {0.0 f, 0.0 f, 0.0 f, 1.0 f.</span><span class="sxs-lookup"><span data-stu-id="e3f4c-139">The default value is {0.0f, 0.0f, 0.0f, 1.0f}.</span></span><br/>                                                                                                                                                                     |
| <span data-ttu-id="e3f4c-140">Optimization</span><span class="sxs-lookup"><span data-stu-id="e3f4c-140">Optimization</span></span><br/> <span data-ttu-id="e3f4c-141">Optimización de D2D1 \_ Shadow \_ prop \_</span><span class="sxs-lookup"><span data-stu-id="e3f4c-141">D2D1\_SHADOW\_PROP\_OPTIMIZATION</span></span><br/>                       | <span data-ttu-id="e3f4c-142">Nivel de optimización del rendimiento.</span><span class="sxs-lookup"><span data-stu-id="e3f4c-142">The level of performance optimization.</span></span><br/> <span data-ttu-id="e3f4c-143">El tipo es D2D1 \_ Shadow \_ Optimization.</span><span class="sxs-lookup"><span data-stu-id="e3f4c-143">The type is D2D1\_SHADOW\_OPTIMIZATION.</span></span><br/> <span data-ttu-id="e3f4c-144">El valor predeterminado es D2D1 \_ Shadow \_ Optimization \_ .</span><span class="sxs-lookup"><span data-stu-id="e3f4c-144">The default value is D2D1\_SHADOW\_OPTIMIZATION\_BALANCED.</span></span><br/>                                                                                                                                                                                                                                                   |



 

## <a name="optimization-modes"></a><span data-ttu-id="e3f4c-145">Modos de optimización</span><span class="sxs-lookup"><span data-stu-id="e3f4c-145">Optimization modes</span></span>



| <span data-ttu-id="e3f4c-146">Nombre</span><span class="sxs-lookup"><span data-stu-id="e3f4c-146">Name</span></span>                                          | <span data-ttu-id="e3f4c-147">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3f4c-147">Description</span></span>                                                                                                                           |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3f4c-148">Velocidad de optimización de D2D1 \_ DIRECTIONALBLUR \_ \_</span><span class="sxs-lookup"><span data-stu-id="e3f4c-148">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_SPEED</span></span>    | <span data-ttu-id="e3f4c-149">Aplica las optimizaciones internas, como el escalado previo en radios relativamente pequeños.</span><span class="sxs-lookup"><span data-stu-id="e3f4c-149">Applies internal optimizations such as pre-scaling at relatively small radii.</span></span> <span data-ttu-id="e3f4c-150">Utiliza el filtrado lineal.</span><span class="sxs-lookup"><span data-stu-id="e3f4c-150">Uses linear filtering.</span></span>                                  |
| <span data-ttu-id="e3f4c-151">Optimización de D2D1 \_ DIRECTIONALBLUR \_ \_ equilibrada</span><span class="sxs-lookup"><span data-stu-id="e3f4c-151">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_BALANCED</span></span> | <span data-ttu-id="e3f4c-152">Usa los mismos umbrales de optimización que el modo de velocidad, pero utiliza el filtrado trilineal.</span><span class="sxs-lookup"><span data-stu-id="e3f4c-152">Uses the same optimization thresholds as Speed mode, but uses trilinear filtering.</span></span>                                                    |
| <span data-ttu-id="e3f4c-153">Calidad de optimización de D2D1 \_ DIRECTIONALBLUR \_ \_</span><span class="sxs-lookup"><span data-stu-id="e3f4c-153">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_QUALITY</span></span>  | <span data-ttu-id="e3f4c-154">Solo usa optimizaciones internas con radios de desenfoque grandes, donde es menos probable que las aproximaciones sean visibles.</span><span class="sxs-lookup"><span data-stu-id="e3f4c-154">Only uses internal optimizations with large blur radii, where approximations are less likely to be visible.</span></span> <span data-ttu-id="e3f4c-155">Utiliza el filtrado trilineal.</span><span class="sxs-lookup"><span data-stu-id="e3f4c-155">Uses trilinear filtering.</span></span> |



 

## <a name="output-bitmap"></a><span data-ttu-id="e3f4c-156">Mapa de bits de salida</span><span class="sxs-lookup"><span data-stu-id="e3f4c-156">Output bitmap</span></span>

<span data-ttu-id="e3f4c-157">El tamaño del mapa de bits de salida es el tamaño de la salida de desenfoque.</span><span class="sxs-lookup"><span data-stu-id="e3f4c-157">The size of the output bitmap is the size of the blur output.</span></span> <span data-ttu-id="e3f4c-158">La cantidad de crecimiento del mapa de bits de salida en relación con el mapa de bits original se puede calcular mediante la siguiente ecuación:</span><span class="sxs-lookup"><span data-stu-id="e3f4c-158">The amount the output bitmap growth relative to the original bitmap can be calculated using the following equation:</span></span>

<span data-ttu-id="e3f4c-159">Crecimiento del mapa de bits de salida (X e y) = BlurStandardDeviation (píxeles independientes del dispositivo (DIP)) \* 6 \* (PPP del usuario)/96</span><span class="sxs-lookup"><span data-stu-id="e3f4c-159">Output Bitmap Growth (X and Y) = BlurStandardDeviation (device-independent pixels (DIPs))\*6\*(User DPI)/96</span></span>

<span data-ttu-id="e3f4c-160">El resultado aumenta igualmente en todas las direcciones, por lo que, por ejemplo, si el tamaño aumenta en 10 píxeles en cada dirección, la esquina superior izquierda del mapa de bits se encuentra en (-5,-5) y la parte inferior derecha estará en (105, 105), tal y como se muestra en el diagrama aquí.</span><span class="sxs-lookup"><span data-stu-id="e3f4c-160">The output increases equally in all direction, so for example if the size increases by 10 pixels in each direction, the upper left corner of the bitmap is located at (-5, -5) and the lower right will be at (105, 105) as shown in the diagram here.</span></span>

![diagrama de crecimiento del tamaño de salida de efecto de sombra.](images/drop-shadow-output-growth.png)

## <a name="requirements"></a><span data-ttu-id="e3f4c-162">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3f4c-162">Requirements</span></span>



| <span data-ttu-id="e3f4c-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3f4c-163">Requirement</span></span> | <span data-ttu-id="e3f4c-164">Value</span><span class="sxs-lookup"><span data-stu-id="e3f4c-164">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e3f4c-165">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3f4c-165">Minimum supported client</span></span> | <span data-ttu-id="e3f4c-166">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="e3f4c-166">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="e3f4c-167">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3f4c-167">Minimum supported server</span></span> | <span data-ttu-id="e3f4c-168">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="e3f4c-168">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="e3f4c-169">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e3f4c-169">Header</span></span>                   | <span data-ttu-id="e3f4c-170">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="e3f4c-170">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="e3f4c-171">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e3f4c-171">Library</span></span>                  | <span data-ttu-id="e3f4c-172">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="e3f4c-172">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="e3f4c-173">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e3f4c-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3f4c-174">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="e3f4c-174">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

