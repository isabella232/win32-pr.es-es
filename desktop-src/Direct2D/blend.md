---
title: Efecto de fusión
description: Use el efecto de mezcla para combinar dos imágenes. Este efecto tiene 26 modos de mezcla.
ms.assetid: 39D8BAA3-8FF3-4F10-99A0-B26FCA3018AE
keywords:
- efecto de mezcla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e248d1f7f41721d173510b8d10feac9be2e08f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905579"
---
# <a name="blend-effect"></a><span data-ttu-id="23da3-105">Efecto de fusión</span><span class="sxs-lookup"><span data-stu-id="23da3-105">Blend effect</span></span>

<span data-ttu-id="23da3-106">Use el efecto de mezcla para combinar dos imágenes.</span><span class="sxs-lookup"><span data-stu-id="23da3-106">Use the blend effect to combine 2 images.</span></span> <span data-ttu-id="23da3-107">Este efecto tiene 26 modos de mezcla.</span><span class="sxs-lookup"><span data-stu-id="23da3-107">This effect has 26 blend modes.</span></span>

<span data-ttu-id="23da3-108">El CLSID para este efecto es CLSID \_ D2D1Blend.</span><span class="sxs-lookup"><span data-stu-id="23da3-108">The CLSID for this effect is CLSID\_D2D1Blend.</span></span>

