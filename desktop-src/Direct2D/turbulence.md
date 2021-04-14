---
title: Efecto de turbulencia
description: Use el efecto turbulencia para generar un mapa de bits basado en la función de ruido de Perlen.
ms.assetid: 86C1990E-958C-46D7-840A-E4A17F1D1740
keywords:
- efecto de turbulencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f67f615ec5b68ca285a048b68bc7bc8eab6e24
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "104564507"
---
# <a name="turbulence-effect"></a><span data-ttu-id="42993-104">Efecto de turbulencia</span><span class="sxs-lookup"><span data-stu-id="42993-104">Turbulence effect</span></span>

<span data-ttu-id="42993-105">Use el efecto turbulencia para generar un mapa de bits basado en la función de ruido de Perlen.</span><span class="sxs-lookup"><span data-stu-id="42993-105">Use the turbulence effect to generate a bitmap based on the Perlin noise function.</span></span>

<span data-ttu-id="42993-106">El efecto de turbulencia no tiene ninguna imagen de entrada.</span><span class="sxs-lookup"><span data-stu-id="42993-106">The turbulence effect has no input image.</span></span>

<span data-ttu-id="42993-107">El CLSID para este efecto es CLSID \_ D2D1Turbulence.</span><span class="sxs-lookup"><span data-stu-id="42993-107">The CLSID for this effect is CLSID\_D2D1Turbulence.</span></span>

