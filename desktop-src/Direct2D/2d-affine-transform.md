---
title: Efecto de transformación afín 2D
description: El efecto de transformación afín 2D aplica una transformación espacial a una imagen basada en una matriz de 3X2 mediante la transformación de matriz de Direct2D y cualquiera de los seis modos de interpolación.
ms.assetid: E8973EBE-764C-4220-BB1E-3BFD4853582D
keywords:
- Efecto de transformación afín 2D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3017992d34cd98095f01192ea948684a6b52e53
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151247"
---
# <a name="2d-affine-transform-effect"></a><span data-ttu-id="c260d-104">Efecto de transformación afín 2D</span><span class="sxs-lookup"><span data-stu-id="c260d-104">2D affine transform effect</span></span>

<span data-ttu-id="c260d-105">El efecto de transformación afín 2D aplica una transformación espacial a una imagen basada en una matriz de 3X2 mediante la [transformación](direct2d-transforms-overview.md) de matriz de Direct2D y cualquiera de los seis modos de interpolación.</span><span class="sxs-lookup"><span data-stu-id="c260d-105">The 2D affine transform effect applies a spatial transform to a image based on a 3X2 matrix using the Direct2D matrix [transform](direct2d-transforms-overview.md) and any of six interpolation modes.</span></span> <span data-ttu-id="c260d-106">Puede usar este efecto para girar, escalar, sesgar o traducir una imagen.</span><span class="sxs-lookup"><span data-stu-id="c260d-106">You can use this effect to rotate, scale, skew, or translate an image.</span></span> <span data-ttu-id="c260d-107">O bien, puede combinar estas operaciones.</span><span class="sxs-lookup"><span data-stu-id="c260d-107">Or, you can combine these operations.</span></span> <span data-ttu-id="c260d-108">Las transferencias afines conservan las líneas paralelas y la proporción de distancias entre los tres puntos de una imagen.</span><span class="sxs-lookup"><span data-stu-id="c260d-108">Affine transfers preserve parallel lines and the ratio of distances between any three points in an image.</span></span>

<span data-ttu-id="c260d-109">El CLSID para este efecto es CLSID \_ D2D12DAffineTransform.</span><span class="sxs-lookup"><span data-stu-id="c260d-109">The CLSID for this effect is CLSID\_D2D12DAffineTransform.</span></span>

