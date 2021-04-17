---
title: Efecto de escala
description: Utilice este efecto para escalar o reducir verticalmente una imagen. El efecto tiene seis modos de escalado más cercanos, lineal, cúbico, Multimuestra lineal, anisotrópico y de alta calidad cúbicos.
ms.assetid: 99DFA8DB-384B-4F64-90A2-0D3D7E1ACF27
keywords:
- efecto de escala
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad3af77bc24db387fff0854e0432c270fa2ce6d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422231"
---
# <a name="scale-effect"></a><span data-ttu-id="6b191-105">Efecto de escala</span><span class="sxs-lookup"><span data-stu-id="6b191-105">Scale effect</span></span>

<span data-ttu-id="6b191-106">Utilice este efecto para escalar o reducir verticalmente una imagen.</span><span class="sxs-lookup"><span data-stu-id="6b191-106">Use this effect to scale an image up or down.</span></span> <span data-ttu-id="6b191-107">El efecto tiene seis modos de escala: vecino más cercano, lineal, cúbico, Multimuestra lineal, anisotrópico y de alta calidad cúbico.</span><span class="sxs-lookup"><span data-stu-id="6b191-107">The effect has six scaling modes: nearest neighbor, linear, cubic, multi-sample linear, anisotropic, and high quality cubic.</span></span>

<span data-ttu-id="6b191-108">El CLSID para este efecto es CLSID \_ D2D1Scale.</span><span class="sxs-lookup"><span data-stu-id="6b191-108">The CLSID for this effect is CLSID\_D2D1Scale.</span></span>