-   [<span data-ttu-id="42993-108">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="42993-108">Example image</span></span>](#example-image)
-   [<span data-ttu-id="42993-109">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="42993-109">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="42993-110">Modos de ruido</span><span class="sxs-lookup"><span data-stu-id="42993-110">Noise modes</span></span>](#noise-modes)
-   [<span data-ttu-id="42993-111">Mapa de bits de salida</span><span class="sxs-lookup"><span data-stu-id="42993-111">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="42993-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42993-112">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="42993-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="42993-113">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="42993-114">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="42993-114">Example image</span></span>

![captura de pantalla de ejemplo de efecto que muestra la salida del efecto de turbulencia.](images/32-turbulence.png)

<span data-ttu-id="42993-116">El efecto de turbulencia calcula la suma de una o más octava de la función de ruido de Perlen.</span><span class="sxs-lookup"><span data-stu-id="42993-116">The Turbulence effect computes the sum of one or more octaves of the Perlin noise function.</span></span> <span data-ttu-id="42993-117">Perlen ruido es una función pseudoaleatorios cuyo valor depende de la frecuencia, la posición y el valor de inicialización.</span><span class="sxs-lookup"><span data-stu-id="42993-117">Perlin noise is a pseudo-random function whose value depends on the frequency, position, and seed value.</span></span> <span data-ttu-id="42993-118">El efecto genera los valores RGBA mediante una de estas ecuaciones.</span><span class="sxs-lookup"><span data-stu-id="42993-118">The effect generates the RGBA values using one of these equations.</span></span>

<span data-ttu-id="42993-119">Si selecciona el modo de \_ ruido de D2D1 turbulencia \_ ruido \_ fractal \_ de la suma de ruido, el efecto utiliza esta ecuación.</span><span class="sxs-lookup"><span data-stu-id="42993-119">If you select the D2D1\_TURBULENCE\_NOISE\_FRACTAL\_SUM noise mode the effect uses this equation.</span></span>

![Captura de pantalla que muestra la función de turbulencias usada para generar un mapa de bits.](images/turbulence-equation1.png)

<span data-ttu-id="42993-121">Si selecciona el modo de \_ \_ ruido de \_ turbulencias de ruido de D2D1, el efecto utiliza esta ecuación.</span><span class="sxs-lookup"><span data-stu-id="42993-121">If you select the D2D1\_TURBULENCE\_NOISE\_TURBULENCE noise mode the effect uses this equation.</span></span>

![la función turbulencias que se usa para generar un mapa de bits.](images/turbulence-equation2.png)

> [!Note]  
> <span data-ttu-id="42993-123">La `PerlinNoise` función tiene un intervalo de \[ -1, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="42993-123">The `PerlinNoise` function has a range of \[-1, 1\].</span></span>

 

<span data-ttu-id="42993-124">Este efecto produce valores de píxeles en alfa premultiplicado.</span><span class="sxs-lookup"><span data-stu-id="42993-124">This effect outputs pixel values in premultiplied alpha.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="42993-125">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="42993-125">Effect properties</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="42993-126">Enumeración de índice y nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="42993-126">Display name and index enumeration</span></span></th>
<th><span data-ttu-id="42993-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="42993-127">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="42993-128">Offset</span><span class="sxs-lookup"><span data-stu-id="42993-128">Offset</span></span><br/> <span data-ttu-id="42993-129">D2D1_TURBULENCE_PROP_OFFSET</span><span class="sxs-lookup"><span data-stu-id="42993-129">D2D1_TURBULENCE_PROP_OFFSET</span></span><br/></td>
<td><span data-ttu-id="42993-130">Coordenadas donde se genera la salida de turbulencias.</span><span class="sxs-lookup"><span data-stu-id="42993-130">The coordinates where the turbulence output is generated.</span></span><br/> <span data-ttu-id="42993-131">El algoritmo utilizado para generar el ruido de Perl es dependiente de la posición, por lo que un desplazamiento diferente da como resultado una salida diferente.</span><span class="sxs-lookup"><span data-stu-id="42993-131">The algorithm used to generate the Perlin noise is position dependent, so a different offset results in a different output.</span></span> <span data-ttu-id="42993-132">Esta propiedad no está enlazada y las unidades se especifican en DIP</span><span class="sxs-lookup"><span data-stu-id="42993-132">This property is not bounded and the units are specified in DIPs</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="42993-133">El desplazamiento no tiene el mismo efecto que una traducción porque la salida de la función de ruido es infinita y la función se ajustará alrededor del mosaico.</span><span class="sxs-lookup"><span data-stu-id="42993-133">The offset does not have the same effect as a translation because the noise function output is infinite and the function will wrap around the tile.</span></span>
</blockquote>
<br/> <span data-ttu-id="42993-134">El tipo es D2D1_VECTOR_2F.</span><span class="sxs-lookup"><span data-stu-id="42993-134">The type is D2D1_VECTOR_2F.</span></span><br/> <span data-ttu-id="42993-135">El valor predeterminado es {0.0 f, 0.0 f}.</span><span class="sxs-lookup"><span data-stu-id="42993-135">The default value is {0.0f, 0.0f}.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42993-136">Tamaño</span><span class="sxs-lookup"><span data-stu-id="42993-136">Size</span></span><br/> <span data-ttu-id="42993-137">D2D1_TURBULENCE_PROP_SIZE</span><span class="sxs-lookup"><span data-stu-id="42993-137">D2D1_TURBULENCE_PROP_SIZE</span></span><br/></td>
<td><span data-ttu-id="42993-138">Tamaño de la salida de turbulencia.</span><span class="sxs-lookup"><span data-stu-id="42993-138">The size of the turbulence output.</span></span><br/> <span data-ttu-id="42993-139">Esta propiedad no está enlazada y las unidades se especifican en DIP</span><span class="sxs-lookup"><span data-stu-id="42993-139">This property is not bounded and the units are specified in DIPs</span></span> <br/>
<br/> <span data-ttu-id="42993-140">El tipo es D2D1_VECTOR_2F.</span><span class="sxs-lookup"><span data-stu-id="42993-140">The type is D2D1_VECTOR_2F.</span></span><br/> <span data-ttu-id="42993-141">El valor predeterminado es {0.0 f, 0.0 f}.</span><span class="sxs-lookup"><span data-stu-id="42993-141">The default value is {0.0f, 0.0f}.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="42993-142">BaseFrequency</span><span class="sxs-lookup"><span data-stu-id="42993-142">BaseFrequency</span></span><br/> <span data-ttu-id="42993-143">D2D1_TURBULENCE_PROP_BASE_FREQUENCY</span><span class="sxs-lookup"><span data-stu-id="42993-143">D2D1_TURBULENCE_PROP_BASE_FREQUENCY</span></span><br/></td>
<td><span data-ttu-id="42993-144">Frecuencias base en la dirección X e y.</span><span class="sxs-lookup"><span data-stu-id="42993-144">The base frequencies in the X and Y direction.</span></span> <span data-ttu-id="42993-145">Esta propiedad es de tipo float y debe ser mayor que 0.</span><span class="sxs-lookup"><span data-stu-id="42993-145">This property is a float and must be greater than 0.</span></span> <span data-ttu-id="42993-146">Las unidades se especifican en 1/DIP.</span><span class="sxs-lookup"><span data-stu-id="42993-146">The units are specified in 1/DIPs.</span></span> <br/> <span data-ttu-id="42993-147">Un valor de 1 (1/DIP) para la frecuencia base da lugar a que el ruido de Perl complete un ciclo completo entre dos píxeles.</span><span class="sxs-lookup"><span data-stu-id="42993-147">A value of 1 (1/DIPs) for the base frequency results in the Perlin noise completing an entire cycle between two pixels.</span></span> <span data-ttu-id="42993-148">La interpolación de facilidad para estos píxeles produce píxeles totalmente aleatorios, ya que no hay ninguna correlación entre los píxeles.</span><span class="sxs-lookup"><span data-stu-id="42993-148">The ease interpolation for these pixels results in completely random pixels, since there is no correlation between the pixels.</span></span><br/> <span data-ttu-id="42993-149">Un valor de 0.1 (1/DIP) para la frecuencia de base, la función de ruido de Perl se repite cada 10 dip.</span><span class="sxs-lookup"><span data-stu-id="42993-149">A value of 0.1(1/DIPs) for the base frequency, the Perlin noise function repeats every 10 DIPs.</span></span> <span data-ttu-id="42993-150">Esto da como resultado una correlación entre píxeles y el efecto de turbulencia típico es visible.</span><span class="sxs-lookup"><span data-stu-id="42993-150">This results in correlation between pixels and the typical turbulence effect is visible.</span></span><br/> <span data-ttu-id="42993-151">El tipo es D2D1_VECTOR_2F.</span><span class="sxs-lookup"><span data-stu-id="42993-151">The type is D2D1_VECTOR_2F.</span></span><br/> <span data-ttu-id="42993-152">El valor predeterminado es {0,01 f, 0,01 f}.</span><span class="sxs-lookup"><span data-stu-id="42993-152">The default value is {0.01f, 0.01f}.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42993-153">NumOctaves</span><span class="sxs-lookup"><span data-stu-id="42993-153">NumOctaves</span></span><br/> <span data-ttu-id="42993-154">D2D1_TURBULENCE_PROP_NUM_OCTAVES</span><span class="sxs-lookup"><span data-stu-id="42993-154">D2D1_TURBULENCE_PROP_NUM_OCTAVES</span></span><br/></td>
<td><span data-ttu-id="42993-155">El número de octavas para la función de ruido.</span><span class="sxs-lookup"><span data-stu-id="42993-155">The number of octaves for the noise function.</span></span> <span data-ttu-id="42993-156">Esta propiedad es un UINT32 y debe ser mayor que 0.</span><span class="sxs-lookup"><span data-stu-id="42993-156">This property is a UINT32 and must be greater than 0.</span></span><br/> <span data-ttu-id="42993-157">El tipo es UINT32.</span><span class="sxs-lookup"><span data-stu-id="42993-157">The type is UINT32.</span></span><br/> <span data-ttu-id="42993-158">El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="42993-158">The default value is 1.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="42993-159">Seed</span><span class="sxs-lookup"><span data-stu-id="42993-159">Seed</span></span><br/> <span data-ttu-id="42993-160">D2D1_TURBULENCE_PROP_SEED</span><span class="sxs-lookup"><span data-stu-id="42993-160">D2D1_TURBULENCE_PROP_SEED</span></span><br/></td>
<td><span data-ttu-id="42993-161">Inicialización del generador pseudoaleatorios.</span><span class="sxs-lookup"><span data-stu-id="42993-161">The seed for the pseudo random generator.</span></span> <span data-ttu-id="42993-162">Esta propiedad no está enlazada.</span><span class="sxs-lookup"><span data-stu-id="42993-162">This property is unbounded.</span></span><br/> <span data-ttu-id="42993-163">El tipo es UINT32.</span><span class="sxs-lookup"><span data-stu-id="42993-163">The type is UINT32.</span></span><br/> <span data-ttu-id="42993-164">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="42993-164">The default value is 0.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42993-165">Ruido</span><span class="sxs-lookup"><span data-stu-id="42993-165">Noise</span></span><br/> <span data-ttu-id="42993-166">D2D1_TURBULENCE_PROP_NOISE</span><span class="sxs-lookup"><span data-stu-id="42993-166">D2D1_TURBULENCE_PROP_NOISE</span></span><br/></td>
<td><span data-ttu-id="42993-167">Modo de ruido de turbulencia.</span><span class="sxs-lookup"><span data-stu-id="42993-167">The turbulence noise mode.</span></span> <span data-ttu-id="42993-168">Esta propiedad puede ser <em>SUM</em> o <em>turbulencia</em>.</span><span class="sxs-lookup"><span data-stu-id="42993-168">This property can be either <em>fractal sum</em> or <em>turbulence</em>.</span></span> <span data-ttu-id="42993-169">Indica si se debe generar un mapa de bits basado en ruido fractal o en la función turbulencias.</span><span class="sxs-lookup"><span data-stu-id="42993-169">Indicates whether to generate a bitmap based on Fractal Noise or the Turbulence function.</span></span> <span data-ttu-id="42993-170">Vea <a href="#noise-modes">modos de ruido</a> para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="42993-170">See <a href="#noise-modes">Noise modes</a> for more info.</span></span> <br/> <span data-ttu-id="42993-171">El tipo es D2D1_TURBULENCE_NOISE.</span><span class="sxs-lookup"><span data-stu-id="42993-171">The type is D2D1_TURBULENCE_NOISE.</span></span><br/> <span data-ttu-id="42993-172">El valor predeterminado es D2D1_TURBULENCE_NOISE_FRACTAL_SUM.</span><span class="sxs-lookup"><span data-stu-id="42993-172">The default value is D2D1_TURBULENCE_NOISE_FRACTAL_SUM.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="42993-173">Que se pudo unir</span><span class="sxs-lookup"><span data-stu-id="42993-173">Stitchable</span></span><br/> <span data-ttu-id="42993-174">D2D1_TURBULENCE_PROP_STITCHABLE</span><span class="sxs-lookup"><span data-stu-id="42993-174">D2D1_TURBULENCE_PROP_STITCHABLE</span></span><br/></td>
<td><span data-ttu-id="42993-175">Activa o desactiva la Unión.</span><span class="sxs-lookup"><span data-stu-id="42993-175">Turns stitching on or off.</span></span> <span data-ttu-id="42993-176">La frecuencia base se ajusta para que se pueda unir el mapa de bits de salida.</span><span class="sxs-lookup"><span data-stu-id="42993-176">The base frequency is adjusted so that output bitmap can be stitched.</span></span> <span data-ttu-id="42993-177">Esto resulta útil si desea colocar en mosaico varias copias de la salida del efecto de turbulencias.</span><span class="sxs-lookup"><span data-stu-id="42993-177">This is useful if you want to tile multiple copies of the turbulence effect output.</span></span>
<ul>
<li><span data-ttu-id="42993-178">True el mapa de bits de salida se puede colocar en mosaico (con el efecto de mosaico) sin la apariencia de las costuras.</span><span class="sxs-lookup"><span data-stu-id="42993-178">True   The output bitmap can be tiled (using the tile effect) without the appearance of seams.</span></span> <span data-ttu-id="42993-179">La frecuencia base se ajusta para que se pueda unir el mapa de bits de salida.</span><span class="sxs-lookup"><span data-stu-id="42993-179">The base frequency is adjusted so that output bitmap can be stitched.</span></span></li>
<li><span data-ttu-id="42993-180">False: no se ajusta la frecuencia base, por lo que pueden aparecer juntas entre mosaicos si el mapa de bits está en mosaico.</span><span class="sxs-lookup"><span data-stu-id="42993-180">False   The base frequency is not adjusted, so seams may appear between tiles if the bitmap is tiled.</span></span></li>
</ul>
<br/> <span data-ttu-id="42993-181">El tipo es BOOL.</span><span class="sxs-lookup"><span data-stu-id="42993-181">The type is BOOL.</span></span><br/> <span data-ttu-id="42993-182">El valor predeterminado es FALSE.</span><span class="sxs-lookup"><span data-stu-id="42993-182">The default value is FALSE.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="noise-modes"></a><span data-ttu-id="42993-183">Modos de ruido</span><span class="sxs-lookup"><span data-stu-id="42993-183">Noise modes</span></span>



| <span data-ttu-id="42993-184">Enumeración</span><span class="sxs-lookup"><span data-stu-id="42993-184">Enumeration</span></span>                           | <span data-ttu-id="42993-185">Descripción</span><span class="sxs-lookup"><span data-stu-id="42993-185">Description</span></span>                                                                           |
|---------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="42993-186">D2D1 \_ turbulencia \_ ruido \_ fractal- \_ suma</span><span class="sxs-lookup"><span data-stu-id="42993-186">D2D1\_TURBULENCE\_NOISE\_FRACTAL\_SUM</span></span> | <span data-ttu-id="42993-187">Calcula una suma de las octavas, desplazando el intervalo de salida de \[ -1, 1 \] , a \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="42993-187">Computes a sum of the octaves, shifting the output range from \[-1, 1\], to \[0, 1\].</span></span> |
| <span data-ttu-id="42993-188">Turbulencia de ruido de D2D1 de \_ turbulencias \_ \_</span><span class="sxs-lookup"><span data-stu-id="42993-188">D2D1\_TURBULENCE\_NOISE\_TURBULENCE</span></span>   | <span data-ttu-id="42993-189">Calcula una suma del valor absoluto de cada octava.</span><span class="sxs-lookup"><span data-stu-id="42993-189">Computes a sum of the absolute value of each octave.</span></span>                                  |



 

> [!Note]  
> <span data-ttu-id="42993-190">Ninguno de los modos contiene una abrazadera explícita de los valores de salida.</span><span class="sxs-lookup"><span data-stu-id="42993-190">Neither mode contains an explicit clamp of the output values.</span></span>

 

## <a name="output-bitmap"></a><span data-ttu-id="42993-191">Mapa de bits de salida</span><span class="sxs-lookup"><span data-stu-id="42993-191">Output bitmap</span></span>

<span data-ttu-id="42993-192">Este efecto genera un mapa de bits de tamaño lógico infinito.</span><span class="sxs-lookup"><span data-stu-id="42993-192">This effect generates a logically infinite sized bitmap.</span></span>

## <a name="requirements"></a><span data-ttu-id="42993-193">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42993-193">Requirements</span></span>



| <span data-ttu-id="42993-194">Requisito</span><span class="sxs-lookup"><span data-stu-id="42993-194">Requirement</span></span> | <span data-ttu-id="42993-195">Value</span><span class="sxs-lookup"><span data-stu-id="42993-195">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="42993-196">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42993-196">Minimum supported client</span></span> | <span data-ttu-id="42993-197">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="42993-197">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="42993-198">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42993-198">Minimum supported server</span></span> | <span data-ttu-id="42993-199">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="42993-199">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="42993-200">Encabezado</span><span class="sxs-lookup"><span data-stu-id="42993-200">Header</span></span>                   | <span data-ttu-id="42993-201">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="42993-201">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="42993-202">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="42993-202">Library</span></span>                  | <span data-ttu-id="42993-203">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="42993-203">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="42993-204">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="42993-204">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42993-205">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="42993-205">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