-   [<span data-ttu-id="c260d-110">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="c260d-110">Example image</span></span>](#example-image)
-   [<span data-ttu-id="c260d-111">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="c260d-111">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="c260d-112">Modos de borde</span><span class="sxs-lookup"><span data-stu-id="c260d-112">Border modes</span></span>](#border-modes)
-   [<span data-ttu-id="c260d-113">Modos de interpolación</span><span class="sxs-lookup"><span data-stu-id="c260d-113">Interpolation modes</span></span>](#interpolation-modes)
-   [<span data-ttu-id="c260d-114">Mapa de bits de salida</span><span class="sxs-lookup"><span data-stu-id="c260d-114">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="c260d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c260d-115">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="c260d-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c260d-116">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="c260d-117">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="c260d-117">Example image</span></span>



| <span data-ttu-id="c260d-118">Antes</span><span class="sxs-lookup"><span data-stu-id="c260d-118">Before</span></span>                                                             |
|--------------------------------------------------------------------|
| ![imagen anterior al efecto.](images/default-before.jpg)         |
| <span data-ttu-id="c260d-120">Después</span><span class="sxs-lookup"><span data-stu-id="c260d-120">After</span></span>                                                              |
| ![la imagen después de la transformación.](images/21-2daffinetransform.png) |



 


```C++
ComPtr<ID2D1Effect> affineTransformEffect;
m_d2dContext->CreateEffect(CLSID_D2D12DAffineTransform, &affineTransformEffect);

affineTransformEffect->SetInput(0, bitmap);

D2D1_MATRIX_3X2_F matrix = D2D1::Matrix3x2F(0.9f, -0.1f,   0.1f, 0.9f,   8.0f, 45.0f);

affineTransformEffect->SetValue(D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX, matrix);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(affineTransformEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="c260d-122">Este efecto realiza esta operación matricial:</span><span class="sxs-lookup"><span data-stu-id="c260d-122">This effect performs this matrix operation:</span></span>

![operación de matriz afín](images/affine-matrix-calculation.png)

<span data-ttu-id="c260d-124">Aunque la matriz de entrada se define como una matriz 3x2, la última columna se rellena con 0, 0 y 1 para generar una matriz cuadrada.</span><span class="sxs-lookup"><span data-stu-id="c260d-124">Although the input matrix is defined as a 3x2 matrix, the last column is padded with 0, 0 and 1 to produce a square matrix.</span></span> <span data-ttu-id="c260d-125">Esto permite la multiplicación de matrices, por lo que las transformaciones se pueden concatenar en una sola matriz.</span><span class="sxs-lookup"><span data-stu-id="c260d-125">This allows for matrix multiplication, so that transforms can be concatenated into a single matrix.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="c260d-126">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="c260d-126">Effect properties</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c260d-127">Enumeración de índice y nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="c260d-127">Display name and index enumeration</span></span></th>
<th><span data-ttu-id="c260d-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="c260d-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c260d-129">InterpolationMode</span><span class="sxs-lookup"><span data-stu-id="c260d-129">InterpolationMode</span></span><br/> <span data-ttu-id="c260d-130">D2D1_2DAFFINETRANSFORM_PROP_INTERPOLATION_MODE</span><span class="sxs-lookup"><span data-stu-id="c260d-130">D2D1_2DAFFINETRANSFORM_PROP_INTERPOLATION_MODE</span></span><br/></td>
<td><span data-ttu-id="c260d-131">El modo de interpolación usado para escalar la imagen.</span><span class="sxs-lookup"><span data-stu-id="c260d-131">The interpolation mode used to scale the image.</span></span> <span data-ttu-id="c260d-132">Hay 6 modos de escala que abarcan la calidad y la velocidad.</span><span class="sxs-lookup"><span data-stu-id="c260d-132">There are 6 scale modes that range in quality and speed.</span></span><br/> <span data-ttu-id="c260d-133">El tipo es D2D1_2DAFFINETRANSFORM_INTERPOLATION_MODE.</span><span class="sxs-lookup"><span data-stu-id="c260d-133">Type is D2D1_2DAFFINETRANSFORM_INTERPOLATION_MODE.</span></span><br/> <span data-ttu-id="c260d-134">El valor predeterminado es D2D1_2DAFFINETRANSFORM_INTERPOLATION_MODE_LINEAR.</span><span class="sxs-lookup"><span data-stu-id="c260d-134">Default value is D2D1_2DAFFINETRANSFORM_INTERPOLATION_MODE_LINEAR.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c260d-135">BorderMode</span><span class="sxs-lookup"><span data-stu-id="c260d-135">BorderMode</span></span><br/> <span data-ttu-id="c260d-136">D2D1_2DAFFINETRANSFORM_PROP_BORDER_MODE</span><span class="sxs-lookup"><span data-stu-id="c260d-136">D2D1_2DAFFINETRANSFORM_PROP_BORDER_MODE</span></span><br/></td>
<td><span data-ttu-id="c260d-137">El modo que se usa para calcular el borde de la imagen, es decir, es flexible o difícil.</span><span class="sxs-lookup"><span data-stu-id="c260d-137">The mode used to calculate the border of the image, soft or hard.</span></span> <span data-ttu-id="c260d-138">Vea <a href="https://www.bing.com/search?q=Border+modes">modos de borde</a> para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="c260d-138">See <a href="https://www.bing.com/search?q=Border+modes">Border modes</a> for more info.</span></span> <br/> <span data-ttu-id="c260d-139">El tipo es D2D1_BORDER_MODE.</span><span class="sxs-lookup"><span data-stu-id="c260d-139">Type is D2D1_BORDER_MODE.</span></span><br/> <span data-ttu-id="c260d-140">El valor predeterminado es D2D1_BORDER_MODE_SOFT.</span><span class="sxs-lookup"><span data-stu-id="c260d-140">Default value is D2D1_BORDER_MODE_SOFT.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c260d-141">TransformMatrix</span><span class="sxs-lookup"><span data-stu-id="c260d-141">TransformMatrix</span></span><br/> <span data-ttu-id="c260d-142">D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX</span><span class="sxs-lookup"><span data-stu-id="c260d-142">D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX</span></span><br/></td>
<td><span data-ttu-id="c260d-143">Matriz de 3x2 que se va a usar para transformar la imagen mediante la <a href="direct2d-transforms-overview.md">transformación</a>de matriz de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="c260d-143">The 3x2 matrix to transform the image using the Direct2D matrix <a href="direct2d-transforms-overview.md">transform</a>.</span></span> <br/> <span data-ttu-id="c260d-144">El tipo es D2D1_MATRIX_3X2_F.</span><span class="sxs-lookup"><span data-stu-id="c260d-144">Type is D2D1_MATRIX_3X2_F.</span></span><br/> <span data-ttu-id="c260d-145">El valor predeterminado es Matrix3x2F:: Identity ().</span><span class="sxs-lookup"><span data-stu-id="c260d-145">Default value is Matrix3x2F::Identity().</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c260d-146">Nitidez</span><span class="sxs-lookup"><span data-stu-id="c260d-146">Sharpness</span></span><br/> <span data-ttu-id="c260d-147">D2D1_2DAFFINETRANSFORM_PROP_SHARPNESS</span><span class="sxs-lookup"><span data-stu-id="c260d-147">D2D1_2DAFFINETRANSFORM_PROP_SHARPNESS</span></span><br/></td>
<td><span data-ttu-id="c260d-148">En el modo de interpolación cúbico de alta calidad, el nivel de nitidez del filtro de escalado es un valor de tipo float entre 0 y 1.</span><span class="sxs-lookup"><span data-stu-id="c260d-148">In the high quality cubic interpolation mode, the sharpness level of the scaling filter as a float between 0 and 1.</span></span> <span data-ttu-id="c260d-149">Los valores son no unitarias.</span><span class="sxs-lookup"><span data-stu-id="c260d-149">The values are unitless.</span></span> <span data-ttu-id="c260d-150">Puede usar la nitidez para ajustar la calidad de una imagen al escalar la imagen.</span><span class="sxs-lookup"><span data-stu-id="c260d-150">You can use sharpness to adjust the quality of an image when you scale the image.</span></span><br/> <span data-ttu-id="c260d-151">El factor de nitidez afecta a la forma del kernel.</span><span class="sxs-lookup"><span data-stu-id="c260d-151">The sharpness factor affects the shape of the kernel.</span></span> <span data-ttu-id="c260d-152">Cuanto mayor sea el factor de nitidez, menor será el kernel.</span><span class="sxs-lookup"><span data-stu-id="c260d-152">The higher the sharpness factor, the smaller the kernel.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="c260d-153">Esta propiedad solo afecta al modo de interpolación cúbico de alta calidad.</span><span class="sxs-lookup"><span data-stu-id="c260d-153">This property affects only the high quality cubic interpolation mode.</span></span>
</blockquote>
<br/> <span data-ttu-id="c260d-154">El tipo es FLOAT.</span><span class="sxs-lookup"><span data-stu-id="c260d-154">Type is FLOAT.</span></span><br/> <span data-ttu-id="c260d-155">El valor predeterminado es 1.0 f.</span><span class="sxs-lookup"><span data-stu-id="c260d-155">Default value is 1.0f.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="border-modes"></a><span data-ttu-id="c260d-156">Modos de borde</span><span class="sxs-lookup"><span data-stu-id="c260d-156">Border modes</span></span>



| <span data-ttu-id="c260d-157">Nombre</span><span class="sxs-lookup"><span data-stu-id="c260d-157">Name</span></span>                     | <span data-ttu-id="c260d-158">Descripción</span><span class="sxs-lookup"><span data-stu-id="c260d-158">Description</span></span>                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c260d-159">D2D1 \_ modo de borde \_ \_ flexible</span><span class="sxs-lookup"><span data-stu-id="c260d-159">D2D1\_BORDER\_MODE\_SOFT</span></span> | <span data-ttu-id="c260d-160">El efecto rellena la imagen con píxeles negros transparentes mientras se interpola, lo que da lugar a un borde flexible.</span><span class="sxs-lookup"><span data-stu-id="c260d-160">The effect pads the image with transparent black pixels as it interpolates, resulting in a soft edge.</span></span><br/> |
| <span data-ttu-id="c260d-161">D2D1 \_ del \_ modo de borde \_</span><span class="sxs-lookup"><span data-stu-id="c260d-161">D2D1\_BORDER\_MODE\_HARD</span></span> | <span data-ttu-id="c260d-162">El efecto fija la salida al tamaño de la imagen de entrada.</span><span class="sxs-lookup"><span data-stu-id="c260d-162">The effect clamps the output to the size of the input image.</span></span> <br/>                                         |



 

## <a name="interpolation-modes"></a><span data-ttu-id="c260d-163">Modos de interpolación</span><span class="sxs-lookup"><span data-stu-id="c260d-163">Interpolation modes</span></span>



| <span data-ttu-id="c260d-164">Enumeración</span><span class="sxs-lookup"><span data-stu-id="c260d-164">Enumeration</span></span>                                                         | <span data-ttu-id="c260d-165">Descripción</span><span class="sxs-lookup"><span data-stu-id="c260d-165">Description</span></span>                                                                                                                                                                                          |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c260d-166">D2D1 \_ el \_ modo de interpolación 2DAFFINETRANSFORM \_ \_ más cercano \_</span><span class="sxs-lookup"><span data-stu-id="c260d-166">D2D1\_2DAFFINETRANSFORM\_INTERPOLATION\_MODE\_NEAREST\_NEIGHBOR</span></span>     | <span data-ttu-id="c260d-167">Muestrea el punto único más cercano y lo usa.</span><span class="sxs-lookup"><span data-stu-id="c260d-167">Samples the nearest single point and uses that.</span></span> <span data-ttu-id="c260d-168">Este modo utiliza menos tiempo de procesamiento, pero genera la imagen de menor calidad.</span><span class="sxs-lookup"><span data-stu-id="c260d-168">This mode uses less processing time, but outputs the lowest quality image.</span></span>                                                                           |
| <span data-ttu-id="c260d-169">D2D1 \_ \_ modo de interpolación 2DAFFINETRANSFORM \_ \_ lineal</span><span class="sxs-lookup"><span data-stu-id="c260d-169">D2D1\_2DAFFINETRANSFORM\_INTERPOLATION\_MODE\_LINEAR</span></span>                | <span data-ttu-id="c260d-170">Utiliza un ejemplo de cuatro puntos y una interpolación lineal.</span><span class="sxs-lookup"><span data-stu-id="c260d-170">Uses a four point sample and linear interpolation.</span></span> <span data-ttu-id="c260d-171">Este modo usa más tiempo de procesamiento que el modo vecino más cercano, pero genera una imagen de mayor calidad.</span><span class="sxs-lookup"><span data-stu-id="c260d-171">This mode uses more processing time than the nearest neighbor mode, but outputs a higher quality image.</span></span>                                           |
| <span data-ttu-id="c260d-172">D2D1 \_ \_ modo de interpolación 2DAFFINETRANSFORM \_ \_ cúbico</span><span class="sxs-lookup"><span data-stu-id="c260d-172">D2D1\_2DAFFINETRANSFORM\_INTERPOLATION\_MODE\_CUBIC</span></span>                 | <span data-ttu-id="c260d-173">Usa un kernel cúbico de ejemplo 16 para la interpolación.</span><span class="sxs-lookup"><span data-stu-id="c260d-173">Uses a 16 sample cubic kernel for interpolation.</span></span> <span data-ttu-id="c260d-174">Este modo utiliza la mayor parte del tiempo de procesamiento, pero genera una imagen de mayor calidad.</span><span class="sxs-lookup"><span data-stu-id="c260d-174">This mode uses the most processing time, but outputs a higher quality image.</span></span>                                                                        |
| <span data-ttu-id="c260d-175">D2D1 \_ 2DAFFINETRANSFORM \_ modo de interpolación \_ \_ lineal de varios \_ ejemplos \_</span><span class="sxs-lookup"><span data-stu-id="c260d-175">D2D1\_2DAFFINETRANSFORM\_INTERPOLATION\_MODE\_MULTI\_SAMPLE\_LINEAR</span></span> | <span data-ttu-id="c260d-176">Usa 4 muestras lineales dentro de un solo píxel para el suavizado de contorno adecuado.</span><span class="sxs-lookup"><span data-stu-id="c260d-176">Uses 4 linear samples within a single pixel for good edge anti-aliasing.</span></span> <span data-ttu-id="c260d-177">Este modo es adecuado para reducir verticalmente en pequeñas cantidades de imágenes con pocos píxeles.</span><span class="sxs-lookup"><span data-stu-id="c260d-177">This mode is good for scaling down by small amounts on images with few pixels.</span></span>                                              |
| <span data-ttu-id="c260d-178">D2D1 \_ \_ modo de interpolación 2DAFFINETRANSFORM \_ \_ anisotrópico</span><span class="sxs-lookup"><span data-stu-id="c260d-178">D2D1\_2DAFFINETRANSFORM\_INTERPOLATION\_MODE\_ANISOTROPIC</span></span>           | <span data-ttu-id="c260d-179">Utiliza el filtrado anisotrópico para muestrear un patrón según la forma transformada del mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="c260d-179">Uses anisotropic filtering to sample a pattern according to the transformed shape of the bitmap.</span></span>                                                                                                     |
| <span data-ttu-id="c260d-180">D2D1 \_ 2DAFFINETRANSFORM \_ modo de interpolación de \_ \_ alta \_ calidad \_ cúbico</span><span class="sxs-lookup"><span data-stu-id="c260d-180">D2D1\_2DAFFINETRANSFORM\_INTERPOLATION\_MODE\_HIGH\_QUALITY\_CUBIC</span></span>  | <span data-ttu-id="c260d-181">Usa un kernel cúbico de alta calidad de tamaño variable para realizar una downscale previa de la imagen si downscaling está implicado en la matriz de transformación.</span><span class="sxs-lookup"><span data-stu-id="c260d-181">Uses a variable size high quality cubic kernel to perform a pre-downscale the image if downscaling is involved in the transform matrix.</span></span> <span data-ttu-id="c260d-182">A continuación, usa el modo de interpolación cúbico para la salida final.</span><span class="sxs-lookup"><span data-stu-id="c260d-182">Then uses the cubic interpolation mode for the final output.</span></span> |



 

> [!Note]  
> <span data-ttu-id="c260d-183">Si no selecciona un modo, el efecto tiene como valor predeterminado el \_ \_ modo de interpolación D2D1 2DAFFINETRANSFORM \_ \_ lineal.</span><span class="sxs-lookup"><span data-stu-id="c260d-183">If you don't select a mode, the effect defaults to D2D1\_2DAFFINETRANSFORM\_INTERPOLATION\_MODE\_LINEAR.</span></span>

 

> [!Note]  
> <span data-ttu-id="c260d-184">El modo anisotrópico genera mapas MIP al escalar; sin embargo, si establece la propiedad **Cached** en true en los efectos que se aplican a este efecto, no se generarán los mapas MIP cada vez para imágenes suficientemente pequeñas.</span><span class="sxs-lookup"><span data-stu-id="c260d-184">Anisotropic mode generates mipmaps when scaling, however, if you set the **Cached** property to true on the effects that are input to this effect, the mipmaps won't be generated every time for sufficiently small images.</span></span>

 

## <a name="output-bitmap"></a><span data-ttu-id="c260d-185">Mapa de bits de salida</span><span class="sxs-lookup"><span data-stu-id="c260d-185">Output bitmap</span></span>

<span data-ttu-id="c260d-186">El tamaño del mapa de bits de salida depende de la matriz de transformación que se aplica a la imagen.</span><span class="sxs-lookup"><span data-stu-id="c260d-186">The size of the output bitmap depends on the transform matrix that is applied to the image.</span></span>

<span data-ttu-id="c260d-187">El efecto realiza la operación de transformación y, a continuación, aplica un cuadro de límite alrededor del resultado.</span><span class="sxs-lookup"><span data-stu-id="c260d-187">The effect performs the transform operation and then applies a bounding box around the result.</span></span> <span data-ttu-id="c260d-188">El mapa de bits de salida es el tamaño del cuadro de límite.</span><span class="sxs-lookup"><span data-stu-id="c260d-188">The output bitmap is the size of the bounding box.</span></span>

## <a name="requirements"></a><span data-ttu-id="c260d-189">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c260d-189">Requirements</span></span>



| <span data-ttu-id="c260d-190">Requisito</span><span class="sxs-lookup"><span data-stu-id="c260d-190">Requirement</span></span> | <span data-ttu-id="c260d-191">Value</span><span class="sxs-lookup"><span data-stu-id="c260d-191">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c260d-192">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c260d-192">Minimum supported client</span></span> | <span data-ttu-id="c260d-193">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="c260d-193">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="c260d-194">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c260d-194">Minimum supported server</span></span> | <span data-ttu-id="c260d-195">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="c260d-195">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="c260d-196">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c260d-196">Header</span></span>                   | <span data-ttu-id="c260d-197">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="c260d-197">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="c260d-198">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c260d-198">Library</span></span>                  | <span data-ttu-id="c260d-199">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="c260d-199">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="c260d-200">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c260d-200">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c260d-201">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="c260d-201">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