-   [<span data-ttu-id="6b191-109">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="6b191-109">Example image</span></span>](#example-image)
-   [<span data-ttu-id="6b191-110">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="6b191-110">Effect properties</span></span>](#effect-properties)
    -   [<span data-ttu-id="6b191-111">Modos de borde</span><span class="sxs-lookup"><span data-stu-id="6b191-111">Border modes</span></span>](#border-modes)
-   [<span data-ttu-id="6b191-112">Modos de interpolación</span><span class="sxs-lookup"><span data-stu-id="6b191-112">Interpolation modes</span></span>](#interpolation-modes)
-   [<span data-ttu-id="6b191-113">Mapa de bits de salida</span><span class="sxs-lookup"><span data-stu-id="6b191-113">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="6b191-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b191-114">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="6b191-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6b191-115">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="6b191-116">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="6b191-116">Example image</span></span>

<span data-ttu-id="6b191-117">En este ejemplo se muestra el efecto de escala de zoom en 2 veces la entrada y recortada al tamaño original.</span><span class="sxs-lookup"><span data-stu-id="6b191-117">This example shows the scale effect zooming in 2 times the input and cropping to the original size.</span></span>



| <span data-ttu-id="6b191-118">Antes</span><span class="sxs-lookup"><span data-stu-id="6b191-118">Before</span></span>                                                     |
|------------------------------------------------------------|
| ![imagen anterior al efecto.](images/default-before.jpg) |
| <span data-ttu-id="6b191-120">Después</span><span class="sxs-lookup"><span data-stu-id="6b191-120">After</span></span>                                                      |
| ![la imagen después de la transformación.](images/22-scale.png)     |



 


```C++
ComPtr<ID2D1Effect> scaleEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Scale, &scaleEffect);

scaleEffect->SetInput(0, bitmap);

scaleEffect->SetValue(D2D1_SCALE_PROP_CENTER_POINT, D2D1::Vector2F(256.0f, 192.0f));
scaleEffect->SetValue(D2D1_SCALE_PROP_SCALE, D2D1::Vector2F(2.0f, 2.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(scaleEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="6b191-122">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="6b191-122">Effect properties</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6b191-123">Enumeración de índice y nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="6b191-123">Display name and index enumeration</span></span></th>
<th><span data-ttu-id="6b191-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="6b191-124">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6b191-125">Escala</span><span class="sxs-lookup"><span data-stu-id="6b191-125">Scale</span></span><br/> <span data-ttu-id="6b191-126">D2D1_SCALE_PROP_SCALE</span><span class="sxs-lookup"><span data-stu-id="6b191-126">D2D1_SCALE_PROP_SCALE</span></span><br/></td>
<td><span data-ttu-id="6b191-127">La cantidad de escala en la dirección X e y como una relación entre el tamaño de salida y el tamaño de entrada.</span><span class="sxs-lookup"><span data-stu-id="6b191-127">The scale amount in the X and Y direction as a ratio of the output size to the input size.</span></span> <span data-ttu-id="6b191-128">Esta propiedad es D2D1_VECTOR_2Fdefined: (escala X, escala Y).</span><span class="sxs-lookup"><span data-stu-id="6b191-128">This property a D2D1_VECTOR_2Fdefined as: (X scale, Y scale).</span></span> <span data-ttu-id="6b191-129">Las cantidades de escala son FLOAT, sin unidades y deben ser positivas o 0.</span><span class="sxs-lookup"><span data-stu-id="6b191-129">The scale amounts are FLOAT, unitless, and must be positive or 0.</span></span><br/> <span data-ttu-id="6b191-130">El tipo es D2D1_VECTOR_2F.</span><span class="sxs-lookup"><span data-stu-id="6b191-130">The type is D2D1_VECTOR_2F.</span></span><br/> <span data-ttu-id="6b191-131">El valor predeterminado es {1.0 f, 1.0 f}.</span><span class="sxs-lookup"><span data-stu-id="6b191-131">The default value is {1.0f, 1.0f}.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6b191-132">CenterPoint</span><span class="sxs-lookup"><span data-stu-id="6b191-132">CenterPoint</span></span><br/> <span data-ttu-id="6b191-133">D2D1_SCALE_PROP_CENTER_POINT</span><span class="sxs-lookup"><span data-stu-id="6b191-133">D2D1_SCALE_PROP_CENTER_POINT</span></span><br/></td>
<td><span data-ttu-id="6b191-134">Punto central de escalado de imagen.</span><span class="sxs-lookup"><span data-stu-id="6b191-134">The image scaling center point.</span></span> <span data-ttu-id="6b191-135">Esta propiedad es una D2D1_VECTOR_2F definida como: (punto X, punto Y).</span><span class="sxs-lookup"><span data-stu-id="6b191-135">This property is a D2D1_VECTOR_2F defined as: (point X, point Y).</span></span> <span data-ttu-id="6b191-136">Las unidades están en DIP.</span><span class="sxs-lookup"><span data-stu-id="6b191-136">The units are in DIPs.</span></span><br/> <span data-ttu-id="6b191-137">Use la propiedad punto central para escalar alrededor de un punto que no sea la esquina superior izquierda.</span><span class="sxs-lookup"><span data-stu-id="6b191-137">Use the center point property to scale around a point other than the upper-left corner.</span></span><br/> <span data-ttu-id="6b191-138">El tipo es D2D1_VECTOR_2F.</span><span class="sxs-lookup"><span data-stu-id="6b191-138">The type is D2D1_VECTOR_2F.</span></span><br/> <span data-ttu-id="6b191-139">El valor predeterminado es {0.0 f, 0.0 f}.</span><span class="sxs-lookup"><span data-stu-id="6b191-139">The default value is {0.0f, 0.0f}.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6b191-140">BorderMode</span><span class="sxs-lookup"><span data-stu-id="6b191-140">BorderMode</span></span><br/> <span data-ttu-id="6b191-141">D2D1_SCALE_PROP_BORDER_MODE</span><span class="sxs-lookup"><span data-stu-id="6b191-141">D2D1_SCALE_PROP_BORDER_MODE</span></span><br/></td>
<td><span data-ttu-id="6b191-142">El modo que se usa para calcular el borde de la imagen, es decir, es flexible o difícil.</span><span class="sxs-lookup"><span data-stu-id="6b191-142">The mode used to calculate the border of the image, soft or hard.</span></span> <span data-ttu-id="6b191-143">Vea <a href="#border-modes">modos de borde</a> para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="6b191-143">See <a href="#border-modes">Border modes</a> for more info.</span></span> <br/> <span data-ttu-id="6b191-144">El tipo es D2D1_BORDER_MODE.</span><span class="sxs-lookup"><span data-stu-id="6b191-144">The type is D2D1_BORDER_MODE.</span></span><br/> <span data-ttu-id="6b191-145">El valor predeterminado es D2D1_BORDER_MODE_SOFT.</span><span class="sxs-lookup"><span data-stu-id="6b191-145">The default value is D2D1_BORDER_MODE_SOFT.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6b191-146">Nitidez</span><span class="sxs-lookup"><span data-stu-id="6b191-146">Sharpness</span></span><br/> <span data-ttu-id="6b191-147">D2D1_SCALE_PROP_SHARPNESS</span><span class="sxs-lookup"><span data-stu-id="6b191-147">D2D1_SCALE_PROP_SHARPNESS</span></span><br/></td>
<td><span data-ttu-id="6b191-148">En el modo de interpolación cúbico de alta calidad, el nivel de nitidez del filtro de escalado es un valor de tipo float entre 0 y 1.</span><span class="sxs-lookup"><span data-stu-id="6b191-148">In the high quality cubic interpolation mode, the sharpness level of the scaling filter as a float between 0 and 1.</span></span> <span data-ttu-id="6b191-149">Los valores son no unitarias.</span><span class="sxs-lookup"><span data-stu-id="6b191-149">The values are unitless.</span></span> <span data-ttu-id="6b191-150">Puede usar la nitidez para ajustar la calidad de una imagen al reducir la escala de la imagen.</span><span class="sxs-lookup"><span data-stu-id="6b191-150">You can use sharpness to adjust the quality of an image when you scale the image down.</span></span><br/> <span data-ttu-id="6b191-151">El factor de nitidez afecta a la forma del kernel.</span><span class="sxs-lookup"><span data-stu-id="6b191-151">The sharpness factor affects the shape of the kernel.</span></span> <span data-ttu-id="6b191-152">Cuanto mayor sea el factor de nitidez, menor será el kernel.</span><span class="sxs-lookup"><span data-stu-id="6b191-152">The higher the sharpness factor, the smaller the kernel.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="6b191-153">Esta propiedad solo afecta al modo de interpolación cúbico de alta calidad.</span><span class="sxs-lookup"><span data-stu-id="6b191-153">This property affects only the high quality cubic interpolation mode.</span></span>
</blockquote>
<br/> <span data-ttu-id="6b191-154">El tipo es FLOAT.</span><span class="sxs-lookup"><span data-stu-id="6b191-154">The type is FLOAT.</span></span><br/> <span data-ttu-id="6b191-155">El valor predeterminado es 0.0 f.</span><span class="sxs-lookup"><span data-stu-id="6b191-155">The default value is 0.0f.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6b191-156">InterpolationMode</span><span class="sxs-lookup"><span data-stu-id="6b191-156">InterpolationMode</span></span><br/> <span data-ttu-id="6b191-157">D2D1_SCALE_PROP_INTERPOLATION_MODE</span><span class="sxs-lookup"><span data-stu-id="6b191-157">D2D1_SCALE_PROP_INTERPOLATION_MODE</span></span><br/></td>
<td><span data-ttu-id="6b191-158">El modo de interpolación que el efecto usa para escalar la imagen.</span><span class="sxs-lookup"><span data-stu-id="6b191-158">The interpolation mode the effect uses to scale the image.</span></span> <span data-ttu-id="6b191-159">Hay 6 modos de escala que abarcan la calidad y la velocidad.</span><span class="sxs-lookup"><span data-stu-id="6b191-159">There are 6 scale modes that range in quality and speed.</span></span> <span data-ttu-id="6b191-160">Vea <a href="#interpolation-modes">modos de interpolación</a> para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="6b191-160">See <a href="#interpolation-modes">Interpolation modes</a> for more info.</span></span> <br/> <span data-ttu-id="6b191-161">El tipo es D2D1_SCALE_INTERPOLATION_MODE.</span><span class="sxs-lookup"><span data-stu-id="6b191-161">The type is D2D1_SCALE_INTERPOLATION_MODE.</span></span><br/> <span data-ttu-id="6b191-162">El valor predeterminado es D2D1_SCALE_INTERPOLATION_MODE_LINEAR.</span><span class="sxs-lookup"><span data-stu-id="6b191-162">The default value is D2D1_SCALE_INTERPOLATION_MODE_LINEAR.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="border-modes"></a><span data-ttu-id="6b191-163">Modos de borde</span><span class="sxs-lookup"><span data-stu-id="6b191-163">Border modes</span></span>



| <span data-ttu-id="6b191-164">Nombre</span><span class="sxs-lookup"><span data-stu-id="6b191-164">Name</span></span>                     | <span data-ttu-id="6b191-165">Descripción</span><span class="sxs-lookup"><span data-stu-id="6b191-165">Description</span></span>                                                                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b191-166">D2D1 \_ modo de borde \_ \_ flexible</span><span class="sxs-lookup"><span data-stu-id="6b191-166">D2D1\_BORDER\_MODE\_SOFT</span></span> | <span data-ttu-id="6b191-167">El efecto rellena la imagen de entrada con píxeles negros transparentes para muestras fuera de los límites de entrada cuando aplica el kernel de circunvolución.</span><span class="sxs-lookup"><span data-stu-id="6b191-167">The effect pads the input image with transparent black pixels for samples outside of the input bounds when it applies the convolution kernel.</span></span> <span data-ttu-id="6b191-168">Esto crea un borde flexible para la imagen y, en el proceso, expande el mapa de bits de salida por el tamaño del kernel.</span><span class="sxs-lookup"><span data-stu-id="6b191-168">This creates a soft edge for the image, and in the process expands the output bitmap by the size of the kernel.</span></span><br/> |
| <span data-ttu-id="6b191-169">D2D1 \_ del \_ modo de borde \_</span><span class="sxs-lookup"><span data-stu-id="6b191-169">D2D1\_BORDER\_MODE\_HARD</span></span> | <span data-ttu-id="6b191-170">El efecto extiende la imagen de entrada con una transformación de borde de tipo de reflejo para las muestras fuera de los límites de entrada.</span><span class="sxs-lookup"><span data-stu-id="6b191-170">The effect extends the input image with a mirror-type border transform for samples outside of the input bounds.</span></span> <span data-ttu-id="6b191-171">El tamaño del mapa de bits de salida es igual al tamaño del mapa de bits de entrada.</span><span class="sxs-lookup"><span data-stu-id="6b191-171">The size of the output bitmap is equal to the size of the input bitmap.</span></span><br/>                                                                       |



 

\`

## <a name="interpolation-modes"></a><span data-ttu-id="6b191-172">Modos de interpolación</span><span class="sxs-lookup"><span data-stu-id="6b191-172">Interpolation modes</span></span>



| <span data-ttu-id="6b191-173">Enumeración</span><span class="sxs-lookup"><span data-stu-id="6b191-173">Enumeration</span></span>                                             | <span data-ttu-id="6b191-174">Descripción</span><span class="sxs-lookup"><span data-stu-id="6b191-174">Description</span></span>                                                                                                                                                                                          |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b191-175">D2D1 \_ modo de interpolación de escala de la \_ \_ \_ proximidad más cercano \_</span><span class="sxs-lookup"><span data-stu-id="6b191-175">D2D1\_SCALE\_INTERPOLATION\_MODE\_NEAREST\_NEIGHBOR</span></span>     | <span data-ttu-id="6b191-176">Muestrea el punto único más cercano y lo usa.</span><span class="sxs-lookup"><span data-stu-id="6b191-176">Samples the nearest single point and uses that.</span></span> <span data-ttu-id="6b191-177">Este modo utiliza menos tiempo de procesamiento, pero genera la imagen de menor calidad.</span><span class="sxs-lookup"><span data-stu-id="6b191-177">This mode uses less processing time, but outputs the lowest quality image.</span></span>                                                                           |
| <span data-ttu-id="6b191-178">\_ \_ \_ Modo lineal de interpolación de escala D2D1 \_</span><span class="sxs-lookup"><span data-stu-id="6b191-178">D2D1\_SCALE\_INTERPOLATION\_MODE\_LINEAR</span></span>                | <span data-ttu-id="6b191-179">Utiliza un ejemplo de cuatro puntos y una interpolación lineal.</span><span class="sxs-lookup"><span data-stu-id="6b191-179">Uses a four point sample and linear interpolation.</span></span> <span data-ttu-id="6b191-180">Este modo usa más tiempo de procesamiento que el modo vecino más cercano, pero genera una imagen de mayor calidad.</span><span class="sxs-lookup"><span data-stu-id="6b191-180">This mode uses more processing time than the nearest neighbor mode, but outputs a higher quality image.</span></span>                                           |
| <span data-ttu-id="6b191-181">\_Modo de \_ interpolación de escala D2D1 \_ \_ cúbico</span><span class="sxs-lookup"><span data-stu-id="6b191-181">D2D1\_SCALE\_INTERPOLATION\_MODE\_CUBIC</span></span>                 | <span data-ttu-id="6b191-182">Usa un kernel cúbico de ejemplo 16 para la interpolación.</span><span class="sxs-lookup"><span data-stu-id="6b191-182">Uses a 16 sample cubic kernel for interpolation.</span></span> <span data-ttu-id="6b191-183">Este modo utiliza la mayor parte del tiempo de procesamiento, pero genera una imagen de mayor calidad.</span><span class="sxs-lookup"><span data-stu-id="6b191-183">This mode uses the most processing time, but outputs a higher quality image.</span></span>                                                                        |
| <span data-ttu-id="6b191-184">\_Modo de \_ interpolación de escala D2D1 \_ \_ \_ Multimuestra \_ lineal</span><span class="sxs-lookup"><span data-stu-id="6b191-184">D2D1\_SCALE\_INTERPOLATION\_MODE\_MULTI\_SAMPLE\_LINEAR</span></span> | <span data-ttu-id="6b191-185">Usa 4 muestras lineales dentro de un solo píxel para el suavizado de contorno adecuado.</span><span class="sxs-lookup"><span data-stu-id="6b191-185">Uses 4 linear samples within a single pixel for good edge anti-aliasing.</span></span> <span data-ttu-id="6b191-186">Este modo es adecuado para reducir verticalmente en pequeñas cantidades de imágenes con pocos píxeles.</span><span class="sxs-lookup"><span data-stu-id="6b191-186">This mode is good for scaling down by small amounts on images with few pixels.</span></span>                                              |
| <span data-ttu-id="6b191-187">\_Modo de \_ interpolación de escala D2D1 \_ \_ anisotrópico</span><span class="sxs-lookup"><span data-stu-id="6b191-187">D2D1\_SCALE\_INTERPOLATION\_MODE\_ANISOTROPIC</span></span>           | <span data-ttu-id="6b191-188">Utiliza el filtrado anisotrópico para muestrear un patrón según la forma transformada del mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="6b191-188">Uses anisotropic filtering to sample a pattern according to the transformed shape of the bitmap.</span></span>                                                                                                     |
| <span data-ttu-id="6b191-189">D2D1 \_ modo de interpolación de escala de \_ \_ \_ alta \_ calidad \_ cúbico</span><span class="sxs-lookup"><span data-stu-id="6b191-189">D2D1\_SCALE\_INTERPOLATION\_MODE\_HIGH\_QUALITY\_CUBIC</span></span>  | <span data-ttu-id="6b191-190">Usa un kernel cúbico de alta calidad de tamaño variable para realizar una downscale previa de la imagen si downscaling está implicado en la matriz de transformación.</span><span class="sxs-lookup"><span data-stu-id="6b191-190">Uses a variable size high quality cubic kernel to perform a pre-downscale the image if downscaling is involved in the transform matrix.</span></span> <span data-ttu-id="6b191-191">A continuación, usa el modo de interpolación cúbico para la salida final.</span><span class="sxs-lookup"><span data-stu-id="6b191-191">Then uses the cubic interpolation mode for the final output.</span></span> |



 

> [!Note]  
> <span data-ttu-id="6b191-192">Si no selecciona un modo, el efecto tiene como valor predeterminado el \_ modo de interpolación de escala D2D1 \_ \_ \_ lineal.</span><span class="sxs-lookup"><span data-stu-id="6b191-192">If you don't select a mode, the effect defaults to D2D1\_SCALE\_INTERPOLATION\_MODE\_LINEAR.</span></span>

 

> [!Note]  
> <span data-ttu-id="6b191-193">El modo anisotrópico genera mapas MIP al escalar; sin embargo, si establece la propiedad **Cached** en true en los efectos que se aplican a este efecto, no se generarán los mapas MIP cada vez para imágenes suficientemente pequeñas.</span><span class="sxs-lookup"><span data-stu-id="6b191-193">Anisotropic mode generates mipmaps when scaling, however, if you set the **Cached** property to true on the effects that are input to this effect, the mipmaps won't be generated every time for sufficiently small images.</span></span>

 

## <a name="output-bitmap"></a><span data-ttu-id="6b191-194">Mapa de bits de salida</span><span class="sxs-lookup"><span data-stu-id="6b191-194">Output bitmap</span></span>

<span data-ttu-id="6b191-195">La ubicación y el tamaño del mapa de bits de salida dependen del factor de escala especificado y del punto central.</span><span class="sxs-lookup"><span data-stu-id="6b191-195">The location and size of the output bitmap depends on the specified scale factor and the center point.</span></span>

<span data-ttu-id="6b191-196">Puede calcular el tamaño del mapa de bits de salida con esta ecuación:</span><span class="sxs-lookup"><span data-stu-id="6b191-196">You can calculate the size of the output bitmap using this equation:</span></span><dl> <span data-ttu-id="6b191-197">BitmapSize? (Píxeles) = escala \* ¿Tamaño del mapa de bits original?</span><span class="sxs-lookup"><span data-stu-id="6b191-197">BitmapSize?(Pixels)=Scale?\*Original Bitmap Size?</span></span> <span data-ttu-id="6b191-198">(DIP) \* (UserDPI/96)</span><span class="sxs-lookup"><span data-stu-id="6b191-198">(DIPs)\*(UserDPI/96)</span></span>  
<span data-ttu-id="6b191-199">BitmapSize<sub>y</sub>(píxeles) =<sub></sub> \* tamaño del mapa de bits original<sub>y</sub> (DIP) \* (UserDPI/96)</span><span class="sxs-lookup"><span data-stu-id="6b191-199">BitmapSize<sub>y</sub>(Pixels)=Scale<sub>y</sub>\*Original Bitmap Size<sub>y</sub> (DIPs)\*(UserDPI/96)</span></span>  
</dl>

<span data-ttu-id="6b191-200">El efecto redondea las fracciones de píxeles hasta el píxel entero más próximo.</span><span class="sxs-lookup"><span data-stu-id="6b191-200">The effect rounds fractions of pixels up to the nearest whole pixel.</span></span>

<span data-ttu-id="6b191-201">La ubicación del mapa de bits es (0,0) o el valor de la propiedad de punto central.</span><span class="sxs-lookup"><span data-stu-id="6b191-201">The location of the bitmap is (0, 0) or the value of the center point property.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b191-202">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b191-202">Requirements</span></span>



| <span data-ttu-id="6b191-203">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b191-203">Requirement</span></span> | <span data-ttu-id="6b191-204">Value</span><span class="sxs-lookup"><span data-stu-id="6b191-204">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6b191-205">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6b191-205">Minimum supported client</span></span> | <span data-ttu-id="6b191-206">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="6b191-206">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="6b191-207">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6b191-207">Minimum supported server</span></span> | <span data-ttu-id="6b191-208">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="6b191-208">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="6b191-209">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6b191-209">Header</span></span>                   | <span data-ttu-id="6b191-210">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="6b191-210">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="6b191-211">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6b191-211">Library</span></span>                  | <span data-ttu-id="6b191-212">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="6b191-212">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="6b191-213">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6b191-213">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b191-214">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="6b191-214">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

