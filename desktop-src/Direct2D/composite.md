---
title: Efecto compuesto
description: Use el efecto compuesto para combinar dos o más imágenes. Este efecto tiene 13 modos compuestos distintos.
ms.assetid: 60b878e9-1bc6-40d4-ade3-4bbd5c822c55
keywords:
- efecto compuesto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9872a66d031e8307f911ec7270af81397a80276
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996540"
---
# <a name="composite-effect"></a><span data-ttu-id="0c932-105">Efecto compuesto</span><span class="sxs-lookup"><span data-stu-id="0c932-105">Composite effect</span></span>

<span data-ttu-id="0c932-106">Use el efecto compuesto para combinar dos o más imágenes.</span><span class="sxs-lookup"><span data-stu-id="0c932-106">Use the composite effect to combine 2 or more images.</span></span> <span data-ttu-id="0c932-107">Este efecto tiene 13 modos compuestos distintos.</span><span class="sxs-lookup"><span data-stu-id="0c932-107">This effect has 13 different composite modes.</span></span> <span data-ttu-id="0c932-108">T</span><span class="sxs-lookup"><span data-stu-id="0c932-108">T</span></span>

<span data-ttu-id="0c932-109">El efecto compuesto acepta 2 o más entradas.</span><span class="sxs-lookup"><span data-stu-id="0c932-109">The composite effect accepts 2 or more inputs.</span></span> <span data-ttu-id="0c932-110">Cuando se especifican dos imágenes, el destino es la primera entrada (índice 0) y el origen es la segunda entrada (Índice 1).</span><span class="sxs-lookup"><span data-stu-id="0c932-110">When you specify 2 images, destination is the first input (index 0) and the source is the second input (index 1).</span></span> <span data-ttu-id="0c932-111">Si especifica más de 2 entradas, las imágenes se componen a partir de la primera entrada y la segunda, etc.</span><span class="sxs-lookup"><span data-stu-id="0c932-111">If you specify more than 2 inputs the images are composited starting with the first input and the second and so on.</span></span>

<span data-ttu-id="0c932-112">Este efecto implementa todos los modos mediante la unidad de fusión de la unidad de procesamiento de gráficos (GPU).</span><span class="sxs-lookup"><span data-stu-id="0c932-112">This effect implements all of the modes using the blending unit of the graphics processing unit (GPU).</span></span>

<span data-ttu-id="0c932-113">El CLSID para este efecto es CLSID \_ D2D1Composite.</span><span class="sxs-lookup"><span data-stu-id="0c932-113">The CLSID for this effect is CLSID\_D2D1Composite.</span></span>

