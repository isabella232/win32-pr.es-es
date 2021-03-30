---
title: Efecto de Desenfoque direccional
description: El efecto de Desenfoque direccional es similar al desenfoque gaussiano, salvo que puede sesgar el desenfoque en una dirección determinada.
ms.assetid: 59328FA4-5C27-4A81-AAB2-C5B25B3615C6
keywords:
- Desenfoque direccional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0e1c098d17929563cf69f4e61416fa0d93a88dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801040"
---
# <a name="directional-blur-effect"></a><span data-ttu-id="88dc1-104">Efecto de Desenfoque direccional</span><span class="sxs-lookup"><span data-stu-id="88dc1-104">Directional blur effect</span></span>

<span data-ttu-id="88dc1-105">El efecto de Desenfoque direccional es similar al [Desenfoque gaussiano](gaussian-blur.md), salvo que puede sesgar el desenfoque en una dirección determinada.</span><span class="sxs-lookup"><span data-stu-id="88dc1-105">The directional blur effect is similar to [Gaussian blur](gaussian-blur.md), except you can skew the blur in a particular direction.</span></span> <span data-ttu-id="88dc1-106">Puede usar este efecto para que una imagen tenga un aspecto como si estuviera en movimiento o para resaltar una imagen animada.</span><span class="sxs-lookup"><span data-stu-id="88dc1-106">You can use this effect to make an image look as if it is in motion or to emphasize an animated image.</span></span>

<span data-ttu-id="88dc1-107">El CLSID para este efecto es CLSID \_ D2D1DirectionalBlur.</span><span class="sxs-lookup"><span data-stu-id="88dc1-107">The CLSID for this effect is CLSID\_D2D1DirectionalBlur.</span></span>