-   [<span data-ttu-id="23da3-109">Ejemplos de fusión</span><span class="sxs-lookup"><span data-stu-id="23da3-109">Blending examples</span></span>](#blending-examples)
-   [<span data-ttu-id="23da3-110">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="23da3-110">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="23da3-111">Modos de fusión</span><span class="sxs-lookup"><span data-stu-id="23da3-111">Blend modes</span></span>](#blend-modes)
-   [<span data-ttu-id="23da3-112">Conversiones de espacio de color HSL</span><span class="sxs-lookup"><span data-stu-id="23da3-112">HSL color space conversions</span></span>](#hsl-color-space-conversions)
    -   [<span data-ttu-id="23da3-113">Convertir de RGB a HSL</span><span class="sxs-lookup"><span data-stu-id="23da3-113">Converting from RGB to HSL</span></span>](#converting-from-rgb-to-hsl)
    -   [<span data-ttu-id="23da3-114">Convertir de HSL a RGB</span><span class="sxs-lookup"><span data-stu-id="23da3-114">Converting from HSL to RGB</span></span>](#converting-from-hsl-to-rgb)
-   [<span data-ttu-id="23da3-115">Mapa de bits de salida</span><span class="sxs-lookup"><span data-stu-id="23da3-115">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="23da3-116">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="23da3-116">Sample code</span></span>](#sample-code)
-   [<span data-ttu-id="23da3-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23da3-117">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="23da3-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="23da3-118">Related topics</span></span>](#related-topics)

## <a name="blending-examples"></a><span data-ttu-id="23da3-119">Ejemplos de fusión</span><span class="sxs-lookup"><span data-stu-id="23da3-119">Blending examples</span></span>

<span data-ttu-id="23da3-120">Esta es una imagen de ejemplo de cada modo de mezcla del efecto de mezcla.</span><span class="sxs-lookup"><span data-stu-id="23da3-120">Here is an example image of every blend mode of the blend effect.</span></span> <span data-ttu-id="23da3-121">En la siguiente sección se muestra una lista completa de los modos de mezcla y las propiedades de modo correspondientes.</span><span class="sxs-lookup"><span data-stu-id="23da3-121">A full list of the blend modes and the corresponding mode properties are in the next section</span></span>

![captura de pantalla de ejemplo de efecto de todos los modos de fusión disponibles.](images/blend-modes.png)

<span data-ttu-id="23da3-123">Este es otro ejemplo que usa el modo de exclusión.</span><span class="sxs-lookup"><span data-stu-id="23da3-123">Here is another example using the exclusion mode.</span></span>



| <span data-ttu-id="23da3-124">Antes de la imagen 1</span><span class="sxs-lookup"><span data-stu-id="23da3-124">Before image 1</span></span>                                                             |
|----------------------------------------------------------------------------|
| ![primera imagen de origen antes del efecto.](images/default-before.jpg)    |
| <span data-ttu-id="23da3-126">Antes de la imagen 2</span><span class="sxs-lookup"><span data-stu-id="23da3-126">Before image 2</span></span>                                                             |
| ![segunda imagen anterior al efecto.](images/4-arthimetic-composite2.jpg) |
| <span data-ttu-id="23da3-128">Después</span><span class="sxs-lookup"><span data-stu-id="23da3-128">After</span></span>                                                                      |
| ![la imagen después de la transformación.](images/5-blend.png)                      |



 


```C++
ComPtr<ID2D1Effect> blendEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Blend, &blendEffect);

blendEffect->SetInput(0, bitmap);
blendEffect->SetInput(1, bitmapTwo);
blendEffect->SetValue(D2D1_BLEND_PROP_MODE, D2D1_BLEND_MODE_EXCLUSION);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(blendEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="23da3-130">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="23da3-130">Effect properties</span></span>



| <span data-ttu-id="23da3-131">Enumeración de índice y nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="23da3-131">Display name and index enumeration</span></span>                 | <span data-ttu-id="23da3-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="23da3-132">Description</span></span>                                                                                                                                                                               |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23da3-133">Mode</span><span class="sxs-lookup"><span data-stu-id="23da3-133">Mode</span></span><br/> <span data-ttu-id="23da3-134">Modo de D2D1 \_ Blend \_ \_</span><span class="sxs-lookup"><span data-stu-id="23da3-134">D2D1\_BLEND\_PROP\_MODE</span></span><br/> | <span data-ttu-id="23da3-135">Modo de mezcla que se usa para el efecto.</span><span class="sxs-lookup"><span data-stu-id="23da3-135">The blend mode used for the effect.</span></span> <span data-ttu-id="23da3-136">Vea [modos de mezcla](#blend-modes) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="23da3-136">See [Blend modes](#blend-modes) for more info.</span></span> <span data-ttu-id="23da3-137">El tipo es D2D1 \_ Blend \_ mode.</span><span class="sxs-lookup"><span data-stu-id="23da3-137">The type is D2D1\_BLEND\_MODE.</span></span><br/> <span data-ttu-id="23da3-138">El valor predeterminado es D2D1 \_ Blend \_ Mode \_ multiplicate.</span><span class="sxs-lookup"><span data-stu-id="23da3-138">The default value is D2D1\_BLEND\_MODE\_MULTIPLY.</span></span><br/> |



 

## <a name="blend-modes"></a><span data-ttu-id="23da3-139">Modos de fusión</span><span class="sxs-lookup"><span data-stu-id="23da3-139">Blend modes</span></span>

<span data-ttu-id="23da3-140">En la tabla siguiente se muestran todos los modos de Blend de este efecto.</span><span class="sxs-lookup"><span data-stu-id="23da3-140">The table here shows all the blend modes of this effect.</span></span> <span data-ttu-id="23da3-141">Las funciones auxiliares necesarias para calcular el resultado del efecto se encuentran en la sección siguiente.</span><span class="sxs-lookup"><span data-stu-id="23da3-141">The helper functions necessary to compute the output of the effect are in the next section.</span></span>

<span data-ttu-id="23da3-142">Color: O <sub>PRGB</sub>  =  *f*(f <sub>RGB</sub>, B <sub>RGB</sub>) \* f <sub>a</sub> \* B <sub>a</sub> + f <sub>RGB</sub> \* f <sub>a</sub> \* (1-B <sub>a</sub>) + B <sub>RGB</sub> \* b <sub>a</sub> \* (1-f <sub>a</sub>)</span><span class="sxs-lookup"><span data-stu-id="23da3-142">Color: O <sub>PRGB</sub> = *f*(F<sub>RGB</sub>, B<sub>RGB</sub>) \* F<sub>A</sub> \* B<sub>A</sub> + F<sub>RGB</sub> \* F<sub>A</sub> \* (1 - B<sub>A</sub>) + B<sub>RGB</sub> \* B<sub>A</sub> \* (1 - F<sub>A</sub>)</span></span>

<span data-ttu-id="23da3-143">Alfa: O<sub>a</sub> = F<sub>a</sub> \* (1-B<sub>a</sub>) + B<sub>a</sub></span><span class="sxs-lookup"><span data-stu-id="23da3-143">Alpha: O<sub>A</sub> = F<sub>A</sub> \* (1 - B<sub>A</sub>) + B<sub>A</sub></span></span>

<span data-ttu-id="23da3-144">Donde:</span><span class="sxs-lookup"><span data-stu-id="23da3-144">Where:</span></span>

-   <span data-ttu-id="23da3-145">O<sub>PRGB</sub> es el color de salida multiplicado previamente</span><span class="sxs-lookup"><span data-stu-id="23da3-145">O<sub>PRGB</sub> is the pre-multiplied output color</span></span>
-   <span data-ttu-id="23da3-146">O es alfa<sub>de</sub> salida</span><span class="sxs-lookup"><span data-stu-id="23da3-146">O<sub>A</sub> is Output Alpha</span></span>
-   <span data-ttu-id="23da3-147">B<sub>RGB</sub> es el color de destino no multiplicado previamente</span><span class="sxs-lookup"><span data-stu-id="23da3-147">B<sub>RGB</sub> is the un-pre-multiplied destination color</span></span>
-   <span data-ttu-id="23da3-148">B<sub>A es el</sub> destino Alfa</span><span class="sxs-lookup"><span data-stu-id="23da3-148">B<sub>A</sub> is destination alpha</span></span>
-   <span data-ttu-id="23da3-149">F<sub>RGB</sub> es el color de origen sin premultiplicado</span><span class="sxs-lookup"><span data-stu-id="23da3-149">F<sub>RGB</sub> is the un-pre-multiplied source color</span></span>
-   <span data-ttu-id="23da3-150">F<sub>A</sub> es alfa de origen</span><span class="sxs-lookup"><span data-stu-id="23da3-150">F<sub>A</sub> is source alpha</span></span>
-   <span data-ttu-id="23da3-151">*f*(S <sub>RGB</sub>, D <sub>RGB</sub>) es una función de Blend que varía según el modo de mezcla.</span><span class="sxs-lookup"><span data-stu-id="23da3-151">*f*(S<sub>RGB</sub>, D<sub>RGB</sub>) is a blend function that varies per-blend-mode</span></span>

<span data-ttu-id="23da3-152">Algunos de los modos de mezcla requieren la conversión del espacio de colores Hue, saturación y luminosidad (HSL) a RGB.</span><span class="sxs-lookup"><span data-stu-id="23da3-152">Some of the blend modes require conversion to and from the hue, saturation, luminosity (HSL) color space to RGB.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="23da3-153">Enumeración</span><span class="sxs-lookup"><span data-stu-id="23da3-153">Enumeration</span></span></th>
<th><span data-ttu-id="23da3-154">Ecuación</span><span class="sxs-lookup"><span data-stu-id="23da3-154">Equation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="23da3-155">D2D1_BLEND_MODE_DARKEN</span><span class="sxs-lookup"><span data-stu-id="23da3-155">D2D1_BLEND_MODE_DARKEN</span></span></td>
<td><span data-ttu-id="23da3-156">Fórmula básica de Blend solo para alpha.</span><span class="sxs-lookup"><span data-stu-id="23da3-156">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-darken-1.png" alt="mathematical formula for a darken effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="23da3-157">D2D1_BLEND_MODE_MULTIPLY</span><span class="sxs-lookup"><span data-stu-id="23da3-157">D2D1_BLEND_MODE_MULTIPLY</span></span></td>
<td><span data-ttu-id="23da3-158">Fórmula básica de Blend solo para alpha.</span><span class="sxs-lookup"><span data-stu-id="23da3-158">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-multiply-1.png" alt="Mathematical formula for a mutiply effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="23da3-159">D2D1_BLEND_MODE_COLOR_BURN</span><span class="sxs-lookup"><span data-stu-id="23da3-159">D2D1_BLEND_MODE_COLOR_BURN</span></span></td>
<td><span data-ttu-id="23da3-160">Fórmulas básicas de Blend con <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="23da3-160">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-colorburn-1.png" alt="Mathematical formula for a coor burn effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="23da3-161">D2D1_BLEND_MODE_LINEAR_BURN</span><span class="sxs-lookup"><span data-stu-id="23da3-161">D2D1_BLEND_MODE_LINEAR_BURN</span></span></td>
<td><span data-ttu-id="23da3-162">Fórmulas básicas de Blend con <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="23da3-162">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-linearburn-1.png" alt="Mathematical formula for a linear burn effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="23da3-163">D2D1_BLEND_MODE_DARKER_COLOR</span><span class="sxs-lookup"><span data-stu-id="23da3-163">D2D1_BLEND_MODE_DARKER_COLOR</span></span></td>
<td><span data-ttu-id="23da3-164">Fórmula básica de Blend solo para alpha.</span><span class="sxs-lookup"><span data-stu-id="23da3-164">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-darkencolor-1.png" alt="Mathematical formla for a darken color effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="23da3-165">D2D1_BLEND_MODE_LIGHTEN</span><span class="sxs-lookup"><span data-stu-id="23da3-165">D2D1_BLEND_MODE_LIGHTEN</span></span></td>
<td><span data-ttu-id="23da3-166">Fórmula básica de Blend solo para alpha.</span><span class="sxs-lookup"><span data-stu-id="23da3-166">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-lighten-1.png" alt="Mathematical formula for a lighten effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="23da3-167">D2D1_BLEND_MODE_SCREEN</span><span class="sxs-lookup"><span data-stu-id="23da3-167">D2D1_BLEND_MODE_SCREEN</span></span></td>
<td><span data-ttu-id="23da3-168">Fórmula básica de Blend solo para alpha.</span><span class="sxs-lookup"><span data-stu-id="23da3-168">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-screen-1.png" alt="Mathematical formula for a screen effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="23da3-169">D2D1_BLEND_MODE_COLOR_DODGE</span><span class="sxs-lookup"><span data-stu-id="23da3-169">D2D1_BLEND_MODE_COLOR_DODGE</span></span></td>
<td><span data-ttu-id="23da3-170">Fórmulas básicas de Blend con <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="23da3-170">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-colordodge-1.png" alt="Mathematical formula for a color dodge effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="23da3-171">D2D1_BLEND_MODE_LINEAR_DODGE</span><span class="sxs-lookup"><span data-stu-id="23da3-171">D2D1_BLEND_MODE_LINEAR_DODGE</span></span></td>
<td><span data-ttu-id="23da3-172">Fórmulas básicas de Blend con <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="23da3-172">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-lineardodge-1.png" alt="Mathematical formula for a linear dodge effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="23da3-173">D2D1_BLEND_MODE_LIGHTER_COLOR</span><span class="sxs-lookup"><span data-stu-id="23da3-173">D2D1_BLEND_MODE_LIGHTER_COLOR</span></span></td>
<td><span data-ttu-id="23da3-174">Fórmula básica de Blend solo para alpha.</span><span class="sxs-lookup"><span data-stu-id="23da3-174">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-lightercolor-1.png" alt="Mathematical formula for a lighter color effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="23da3-175">D2D1_BLEND_MODE_OVERLAY</span><span class="sxs-lookup"><span data-stu-id="23da3-175">D2D1_BLEND_MODE_OVERLAY</span></span></td>
<td><span data-ttu-id="23da3-176">Fórmulas básicas de Blend con <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="23da3-176">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-overlay-1.png" alt="Mathematical formula for an overlay effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="23da3-177">D2D1_BLEND_MODE_SOFT_LIGHT</span><span class="sxs-lookup"><span data-stu-id="23da3-177">D2D1_BLEND_MODE_SOFT_LIGHT</span></span></td>
<td><span data-ttu-id="23da3-178">Fórmulas básicas de Blend con <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="23da3-178">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-softlight-1.png" alt="Mathematical formula for a soft light effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="23da3-179">D2D1_BLEND_MODE_HARD_LIGHT</span><span class="sxs-lookup"><span data-stu-id="23da3-179">D2D1_BLEND_MODE_HARD_LIGHT</span></span></td>
<td><span data-ttu-id="23da3-180">Fórmulas básicas de Blend con <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="23da3-180">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-hardlight-1.png" alt="Mathematical formula for a hard light effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="23da3-181">D2D1_BLEND_MODE_VIVID_LIGHT</span><span class="sxs-lookup"><span data-stu-id="23da3-181">D2D1_BLEND_MODE_VIVID_LIGHT</span></span></td>
<td><span data-ttu-id="23da3-182">Fórmulas básicas de Blend con <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="23da3-182">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-vividlight-1.png" alt="Mathematical formula for a vivid light effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="23da3-183">D2D1_BLEND_MODE_LINEAR_LIGHT</span><span class="sxs-lookup"><span data-stu-id="23da3-183">D2D1_BLEND_MODE_LINEAR_LIGHT</span></span></td>
<td><span data-ttu-id="23da3-184">Fórmulas básicas de Blend con <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="23da3-184">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-linearlight-1.png" alt="Mathematical formula for a linear light effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="23da3-185">D2D1_BLEND_MODE_PIN_LIGHT</span><span class="sxs-lookup"><span data-stu-id="23da3-185">D2D1_BLEND_MODE_PIN_LIGHT</span></span></td>
<td><span data-ttu-id="23da3-186">Fórmulas básicas de Blend con <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="23da3-186">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-pinlight-1.png" alt="Mathematical formula for a pin light effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="23da3-187">D2D1_BLEND_MODE_HARD_MIX</span><span class="sxs-lookup"><span data-stu-id="23da3-187">D2D1_BLEND_MODE_HARD_MIX</span></span></td>
<td><span data-ttu-id="23da3-188">Fórmulas básicas de Blend con <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="23da3-188">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-hardmix-1.png" alt="Mathematical formula for a hard mix effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="23da3-189">D2D1_BLEND_MODE_DIFFERENCE</span><span class="sxs-lookup"><span data-stu-id="23da3-189">D2D1_BLEND_MODE_DIFFERENCE</span></span></td>
<td><span data-ttu-id="23da3-190">Fórmulas básicas de Blend con <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = ABS (f<sub>RGB</sub> - B<sub>RGB</sub>)</span><span class="sxs-lookup"><span data-stu-id="23da3-190">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) = abs(F<sub>RGB</sub> - B<sub>RGB</sub>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="23da3-191">D2D1_BLEND_MODE_EXCLUSION</span><span class="sxs-lookup"><span data-stu-id="23da3-191">D2D1_BLEND_MODE_EXCLUSION</span></span></td>
<td><span data-ttu-id="23da3-192">Fórmulas básicas de Blend con <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = F<sub>RGB</sub> + b<sub>RGB</sub>   2 \* f<sub>RGB</sub> \* b<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="23da3-192">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) = F<sub>RGB</sub> + B<sub>RGB</sub>   2 \* F<sub>RGB</sub> \* B<sub>RGB</sub></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="23da3-193">D2D1_BLEND_MODE_HUE</span><span class="sxs-lookup"><span data-stu-id="23da3-193">D2D1_BLEND_MODE_HUE</span></span></td>
<td><span data-ttu-id="23da3-194">Fórmula básica de Blend solo para alpha.</span><span class="sxs-lookup"><span data-stu-id="23da3-194">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-hue-1.png" alt="Mathematical formula for a hue blend effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="23da3-195">D2D1_BLEND_MODE_SATURATION</span><span class="sxs-lookup"><span data-stu-id="23da3-195">D2D1_BLEND_MODE_SATURATION</span></span></td>
<td><span data-ttu-id="23da3-196">Fórmula básica de Blend solo para alpha.</span><span class="sxs-lookup"><span data-stu-id="23da3-196">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-saturation-1.png" alt="Mathematical formula for a sturation blend effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="23da3-197">D2D1_BLEND_MODE_COLOR</span><span class="sxs-lookup"><span data-stu-id="23da3-197">D2D1_BLEND_MODE_COLOR</span></span></td>
<td><span data-ttu-id="23da3-198">Fórmula básica de Blend solo para alpha.</span><span class="sxs-lookup"><span data-stu-id="23da3-198">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-color-1.png" alt="Mathematical formula for a color blend effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="23da3-199">D2D1_BLEND_MODE_LUMINOSITY</span><span class="sxs-lookup"><span data-stu-id="23da3-199">D2D1_BLEND_MODE_LUMINOSITY</span></span></td>
<td><span data-ttu-id="23da3-200">Fórmula básica de Blend solo para alpha.</span><span class="sxs-lookup"><span data-stu-id="23da3-200">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-luminosity-1.png" alt="Mathematical formula for a luminosity blend effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="23da3-201">D2D1_BLEND_MODE_DISSOLVE</span><span class="sxs-lookup"><span data-stu-id="23da3-201">D2D1_BLEND_MODE_DISSOLVE</span></span></td>
<td><span data-ttu-id="23da3-202">Con estas premisas:</span><span class="sxs-lookup"><span data-stu-id="23da3-202">Given:</span></span>
<ul>
<li><span data-ttu-id="23da3-203">Coordenadas de la escena XY para el píxel actual.</span><span class="sxs-lookup"><span data-stu-id="23da3-203">A scene coordinate XY for the current pixel</span></span></li>
<li><span data-ttu-id="23da3-204">El generador de números pseudoaleatorios deterministas Rand (XY) basado en la coordenada de inicialización XY, con distribución no sesgada de valores de [0, 1]</span><span class="sxs-lookup"><span data-stu-id="23da3-204">A deterministic pseudo-random number generator rand(XY) based on seed coordinate XY, with unbiased distribution of values from [0, 1]</span></span></li>
</ul>
<br/> <img src="images/blend-mode-dissolve-1.png" alt="Mathematical formula for a dissolve blend effect." /><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="23da3-205">D2D1_BLEND_MODE_SUBTRACT</span><span class="sxs-lookup"><span data-stu-id="23da3-205">D2D1_BLEND_MODE_SUBTRACT</span></span></td>
<td><span data-ttu-id="23da3-206">Fórmula básica de Blend solo para alpha.</span><span class="sxs-lookup"><span data-stu-id="23da3-206">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-subtract-1.png" alt="Mathematical formula for a subtract blend effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="23da3-207">D2D1_BLEND_MODE_DIVISION</span><span class="sxs-lookup"><span data-stu-id="23da3-207">D2D1_BLEND_MODE_DIVISION</span></span></td>
<td><span data-ttu-id="23da3-208">Fórmula básica de Blend solo para alpha.</span><span class="sxs-lookup"><span data-stu-id="23da3-208">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-division-1.png" alt="Mathematical formula for a division blend effect." /></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="23da3-209">En todos los modos de fusión, el valor de salida se multiplica previamente y se fija en el intervalo de \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="23da3-209">For all Blend modes, the output value is premultiplied and clamped to the range \[0, 1\].</span></span>

 

## <a name="hsl-color-space-conversions"></a><span data-ttu-id="23da3-210">Conversiones de espacio de color HSL</span><span class="sxs-lookup"><span data-stu-id="23da3-210">HSL color space conversions</span></span>

<span data-ttu-id="23da3-211">El componente luminosidad se calcula con los pesos RGB aquí:</span><span class="sxs-lookup"><span data-stu-id="23da3-211">The luminosity component is computed using the RGB weights here:</span></span>

-   <span data-ttu-id="23da3-212">*k*<sub>R</sub> = 0,30</span><span class="sxs-lookup"><span data-stu-id="23da3-212">*k*<sub>R</sub> = 0.30</span></span>
-   <span data-ttu-id="23da3-213">*k*<sub>G</sub> = 0,59</span><span class="sxs-lookup"><span data-stu-id="23da3-213">*k*<sub>G</sub> = 0.59</span></span>
-   <span data-ttu-id="23da3-214">*k*<sub>B</sub> = 0,11</span><span class="sxs-lookup"><span data-stu-id="23da3-214">*k*<sub>B</sub> = 0.11</span></span>

### <a name="converting-from-rgb-to-hsl"></a><span data-ttu-id="23da3-215">Convertir de RGB a HSL</span><span class="sxs-lookup"><span data-stu-id="23da3-215">Converting from RGB to HSL</span></span>

![fórmula matemática que describe la transformación de color RGB a color HSL.](images/blend-rgb-to-hsl-1.png)

<span data-ttu-id="23da3-217">Esto coloca *S* y *L* en el intervalo \[ 0,0, 1,0 \] y *H* en el intervalo \[ -1,0, 5,0 \] .</span><span class="sxs-lookup"><span data-stu-id="23da3-217">This places *S* and *L* in the range \[0.0, 1.0\] and *H* in the range \[-1.0, 5.0\].</span></span>

### <a name="converting-from-hsl-to-rgb"></a><span data-ttu-id="23da3-218">Convertir de HSL a RGB</span><span class="sxs-lookup"><span data-stu-id="23da3-218">Converting from HSL to RGB</span></span>

<span data-ttu-id="23da3-219">Para convertir la otra manera, usamos el inverso de los cálculos anteriores.</span><span class="sxs-lookup"><span data-stu-id="23da3-219">To convert the other way we use the inverse of the previous calculations.</span></span>

<span data-ttu-id="23da3-220">Si *S* = 0, entonces *R*  =  *G*  =  *B*  =  *L*</span><span class="sxs-lookup"><span data-stu-id="23da3-220">If *S* = 0 then *R* = *G* = *B* = *L*</span></span>

<span data-ttu-id="23da3-221">De lo contrario, hay seis casos dependientes de matiz:</span><span class="sxs-lookup"><span data-stu-id="23da3-221">Otherwise there are six hue-dependant cases:</span></span>

<span data-ttu-id="23da3-222">Si *H* es mayor que 0, los valores se encuentran en el sector rojo/magenta donde *R*  >  *B*  >  *G*.</span><span class="sxs-lookup"><span data-stu-id="23da3-222">If *H* is greater than 0, the values are in the red/magenta sector where *R* > *B* > *G*.</span></span>

![equaiton matemático paso 1 de seis conversión del color HSL a RGB.](images/blend-hsl-to-rgb-1rm.png)

<span data-ttu-id="23da3-224">Si *H* es mayor o igual que 0 y menor que 1, los valores se encuentran en el sector rojo/amarillo donde *R*  >  *G*  >  *B*.</span><span class="sxs-lookup"><span data-stu-id="23da3-224">If *H* is greater than or equal to 0 and less than 1, the values are in the red/yellow sector where *R* > *G* > *B*.</span></span>

![equaiton matemático paso 2 de seis conversión del color HSL a RGB.](images/blend-hsl-to-rgb-1ry.png)

<span data-ttu-id="23da3-226">Si *H* es mayor o igual que 1 y menor que 2, los valores se encuentran en el sector amarillo/verde donde *G*  >  *R*  >  *B*.</span><span class="sxs-lookup"><span data-stu-id="23da3-226">If *H* is greater than or equal to 1 and less than 2, the values are in the yellow/green sector where *G* > *R* > *B*.</span></span>

![equaiton matemático paso tres de seis conversión del color HSL a RGB.](images/blend-hsl-to-rgb-1yg.png)

<span data-ttu-id="23da3-228">Si *H* es mayor o igual que 2 y menor que 3, los valores se encuentran en el sector verde/aguamarina donde *G*  >  *B*  >  *R*.</span><span class="sxs-lookup"><span data-stu-id="23da3-228">If *H* is greater than or equal to 2 and less than 3, the values are in the green/cyan sector where *G* > *B* > *R*.</span></span>

![equaiton matemático paso cuatro de seis conversión del color HSL a RGB.](images/blend-hsl-to-rgb-1gc.png)

<span data-ttu-id="23da3-230">Si *H* es mayor o igual que 3 y menor que 4, los valores se encuentran en el sector cian/azul donde *B*  >  *G*  >  *R*.</span><span class="sxs-lookup"><span data-stu-id="23da3-230">If *H* is greater than or equal to 3 and less than 4, the values are in the cyan/blue sector where *B* > *G* > *R*.</span></span>

![equaiton matemático paso cinco de seis conversión del color HSL a RGB.](images/blend-hsl-to-rgb-1cb.png)

<span data-ttu-id="23da3-232">Si *H* es mayor o igual que 4, los valores se encuentran en el sector azul/magenta donde *B*  >  *R*  >  *G*.</span><span class="sxs-lookup"><span data-stu-id="23da3-232">If *H* is greater than or equal to 4, the values are in the blue/magenta sector where *B* > *R* > *G*.</span></span>

![equaiton matemático paso seis de seis conversión del color HSL a RGB.](images/blend-hsl-to-rgb-1bm.png)

<span data-ttu-id="23da3-234">Dado que los modos de mezcla realizan combinaciones arbitrarias de componentes HSL de dos colores diferentes, es habitual que el valor RGB convertido sea fuera de gama, es decir, uno o varios componentes del canal pueden estar fuera del intervalo legal de \[ 0,0, 1,0 \] .</span><span class="sxs-lookup"><span data-stu-id="23da3-234">Because the blending modes make arbitrary combinations of HSL components from two different colors, it is common for the converted RGB value to be out-of-gamut, that is, one or more channel components may be outside the legal range of \[0.0, 1.0\].</span></span> <span data-ttu-id="23da3-235">Estos colores se vuelven a la gama reduciendo mínimamente la saturación, al tiempo que se conservan el matiz y la luminosidad:</span><span class="sxs-lookup"><span data-stu-id="23da3-235">These colors are brought back into gamut by minimally reducing the saturation, while preserving both hue and luminosity:</span></span>

![fórmula matemática que describe las correcciones necesarias para las instancias fuera de la gama.](images/blend-gamut-correction.png)

## <a name="output-bitmap"></a><span data-ttu-id="23da3-237">Mapa de bits de salida</span><span class="sxs-lookup"><span data-stu-id="23da3-237">Output bitmap</span></span>

<span data-ttu-id="23da3-238">El mapa de bits de salida para este efecto es siempre el tamaño de la Unión de las dos imágenes de entrada.</span><span class="sxs-lookup"><span data-stu-id="23da3-238">The output bitmap for this effect is always the size of the union of the two input images.</span></span>

## <a name="sample-code"></a><span data-ttu-id="23da3-239">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="23da3-239">Sample code</span></span>

<span data-ttu-id="23da3-240">Para obtener un ejemplo de este efecto, descargue el [ejemplo de modos de efecto compuesto de Direct2D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample).</span><span class="sxs-lookup"><span data-stu-id="23da3-240">For an example of this effect, download the [Direct2D composite effect modes sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample).</span></span>

## <a name="requirements"></a><span data-ttu-id="23da3-241">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23da3-241">Requirements</span></span>



| <span data-ttu-id="23da3-242">Requisito</span><span class="sxs-lookup"><span data-stu-id="23da3-242">Requirement</span></span> | <span data-ttu-id="23da3-243">Value</span><span class="sxs-lookup"><span data-stu-id="23da3-243">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="23da3-244">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23da3-244">Minimum supported client</span></span> | <span data-ttu-id="23da3-245">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="23da3-245">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="23da3-246">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23da3-246">Minimum supported server</span></span> | <span data-ttu-id="23da3-247">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="23da3-247">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="23da3-248">Encabezado</span><span class="sxs-lookup"><span data-stu-id="23da3-248">Header</span></span>                   | <span data-ttu-id="23da3-249">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="23da3-249">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="23da3-250">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="23da3-250">Library</span></span>                  | <span data-ttu-id="23da3-251">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="23da3-251">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="23da3-252">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="23da3-252">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23da3-253">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="23da3-253">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