-   [<span data-ttu-id="0c932-114">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="0c932-114">Example image</span></span>](#example-image)
-   [<span data-ttu-id="0c932-115">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="0c932-115">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="0c932-116">Tipos de modo</span><span class="sxs-lookup"><span data-stu-id="0c932-116">Mode types</span></span>](#mode-types)
-   [<span data-ttu-id="0c932-117">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="0c932-117">Sample code</span></span>](#sample-code)
-   [<span data-ttu-id="0c932-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c932-118">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="0c932-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0c932-119">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="0c932-120">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="0c932-120">Example image</span></span>

<span data-ttu-id="0c932-121">En la imagen siguiente se muestran dos rectángulos redondeados del mismo tamaño que se superponen.</span><span class="sxs-lookup"><span data-stu-id="0c932-121">The image here shows 2 rounded rectangles of the same size that overlap.</span></span> <span data-ttu-id="0c932-122">El rectángulo azul es el origen y el rectángulo rojo es el destino.</span><span class="sxs-lookup"><span data-stu-id="0c932-122">The blue rectangle is the source and the red rectangle is the destination.</span></span> <span data-ttu-id="0c932-123">Las imágenes se han compuesto con el modo de origen sobre.</span><span class="sxs-lookup"><span data-stu-id="0c932-123">The images were composited with the Source Over mode.</span></span>

![imagen de ejemplo que muestra dos rectángulos redondeados del mismo tamaño que se superponen con el modo de origen sobre.](images/composite-over.png)

<span data-ttu-id="0c932-125">Este es otro ejemplo en el que se usa el modo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="0c932-125">Here's another example using the default mode.</span></span>



| <span data-ttu-id="0c932-126">Antes de la imagen 1</span><span class="sxs-lookup"><span data-stu-id="0c932-126">Before image 1</span></span>                                                          |
|-------------------------------------------------------------------------|
| ![primera imagen de origen antes del efecto.](images/default-before.jpg) |
| <span data-ttu-id="0c932-128">Antes de la imagen 2</span><span class="sxs-lookup"><span data-stu-id="0c932-128">Before image 2</span></span>                                                          |
| ![segunda imagen anterior al efecto.](images/3-composite(2of2).png)    |
| <span data-ttu-id="0c932-130">Después</span><span class="sxs-lookup"><span data-stu-id="0c932-130">After</span></span>                                                                   |
| ![la imagen después de la transformación.](images/3-composite.png)               |



 


```C++
ComPtr<ID2D1Effect> compositeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect);

compositeEffect->SetInput(0, bitmap);
compositeEffect->SetInput(1, bitmapTwo);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="0c932-132">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="0c932-132">Effect properties</span></span>



| <span data-ttu-id="0c932-133">Enumeración de índice y nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="0c932-133">Display name and index enumeration</span></span>                     | <span data-ttu-id="0c932-134">Tipo y valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="0c932-134">Type and default value</span></span>                                                          | <span data-ttu-id="0c932-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="0c932-135">Description</span></span>                   |
|--------------------------------------------------------|---------------------------------------------------------------------------------|-------------------------------|
| <span data-ttu-id="0c932-136">Mode</span><span class="sxs-lookup"><span data-stu-id="0c932-136">Mode</span></span><br/> <span data-ttu-id="0c932-137">Modo de D2D1 \_ composite \_ props \_</span><span class="sxs-lookup"><span data-stu-id="0c932-137">D2D1\_COMPOSITE\_PROP\_MODE</span></span><br/> | <span data-ttu-id="0c932-138">\_Modo compuesto \_ D2D1</span><span class="sxs-lookup"><span data-stu-id="0c932-138">D2D1\_COMPOSITE\_MODE</span></span><br/> <span data-ttu-id="0c932-139">\_Origen de \_ modo compuesto D2D1 \_ \_ sobre</span><span class="sxs-lookup"><span data-stu-id="0c932-139">D2D1\_COMPOSITE\_MODE\_SOURCE\_OVER</span></span><br/> | <span data-ttu-id="0c932-140">Modo utilizado para el efecto.</span><span class="sxs-lookup"><span data-stu-id="0c932-140">The mode used for the effect.</span></span> |



 

## <a name="mode-types"></a><span data-ttu-id="0c932-141">Tipos de modo</span><span class="sxs-lookup"><span data-stu-id="0c932-141">Mode types</span></span>

<span data-ttu-id="0c932-142">En la tabla siguiente se muestran los modos de este efecto.</span><span class="sxs-lookup"><span data-stu-id="0c932-142">The table here shows the modes of this effect.</span></span> <span data-ttu-id="0c932-143">Las ecuaciones que aparecen en la tabla usan estos elementos:</span><span class="sxs-lookup"><span data-stu-id="0c932-143">The equations listed in the table use these elements:</span></span>

-   <span data-ttu-id="0c932-144">O = salida</span><span class="sxs-lookup"><span data-stu-id="0c932-144">O = Output</span></span>
-   <span data-ttu-id="0c932-145">S = origen</span><span class="sxs-lookup"><span data-stu-id="0c932-145">S = Source</span></span>
-   <span data-ttu-id="0c932-146">SA = alfa de origen</span><span class="sxs-lookup"><span data-stu-id="0c932-146">SA = Source Alpha</span></span>
-   <span data-ttu-id="0c932-147">D = destino</span><span class="sxs-lookup"><span data-stu-id="0c932-147">D = Destination</span></span>
-   <span data-ttu-id="0c932-148">DA = alfa de destino</span><span class="sxs-lookup"><span data-stu-id="0c932-148">DA = Destination Alpha</span></span>



| <span data-ttu-id="0c932-149">Enumeración</span><span class="sxs-lookup"><span data-stu-id="0c932-149">Enumeration</span></span>                                  | <span data-ttu-id="0c932-150">Ecuación</span><span class="sxs-lookup"><span data-stu-id="0c932-150">Equation</span></span>                          | <span data-ttu-id="0c932-151">Tamaño del mapa de bits de salida</span><span class="sxs-lookup"><span data-stu-id="0c932-151">Output Bitmap Size</span></span>                                                                                      |
|----------------------------------------------|-----------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c932-152">\_Origen de \_ modo compuesto D2D1 \_ \_ sobre</span><span class="sxs-lookup"><span data-stu-id="0c932-152">D2D1\_COMPOSITE\_MODE\_SOURCE\_OVER</span></span>          | <span data-ttu-id="0c932-153">O = S + (1 SA) \* D</span><span class="sxs-lookup"><span data-stu-id="0c932-153">O = S + (1   SA) \* D</span></span>             | <span data-ttu-id="0c932-154">Unión de mapas de bits de origen y de destino</span><span class="sxs-lookup"><span data-stu-id="0c932-154">Union of source and destination bitmaps</span></span>                                                                 |
| <span data-ttu-id="0c932-155">\_Destino de \_ modo compuesto D2D1 \_ \_ sobre</span><span class="sxs-lookup"><span data-stu-id="0c932-155">D2D1\_COMPOSITE\_MODE\_DESTINATION\_OVER</span></span>     | <span data-ttu-id="0c932-156">O = (1 DA) \* S + D</span><span class="sxs-lookup"><span data-stu-id="0c932-156">O = (1   DA) \* S + D</span></span>             | <span data-ttu-id="0c932-157">Unión de mapas de bits de origen y de destino</span><span class="sxs-lookup"><span data-stu-id="0c932-157">Union of source and destination bitmaps</span></span>                                                                 |
| <span data-ttu-id="0c932-158">\_ \_ Origen de modo compuesto D2D1 \_ \_ en</span><span class="sxs-lookup"><span data-stu-id="0c932-158">D2D1\_COMPOSITE\_MODE\_SOURCE\_IN</span></span>            | <span data-ttu-id="0c932-159">O = DA \* S</span><span class="sxs-lookup"><span data-stu-id="0c932-159">O = DA \* S</span></span>                       | <span data-ttu-id="0c932-160">Intersección de los mapas de bits de origen y de destino</span><span class="sxs-lookup"><span data-stu-id="0c932-160">Intersection of source and destination bitmaps</span></span>                                                          |
| <span data-ttu-id="0c932-161">\_ \_ Destino de modo compuesto D2D1 \_ \_ en</span><span class="sxs-lookup"><span data-stu-id="0c932-161">D2D1\_COMPOSITE\_MODE\_DESTINATION\_IN</span></span>       | <span data-ttu-id="0c932-162">O = SA \* D</span><span class="sxs-lookup"><span data-stu-id="0c932-162">O = SA \* D</span></span>                       | <span data-ttu-id="0c932-163">Intersección de los mapas de bits de origen y de destino</span><span class="sxs-lookup"><span data-stu-id="0c932-163">Intersection of source and destination bitmaps</span></span>                                                          |
| <span data-ttu-id="0c932-164">\_Origen de \_ modo \_ compuesto \_ D2D1</span><span class="sxs-lookup"><span data-stu-id="0c932-164">D2D1\_COMPOSITE\_MODE\_SOURCE\_OUT</span></span>           | <span data-ttu-id="0c932-165">O = (1-DA) \* S</span><span class="sxs-lookup"><span data-stu-id="0c932-165">O = (1 - DA) \* S</span></span>                 | <span data-ttu-id="0c932-166">Región del mapa de bits de origen</span><span class="sxs-lookup"><span data-stu-id="0c932-166">Region of the source bitmap</span></span>                                                                             |
| <span data-ttu-id="0c932-167">\_Destino de \_ modo \_ compuesto \_ de D2D1</span><span class="sxs-lookup"><span data-stu-id="0c932-167">D2D1\_COMPOSITE\_MODE\_DESTINATION\_OUT</span></span>      | <span data-ttu-id="0c932-168">O = (1-SA) \* D</span><span class="sxs-lookup"><span data-stu-id="0c932-168">O = (1 - SA) \* D</span></span>                 | <span data-ttu-id="0c932-169">Región del mapa de bits de destino</span><span class="sxs-lookup"><span data-stu-id="0c932-169">Region of the destination bitmap</span></span>                                                                        |
| <span data-ttu-id="0c932-170">\_Origen de \_ modo \_ compuesto \_ D2D1 sobre</span><span class="sxs-lookup"><span data-stu-id="0c932-170">D2D1\_COMPOSITE\_MODE\_SOURCE\_ATOP</span></span>          | <span data-ttu-id="0c932-171">O = DA \* S + (1-SA) \* D</span><span class="sxs-lookup"><span data-stu-id="0c932-171">O = DA \* S + (1 - SA) \* D</span></span>       | <span data-ttu-id="0c932-172">Región del mapa de bits de destino</span><span class="sxs-lookup"><span data-stu-id="0c932-172">Region of the destination bitmap</span></span>                                                                        |
| <span data-ttu-id="0c932-173">\_Destino de \_ modo \_ compuesto \_ D2D1 sobre</span><span class="sxs-lookup"><span data-stu-id="0c932-173">D2D1\_COMPOSITE\_MODE\_DESTINATION\_ATOP</span></span>     | <span data-ttu-id="0c932-174">O = (1-DA) \* S + SA \* D</span><span class="sxs-lookup"><span data-stu-id="0c932-174">O = (1 - DA) \* S + SA \* D</span></span>       | <span data-ttu-id="0c932-175">Región del mapa de bits de origen</span><span class="sxs-lookup"><span data-stu-id="0c932-175">Region of the source bitmap</span></span>                                                                             |
| <span data-ttu-id="0c932-176">D2D1 \_ \_ modo compuesto \_ XOR</span><span class="sxs-lookup"><span data-stu-id="0c932-176">D2D1\_COMPOSITE\_MODE\_XOR</span></span>                   | <span data-ttu-id="0c932-177">O = (1-DA) \* S + (1-SA) \* D</span><span class="sxs-lookup"><span data-stu-id="0c932-177">O = (1 - DA) \* S + (1 - SA) \* D</span></span> | <span data-ttu-id="0c932-178">Unión de mapas de bits de origen y de destino</span><span class="sxs-lookup"><span data-stu-id="0c932-178">Union of source and destination bitmaps</span></span>                                                                 |
| <span data-ttu-id="0c932-179">D2D1 \_ \_ modo compuesto \_ más</span><span class="sxs-lookup"><span data-stu-id="0c932-179">D2D1\_COMPOSITE\_MODE\_PLUS</span></span>                  | <span data-ttu-id="0c932-180">O = S + D</span><span class="sxs-lookup"><span data-stu-id="0c932-180">O = S + D</span></span>                         | <span data-ttu-id="0c932-181">Unión de mapas de bits de origen y de destino</span><span class="sxs-lookup"><span data-stu-id="0c932-181">Union of source and destination bitmaps</span></span>                                                                 |
| <span data-ttu-id="0c932-182">D2D1 \_ \_ copia de \_ origen del modo compuesto \_</span><span class="sxs-lookup"><span data-stu-id="0c932-182">D2D1\_COMPOSITE\_MODE\_SOURCE\_COPY</span></span>          | <span data-ttu-id="0c932-183">O = S</span><span class="sxs-lookup"><span data-stu-id="0c932-183">O = S</span></span>                             | <span data-ttu-id="0c932-184">Región del mapa de bits de origen</span><span class="sxs-lookup"><span data-stu-id="0c932-184">Region of the source bitmap</span></span>                                                                             |
| <span data-ttu-id="0c932-185">D2D1 \_ \_ copia de \_ origen enlazada en modo compuesto \_ \_</span><span class="sxs-lookup"><span data-stu-id="0c932-185">D2D1\_COMPOSITE\_MODE\_BOUNDED\_SOURCE\_COPY</span></span> | <span data-ttu-id="0c932-186">O = S (solo cuando existe el origen)</span><span class="sxs-lookup"><span data-stu-id="0c932-186">O = S (only where source exists)</span></span>  | <span data-ttu-id="0c932-187">Unión de los mapas de bits de origen y de destino.</span><span class="sxs-lookup"><span data-stu-id="0c932-187">Union of source and destination bitmaps.</span></span> <span data-ttu-id="0c932-188">El destino no se sobrescribe cuando el origen no existe.</span><span class="sxs-lookup"><span data-stu-id="0c932-188">Destination is not overwritten where the source doesn't exist.</span></span> |
| <span data-ttu-id="0c932-189">Invertida de la \_ \_ máscara de modo compuesto \_ D2D1 \_</span><span class="sxs-lookup"><span data-stu-id="0c932-189">D2D1\_COMPOSITE\_MODE\_MASK\_INVERT</span></span>          | <span data-ttu-id="0c932-190">O = (1 D) \* S + (1 SA) \* D</span><span class="sxs-lookup"><span data-stu-id="0c932-190">O = (1   D) \* S + (1   SA) \* D</span></span>  | <span data-ttu-id="0c932-191">Unión de los mapas de bits de origen y de destino. Los valores alfa no se modifican.</span><span class="sxs-lookup"><span data-stu-id="0c932-191">Union of source and destination bitmaps.The alpha values are unchanged.</span></span>                                 |



 

<span data-ttu-id="0c932-192">En la ilustración siguiente se muestra un ejemplo de cada uno de los modos con imágenes que tienen una opacidad de 1,0 o 0,5.</span><span class="sxs-lookup"><span data-stu-id="0c932-192">The figure here shows an example of each of the modes with images that have an opacity of 1.0 or 0.5.</span></span>

![una imagen de ejemplo de cada uno de los modos con opacidad establecida en 1,0 o 0,5.](images/composite-types.png)

## <a name="sample-code"></a><span data-ttu-id="0c932-194">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="0c932-194">Sample code</span></span>

<span data-ttu-id="0c932-195">Para obtener un ejemplo de este efecto, descargue el [ejemplo de modos de efecto compuesto de Direct2D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample).</span><span class="sxs-lookup"><span data-stu-id="0c932-195">For an example of this effect, download the [Direct2D composite effect modes sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample).</span></span>

## <a name="requirements"></a><span data-ttu-id="0c932-196">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c932-196">Requirements</span></span>



| <span data-ttu-id="0c932-197">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c932-197">Requirement</span></span> | <span data-ttu-id="0c932-198">Value</span><span class="sxs-lookup"><span data-stu-id="0c932-198">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0c932-199">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0c932-199">Minimum supported client</span></span> | <span data-ttu-id="0c932-200">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="0c932-200">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="0c932-201">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0c932-201">Minimum supported server</span></span> | <span data-ttu-id="0c932-202">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="0c932-202">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="0c932-203">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0c932-203">Header</span></span>                   | <span data-ttu-id="0c932-204">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="0c932-204">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="0c932-205">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0c932-205">Library</span></span>                  | <span data-ttu-id="0c932-206">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="0c932-206">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="0c932-207">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0c932-207">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c932-208">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="0c932-208">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