-   [<span data-ttu-id="88dc1-108">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="88dc1-108">Example image</span></span>](#example-image)
-   [<span data-ttu-id="88dc1-109">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="88dc1-109">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="88dc1-110">Modos de optimización</span><span class="sxs-lookup"><span data-stu-id="88dc1-110">Optimization modes</span></span>](#optimization-modes)
-   [<span data-ttu-id="88dc1-111">Modos de borde</span><span class="sxs-lookup"><span data-stu-id="88dc1-111">Border modes</span></span>](#border-modes)
-   [<span data-ttu-id="88dc1-112">Mapa de bits de salida</span><span class="sxs-lookup"><span data-stu-id="88dc1-112">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="88dc1-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88dc1-113">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="88dc1-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="88dc1-114">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="88dc1-115">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="88dc1-115">Example image</span></span>



| <span data-ttu-id="88dc1-116">Antes</span><span class="sxs-lookup"><span data-stu-id="88dc1-116">Before</span></span>                                                          |
|-----------------------------------------------------------------|
| ![imagen anterior al efecto.](images/default-before.jpg)      |
| <span data-ttu-id="88dc1-118">Después</span><span class="sxs-lookup"><span data-stu-id="88dc1-118">After</span></span>                                                           |
| ![la imagen después de la transformación.](images/2-directionalblur.png) |



 


```C++
ComPtr<ID2D1Effect> directionalBlurEffect;
m_d2dContext->CreateEffect(CLSID_D2D1DirectionalBlur, &directionalBlurEffect);

directionalBlurEffect->SetInput(0, bitmap);
directionalBlurEffect->SetValue(D2D1_DIRECTIONALBLUR_PROP_STANDARD_DEVIATION, 7.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(directionalBlurEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="88dc1-120">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="88dc1-120">Effect properties</span></span>



| <span data-ttu-id="88dc1-121">Enumeración de índice y nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="88dc1-121">Display name and index enumeration</span></span>                                                       | <span data-ttu-id="88dc1-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="88dc1-122">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88dc1-123">StandardDeviation</span><span class="sxs-lookup"><span data-stu-id="88dc1-123">StandardDeviation</span></span><br/> <span data-ttu-id="88dc1-124">\_ \_ \_ Desviación estándar de la D2D1 DIRECTIONALBLUR \_</span><span class="sxs-lookup"><span data-stu-id="88dc1-124">D2D1\_DIRECTIONALBLUR\_PROP\_STANDARD\_DEVIATION</span></span><br/> | <span data-ttu-id="88dc1-125">Cantidad de desenfoque que se va a aplicar a la imagen.</span><span class="sxs-lookup"><span data-stu-id="88dc1-125">The amount of blur to be applied to the image.</span></span> <span data-ttu-id="88dc1-126">Puede calcular el radio de desenfoque del kernel multiplicando la desviación estándar por 3.</span><span class="sxs-lookup"><span data-stu-id="88dc1-126">You can compute the blur radius of the kernel by multiplying the standard deviation by 3.</span></span> <span data-ttu-id="88dc1-127">Las unidades de la desviación estándar y el radio de desenfoque son DIP.</span><span class="sxs-lookup"><span data-stu-id="88dc1-127">The units of both the standard deviation and blur radius are DIPs.</span></span> <span data-ttu-id="88dc1-128">Un valor de 0 DIP deshabilita este efecto.</span><span class="sxs-lookup"><span data-stu-id="88dc1-128">A value of 0 DIPs disables this effect.</span></span> <span data-ttu-id="88dc1-129">El tipo es FLOAT.</span><span class="sxs-lookup"><span data-stu-id="88dc1-129">The type is FLOAT.</span></span><br/> <span data-ttu-id="88dc1-130">El valor predeterminado es 3.0 f.</span><span class="sxs-lookup"><span data-stu-id="88dc1-130">The default value is 3.0f.</span></span><br/>                                                                            |
| <span data-ttu-id="88dc1-131">Ángulo</span><span class="sxs-lookup"><span data-stu-id="88dc1-131">Angle</span></span><br/> <span data-ttu-id="88dc1-132">Ángulo de la D2D1 \_ DIRECTIONALBLUR \_ \_</span><span class="sxs-lookup"><span data-stu-id="88dc1-132">D2D1\_DIRECTIONALBLUR\_PROP\_ANGLE</span></span><br/>                           | <span data-ttu-id="88dc1-133">Ángulo del desenfoque con respecto al eje x, en sentido contrario a las agujas del reloj.</span><span class="sxs-lookup"><span data-stu-id="88dc1-133">The angle of the blur relative to the x-axis, in the counterclockwise direction.</span></span> <span data-ttu-id="88dc1-134">Las unidades se especifican en grados.</span><span class="sxs-lookup"><span data-stu-id="88dc1-134">The units are specified in degrees.</span></span><br/> <span data-ttu-id="88dc1-135">El kernel de desenfoque se genera primero mediante el mismo proceso que para el efecto [Desenfoque gaussiano](gaussian-blur.md) .</span><span class="sxs-lookup"><span data-stu-id="88dc1-135">The blur kernel is first generated using the same process as for the [Gaussian blur](gaussian-blur.md) effect.</span></span> <span data-ttu-id="88dc1-136">Después, los valores de kernel se transforman según el ángulo de desenfoque.</span><span class="sxs-lookup"><span data-stu-id="88dc1-136">The kernel values are then transformed according to the blur angle.</span></span><br/> <span data-ttu-id="88dc1-137">El tipo es FLOAT.</span><span class="sxs-lookup"><span data-stu-id="88dc1-137">The type is FLOAT.</span></span><br/> <span data-ttu-id="88dc1-138">El valor predeterminado es 0.0 f.</span><span class="sxs-lookup"><span data-stu-id="88dc1-138">The default value is 0.0f.</span></span><br/> |
| <span data-ttu-id="88dc1-139">Optimization</span><span class="sxs-lookup"><span data-stu-id="88dc1-139">Optimization</span></span><br/> <span data-ttu-id="88dc1-140">Optimización de D2D1 \_ DIRECTIONALBLUR \_ \_</span><span class="sxs-lookup"><span data-stu-id="88dc1-140">D2D1\_DIRECTIONALBLUR\_PROP\_OPTIMIZATION</span></span><br/>             | <span data-ttu-id="88dc1-141">Modo de optimización.</span><span class="sxs-lookup"><span data-stu-id="88dc1-141">The optimization mode.</span></span> <span data-ttu-id="88dc1-142">Vea [modos de optimización](#optimization-modes) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="88dc1-142">See [Optimization modes](#optimization-modes) for more info.</span></span><br/> <span data-ttu-id="88dc1-143">El tipo es D2D1 \_ DIRECTIONALBLUR \_ Optimization.</span><span class="sxs-lookup"><span data-stu-id="88dc1-143">The type is D2D1\_DIRECTIONALBLUR\_OPTIMIZATION.</span></span><br/> <span data-ttu-id="88dc1-144">El valor predeterminado es D2D1 \_ DIRECTIONALBLUR \_ optimizado de optimización \_ .</span><span class="sxs-lookup"><span data-stu-id="88dc1-144">The default value is D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_BALANCED.</span></span> <br/>                                                                                                                                                         |
| <span data-ttu-id="88dc1-145">BorderMode</span><span class="sxs-lookup"><span data-stu-id="88dc1-145">BorderMode</span></span><br/> <span data-ttu-id="88dc1-146">D2D1 \_ DIRECTIONALBLUR \_ \_ modo de borde \_ de la Prop</span><span class="sxs-lookup"><span data-stu-id="88dc1-146">D2D1\_DIRECTIONALBLUR\_PROP\_BORDER\_MODE</span></span><br/>               | <span data-ttu-id="88dc1-147">El modo que se usa para calcular el borde de la imagen, es decir, es flexible o difícil.</span><span class="sxs-lookup"><span data-stu-id="88dc1-147">The mode used to calculate the border of the image, soft or hard.</span></span> <span data-ttu-id="88dc1-148">Vea [modos de borde](#border-modes) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="88dc1-148">See [Border modes](#border-modes) for more info.</span></span><br/> <span data-ttu-id="88dc1-149">El tipo es D2D1 \_ Border \_ mode.</span><span class="sxs-lookup"><span data-stu-id="88dc1-149">The type is D2D1\_BORDER\_MODE.</span></span><br/> <span data-ttu-id="88dc1-150">El valor predeterminado es D2D1 \_ Border \_ Mode \_ .</span><span class="sxs-lookup"><span data-stu-id="88dc1-150">The default value is D2D1\_BORDER\_MODE\_SOFT.</span></span><br/>                                                                                                                                                                 |



 

## <a name="optimization-modes"></a><span data-ttu-id="88dc1-151">Modos de optimización</span><span class="sxs-lookup"><span data-stu-id="88dc1-151">Optimization modes</span></span>



| <span data-ttu-id="88dc1-152">Nombre</span><span class="sxs-lookup"><span data-stu-id="88dc1-152">Name</span></span>                                          | <span data-ttu-id="88dc1-153">Descripción</span><span class="sxs-lookup"><span data-stu-id="88dc1-153">Description</span></span>                                                                                                                           |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88dc1-154">Velocidad de optimización de D2D1 \_ DIRECTIONALBLUR \_ \_</span><span class="sxs-lookup"><span data-stu-id="88dc1-154">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_SPEED</span></span>    | <span data-ttu-id="88dc1-155">Aplica las optimizaciones internas, como el escalado previo en radios relativamente pequeños.</span><span class="sxs-lookup"><span data-stu-id="88dc1-155">Applies internal optimizations such as pre-scaling at relatively small radii.</span></span> <span data-ttu-id="88dc1-156">Utiliza el filtrado lineal.</span><span class="sxs-lookup"><span data-stu-id="88dc1-156">Uses linear filtering.</span></span>                                  |
| <span data-ttu-id="88dc1-157">Optimización de D2D1 \_ DIRECTIONALBLUR \_ \_ equilibrada</span><span class="sxs-lookup"><span data-stu-id="88dc1-157">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_BALANCED</span></span> | <span data-ttu-id="88dc1-158">Usa los mismos umbrales de optimización que el modo de velocidad, pero utiliza el filtrado trilineal.</span><span class="sxs-lookup"><span data-stu-id="88dc1-158">Uses the same optimization thresholds as Speed mode, but uses trilinear filtering.</span></span>                                                    |
| <span data-ttu-id="88dc1-159">Calidad de optimización de D2D1 \_ DIRECTIONALBLUR \_ \_</span><span class="sxs-lookup"><span data-stu-id="88dc1-159">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_QUALITY</span></span>  | <span data-ttu-id="88dc1-160">Solo usa optimizaciones internas con radios de desenfoque grandes, donde es menos probable que las aproximaciones sean visibles.</span><span class="sxs-lookup"><span data-stu-id="88dc1-160">Only uses internal optimizations with large blur radii, where approximations are less likely to be visible.</span></span> <span data-ttu-id="88dc1-161">Utiliza el filtrado trilineal.</span><span class="sxs-lookup"><span data-stu-id="88dc1-161">Uses trilinear filtering.</span></span> |



 

## <a name="border-modes"></a><span data-ttu-id="88dc1-162">Modos de borde</span><span class="sxs-lookup"><span data-stu-id="88dc1-162">Border modes</span></span>



| <span data-ttu-id="88dc1-163">Nombre</span><span class="sxs-lookup"><span data-stu-id="88dc1-163">Name</span></span>                     | <span data-ttu-id="88dc1-164">Descripción</span><span class="sxs-lookup"><span data-stu-id="88dc1-164">Description</span></span>                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88dc1-165">D2D1 \_ modo de borde \_ \_ flexible</span><span class="sxs-lookup"><span data-stu-id="88dc1-165">D2D1\_BORDER\_MODE\_SOFT</span></span> | <span data-ttu-id="88dc1-166">El efecto rellena la imagen con píxeles negros transparentes cuando aplica el kernel de desenfoque, lo que da lugar a un borde flexible.</span><span class="sxs-lookup"><span data-stu-id="88dc1-166">The effect pads the image with transparent black pixels as it applies the blur kernel, resulting in a soft edge.</span></span> <br/>                                                                                             |
| <span data-ttu-id="88dc1-167">D2D1 \_ del \_ modo de borde \_</span><span class="sxs-lookup"><span data-stu-id="88dc1-167">D2D1\_BORDER\_MODE\_HARD</span></span> | <span data-ttu-id="88dc1-168">El efecto fija la salida al tamaño de la imagen de entrada.</span><span class="sxs-lookup"><span data-stu-id="88dc1-168">The effect clamps the output to the size of the input image.</span></span> <span data-ttu-id="88dc1-169">Cuando el efecto aplica el kernel de desenfoque, extiende la imagen de entrada con una transformación de borde de tipo de reflejo para las muestras fuera de los límites de entrada.</span><span class="sxs-lookup"><span data-stu-id="88dc1-169">When the effect applies the blur kernel, it extends the input image with a mirror-type border transform for samples outside of the input bounds.</span></span><br/> |



 

## <a name="output-bitmap"></a><span data-ttu-id="88dc1-170">Mapa de bits de salida</span><span class="sxs-lookup"><span data-stu-id="88dc1-170">Output bitmap</span></span>

<span data-ttu-id="88dc1-171">El tamaño del mapa de bits de salida aumenta en función de la desviación estándar, el ángulo del efecto y el modo de borde.</span><span class="sxs-lookup"><span data-stu-id="88dc1-171">The size of the output bitmap increases based on the standard deviation, the angle of the effect, and the border mode.</span></span> <span data-ttu-id="88dc1-172">Si el modo de borde se establece en el \_ modo de borde D2D1 \_ \_ , aumenta el tamaño del mapa de bits de salida en función del tamaño del kernel de desenfoque, representado en píxeles.</span><span class="sxs-lookup"><span data-stu-id="88dc1-172">If the border mode is set to D2D1\_BORDER\_MODE\_SOFT the size of the output bitmap increases by the size of the blur kernel, represented in pixels.</span></span> <span data-ttu-id="88dc1-173">Estas ecuaciones se pueden usar para calcular el tamaño del mapa de bits de salida.</span><span class="sxs-lookup"><span data-stu-id="88dc1-173">These equations can be used to calculate the size of the output bitmap.</span></span>



| <span data-ttu-id="88dc1-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="88dc1-174">Requirement</span></span> | <span data-ttu-id="88dc1-175">Value</span><span class="sxs-lookup"><span data-stu-id="88dc1-175">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="88dc1-176">Crecimiento de mapa de bits de salida X</span><span class="sxs-lookup"><span data-stu-id="88dc1-176">Output Bitmap Growth X</span></span> | <span data-ttu-id="88dc1-177">StandardDeviation (DIP) \* 6 \* ((PPP del usuario)/96) \* cos (ángulo))</span><span class="sxs-lookup"><span data-stu-id="88dc1-177">StandardDeviation (DIPs) \* 6 \* ((User DPI) / 96) \* cos(Angle))</span></span> |
| <span data-ttu-id="88dc1-178">Crecimiento de mapa de bits de salida Y</span><span class="sxs-lookup"><span data-stu-id="88dc1-178">Output Bitmap Growth Y</span></span> | <span data-ttu-id="88dc1-179">StandardDeviation (DIP) \* 6 \* ((PPP del usuario)/96) \* sin (ángulo)</span><span class="sxs-lookup"><span data-stu-id="88dc1-179">StandardDeviation (DIPs) \* 6 \* ((User DPI) / 96) \* sin(Angle))</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="88dc1-180">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88dc1-180">Requirements</span></span>



| <span data-ttu-id="88dc1-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="88dc1-181">Requirement</span></span> | <span data-ttu-id="88dc1-182">Value</span><span class="sxs-lookup"><span data-stu-id="88dc1-182">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="88dc1-183">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88dc1-183">Minimum supported client</span></span> | <span data-ttu-id="88dc1-184">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="88dc1-184">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="88dc1-185">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88dc1-185">Minimum supported server</span></span> | <span data-ttu-id="88dc1-186">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="88dc1-186">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="88dc1-187">Encabezado</span><span class="sxs-lookup"><span data-stu-id="88dc1-187">Header</span></span>                   | <span data-ttu-id="88dc1-188">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="88dc1-188">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="88dc1-189">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="88dc1-189">Library</span></span>                  | <span data-ttu-id="88dc1-190">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="88dc1-190">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="88dc1-191">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="88dc1-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88dc1-192">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="88dc1-192">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

