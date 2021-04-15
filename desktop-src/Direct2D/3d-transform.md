---
title: Efecto de transformación 3D
description: Utilice el efecto transformación 3D para aplicar una matriz de transformación 4x4 arbitraria a una imagen.
ms.assetid: BC2F2837-40F0-4293-A190-8B5F81BB01B6
keywords:
- efecto transformación 3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fabe0c2c220038802b5218b54187a1ff89268bfa
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/28/2021
ms.locfileid: "104570407"
---
# <a name="3d-transform-effect"></a><span data-ttu-id="52343-104">Efecto de transformación 3D</span><span class="sxs-lookup"><span data-stu-id="52343-104">3D transform effect</span></span>

<span data-ttu-id="52343-105">Utilice el efecto transformación 3D para aplicar una matriz de transformación 4x4 arbitraria a una imagen.</span><span class="sxs-lookup"><span data-stu-id="52343-105">Use the 3D transform effect to apply an arbitrary 4x4 transform matrix to an image.</span></span>

<span data-ttu-id="52343-106">Este efecto aplica la matriz (M?) que se proporciona a los vértices de esquina de la imagen de origen ( \[ x y z 1 \] ) mediante este cálculo:</span><span class="sxs-lookup"><span data-stu-id="52343-106">This effect applies the matrix (M?) you provide to the corner vertices of the source image (\[ x y z 1 \]) using this calculation:</span></span>

<span data-ttu-id="52343-107">\[x<sub>r</sub> y<sub>r</sub> z<sub>r</sub> 1 \] = \[ x y z 1 \] \* M?</span><span class="sxs-lookup"><span data-stu-id="52343-107">\[ x<sub>r</sub> y<sub>r</sub> z<sub>r</sub> 1 \]=\[ x y z 1 \]\*M?</span></span>

<span data-ttu-id="52343-108">El CLSID para este efecto es CLSID \_ D2D13DTransform.</span><span class="sxs-lookup"><span data-stu-id="52343-108">The CLSID for this effect is CLSID\_D2D13DTransform.</span></span>

-   [<span data-ttu-id="52343-109">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="52343-109">Example image</span></span>](#example-image)
-   [<span data-ttu-id="52343-110">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="52343-110">Effect properties</span></span>](#effect-properties)
    -   [<span data-ttu-id="52343-111">Modos de interpolación</span><span class="sxs-lookup"><span data-stu-id="52343-111">Interpolation modes</span></span>](#interpolation-modes)
    -   [<span data-ttu-id="52343-112">Modos de borde</span><span class="sxs-lookup"><span data-stu-id="52343-112">Border modes</span></span>](#border-modes)
-   [<span data-ttu-id="52343-113">4x4 Transform Matrix (clase)</span><span class="sxs-lookup"><span data-stu-id="52343-113">4x4 Transform Matrix Class</span></span>](#4x4-transform-matrix-class)
-   [<span data-ttu-id="52343-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52343-114">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="52343-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="52343-115">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="52343-116">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="52343-116">Example image</span></span>



| <span data-ttu-id="52343-117">Antes</span><span class="sxs-lookup"><span data-stu-id="52343-117">Before</span></span>                                                        |
|---------------------------------------------------------------|
| ![la imagen antes de la transformación.](images/default-before.jpg) |
| <span data-ttu-id="52343-119">Después</span><span class="sxs-lookup"><span data-stu-id="52343-119">After</span></span>                                                         |
| ![la imagen después de la transformación.](images/24-3dtransform.png)  |



 


```C++
ComPtr<ID2D1Effect> D2D13DTransformEffect;
m_d2dContext->CreateEffect(CLSID_D2D13DTransform, &D2D13DTransformEffect);

D2D13DTransformEffect->SetInput(0, bitmap);

// You can use the helper methods in D2D1::Matrix4x4F to create common matrix transformations.
D2D1_MATRIX_4X4_F matrix = 
    D2D1::Matrix4x4F::Translation(0.0f, -192.0f, 0.0f) *
    D2D1::Matrix4x4F::RotationY(30.0f) *
    D2D1::Matrix4x4F::Translation(0.0f, 192.0f, 0.0f);

D2D13DTransformEffect->SetValue(D2D1_3DTRANSFORM_PROP_TRANSFORM_MATRIX, matrix);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(D2D13DTransformEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="52343-121">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="52343-121">Effect properties</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="52343-122">Enumeración de índice y nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="52343-122">Display name and index enumeration</span></span></th>
<th><span data-ttu-id="52343-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="52343-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="52343-124">InterpolationMode</span><span class="sxs-lookup"><span data-stu-id="52343-124">InterpolationMode</span></span><br/> <span data-ttu-id="52343-125">D2D1_3DTRANSFORM_PROP_INTERPOLATION_MODE</span><span class="sxs-lookup"><span data-stu-id="52343-125">D2D1_3DTRANSFORM_PROP_INTERPOLATION_MODE</span></span><br/></td>
<td><span data-ttu-id="52343-126">El modo de interpolación que el efecto usa en la imagen.</span><span class="sxs-lookup"><span data-stu-id="52343-126">The interpolation mode the effect uses on the image.</span></span> <span data-ttu-id="52343-127">Hay 5 modos de escala que abarcan la calidad y la velocidad.</span><span class="sxs-lookup"><span data-stu-id="52343-127">There are 5 scale modes that range in quality and speed.</span></span><br/> <span data-ttu-id="52343-128">El tipo es D2D1_3DTRANSFORM_INTERPOLATION_MODE.</span><span class="sxs-lookup"><span data-stu-id="52343-128">Type is D2D1_3DTRANSFORM_INTERPOLATION_MODE.</span></span><br/> <span data-ttu-id="52343-129">El valor predeterminado es D2D1_3DTRANSFORM_INTERPOLATION_MODE_LINEAR.</span><span class="sxs-lookup"><span data-stu-id="52343-129">Default value is D2D1_3DTRANSFORM_INTERPOLATION_MODE_LINEAR.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="52343-130">BorderMode</span><span class="sxs-lookup"><span data-stu-id="52343-130">BorderMode</span></span><br/> <span data-ttu-id="52343-131">D2D1_3DTRANSFORM_PROP_BORDER_MODE</span><span class="sxs-lookup"><span data-stu-id="52343-131">D2D1_3DTRANSFORM_PROP_BORDER_MODE</span></span><br/></td>
<td><span data-ttu-id="52343-132">El modo que se usa para calcular el borde de la imagen, es decir, es flexible o difícil.</span><span class="sxs-lookup"><span data-stu-id="52343-132">The mode used to calculate the border of the image, soft or hard.</span></span> <span data-ttu-id="52343-133">Vea <a href="https://www.bing.com/search?q=Border+modes">modos de borde</a> para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="52343-133">See <a href="https://www.bing.com/search?q=Border+modes">Border modes</a> for more info.</span></span><br/> <span data-ttu-id="52343-134">El tipo es D2D1_BORDER_MODE.</span><span class="sxs-lookup"><span data-stu-id="52343-134">Type is D2D1_BORDER_MODE.</span></span><br/> <span data-ttu-id="52343-135">El valor predeterminado es D2D1_BORDER_MODE_SOFT.</span><span class="sxs-lookup"><span data-stu-id="52343-135">Default value is D2D1_BORDER_MODE_SOFT.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="52343-136">TransformMatrix</span><span class="sxs-lookup"><span data-stu-id="52343-136">TransformMatrix</span></span><br/> <span data-ttu-id="52343-137">D2D1_3DTRANSFORM_PROP_TRANSFORM_MATRIX</span><span class="sxs-lookup"><span data-stu-id="52343-137">D2D1_3DTRANSFORM_PROP_TRANSFORM_MATRIX</span></span><br/></td>
<td><span data-ttu-id="52343-138">Matriz de transformación 4x4 aplicada al plano de proyección.</span><span class="sxs-lookup"><span data-stu-id="52343-138">A 4x4 transform matrix applied to the projection plane.</span></span> <span data-ttu-id="52343-139">El siguiente cálculo de matriz se utiliza para asignar puntos de un sistema de coordenadas 3D al sistema de coordenadas 2D transformado.</span><span class="sxs-lookup"><span data-stu-id="52343-139">The following matrix calculation is used to map points from one 3D coordinate system to the transformed 2D coordinate system.</span></span> <br/><img src="images/3d-transform-matrix1.png" alt="3D Depth Matrix" /><span data-ttu-id="52343-140">Donde:</span><span class="sxs-lookup"><span data-stu-id="52343-140">Where:</span></span><dl> <span data-ttu-id="52343-141">X, Y, Z = coordenadas del plano de proyección de entrada</span><span class="sxs-lookup"><span data-stu-id="52343-141">X, Y, Z = Input projection plane coordinates</span></span><br />
<span data-ttu-id="52343-142">M<sub>x, y</sub> = transformar elementos de matriz</span><span class="sxs-lookup"><span data-stu-id="52343-142">M<sub>x,y</sub> = Transform Matrix elements</span></span><br />
<span data-ttu-id="52343-143">X, Y, Z = coordenadas del plano de proyección de salida</span><span class="sxs-lookup"><span data-stu-id="52343-143">X , Y , Z  =Output projection plane coordinates</span></span><br />
</dl> <br/> <span data-ttu-id="52343-144">Los elementos individuales de la matriz no están limitados y no tienen unidades.</span><span class="sxs-lookup"><span data-stu-id="52343-144">The individual matrix elements are not bounded and are unitless.</span></span> <br/> <span data-ttu-id="52343-145">El tipo es D2D1_MATRIX_4X4_F.</span><span class="sxs-lookup"><span data-stu-id="52343-145">Type is D2D1_MATRIX_4X4_F.</span></span><br/> <span data-ttu-id="52343-146">El valor predeterminado es Matrix4x4F (1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="52343-146">Default value is Matrix4x4F(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1).</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="interpolation-modes"></a><span data-ttu-id="52343-147">Modos de interpolación</span><span class="sxs-lookup"><span data-stu-id="52343-147">Interpolation modes</span></span>



| <span data-ttu-id="52343-148">Enumeración</span><span class="sxs-lookup"><span data-stu-id="52343-148">Enumeration</span></span>                                                   | <span data-ttu-id="52343-149">Descripción</span><span class="sxs-lookup"><span data-stu-id="52343-149">Description</span></span>                                                                                                                                                |
|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52343-150">D2D1 \_ el \_ modo de interpolación 3DTRANSFORM \_ \_ más cercano \_</span><span class="sxs-lookup"><span data-stu-id="52343-150">D2D1\_3DTRANSFORM\_INTERPOLATION\_MODE\_NEAREST\_NEIGHBOR</span></span>     | <span data-ttu-id="52343-151">Muestrea el punto único más cercano y lo usa.</span><span class="sxs-lookup"><span data-stu-id="52343-151">Samples the nearest single point and uses that.</span></span> <span data-ttu-id="52343-152">Este modo utiliza menos tiempo de procesamiento, pero genera la imagen de menor calidad.</span><span class="sxs-lookup"><span data-stu-id="52343-152">This mode uses less processing time, but outputs the lowest quality image.</span></span>                                 |
| <span data-ttu-id="52343-153">D2D1 \_ \_ modo de interpolación 3DTRANSFORM \_ \_ lineal</span><span class="sxs-lookup"><span data-stu-id="52343-153">D2D1\_3DTRANSFORM\_INTERPOLATION\_MODE\_LINEAR</span></span>                | <span data-ttu-id="52343-154">Utiliza un ejemplo de cuatro puntos y una interpolación lineal.</span><span class="sxs-lookup"><span data-stu-id="52343-154">Uses a four point sample and linear interpolation.</span></span> <span data-ttu-id="52343-155">Este modo usa más tiempo de procesamiento que el modo vecino más cercano, pero genera una imagen de mayor calidad.</span><span class="sxs-lookup"><span data-stu-id="52343-155">This mode uses more processing time than the nearest neighbor mode, but outputs a higher quality image.</span></span> |
| <span data-ttu-id="52343-156">D2D1 \_ \_ modo de interpolación 3DTRANSFORM \_ \_ cúbico</span><span class="sxs-lookup"><span data-stu-id="52343-156">D2D1\_3DTRANSFORM\_INTERPOLATION\_MODE\_CUBIC</span></span>                 | <span data-ttu-id="52343-157">Usa un kernel cúbico de ejemplo 16 para la interpolación.</span><span class="sxs-lookup"><span data-stu-id="52343-157">Uses a 16 sample cubic kernel for interpolation.</span></span> <span data-ttu-id="52343-158">Este modo utiliza la mayor parte del tiempo de procesamiento, pero genera una imagen de mayor calidad.</span><span class="sxs-lookup"><span data-stu-id="52343-158">This mode uses the most processing time, but outputs a higher quality image.</span></span>                              |
| <span data-ttu-id="52343-159">D2D1 \_ 3DTRANSFORM \_ modo de interpolación \_ \_ lineal de varios \_ ejemplos \_</span><span class="sxs-lookup"><span data-stu-id="52343-159">D2D1\_3DTRANSFORM\_INTERPOLATION\_MODE\_MULTI\_SAMPLE\_LINEAR</span></span> | <span data-ttu-id="52343-160">Usa 4 muestras lineales dentro de un solo píxel para el suavizado de contorno adecuado.</span><span class="sxs-lookup"><span data-stu-id="52343-160">Uses 4 linear samples within a single pixel for good edge anti-aliasing.</span></span> <span data-ttu-id="52343-161">Este modo es adecuado para reducir verticalmente en pequeñas cantidades de imágenes con pocos píxeles.</span><span class="sxs-lookup"><span data-stu-id="52343-161">This mode is good for scaling down by small amounts on images with few pixels.</span></span>    |
| <span data-ttu-id="52343-162">D2D1 \_ \_ modo de interpolación 3DTRANSFORM \_ \_ anisotrópico</span><span class="sxs-lookup"><span data-stu-id="52343-162">D2D1\_3DTRANSFORM\_INTERPOLATION\_MODE\_ANISOTROPIC</span></span>           | <span data-ttu-id="52343-163">Utiliza el filtrado anisotrópico para muestrear un patrón según la forma transformada del mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="52343-163">Uses anisotropic filtering to sample a pattern according to the transformed shape of the bitmap.</span></span>                                                           |



 

> [!Note]  
> <span data-ttu-id="52343-164">Si no selecciona un modo, el efecto tiene como valor predeterminado el \_ \_ modo de interpolación D2D1 3DTRANSFORM \_ \_ lineal.</span><span class="sxs-lookup"><span data-stu-id="52343-164">If you don't select a mode, the effect defaults to D2D1\_3DTRANSFORM\_INTERPOLATION\_MODE\_LINEAR.</span></span>

 

> [!Note]  
> <span data-ttu-id="52343-165">El modo anisotrópico genera mapas MIP al escalar; sin embargo, si establece la propiedad **Cached** en true en los efectos que se aplican a este efecto, no se generarán los mapas MIP cada vez para imágenes suficientemente pequeñas.</span><span class="sxs-lookup"><span data-stu-id="52343-165">Anisotropic mode generates mipmaps when scaling, however, if you set the **Cached** property to true on the effects that are input to this effect, the mipmaps won't be generated every time for sufficiently small images.</span></span>

 

### <a name="border-modes"></a><span data-ttu-id="52343-166">Modos de borde</span><span class="sxs-lookup"><span data-stu-id="52343-166">Border modes</span></span>



| <span data-ttu-id="52343-167">Nombre</span><span class="sxs-lookup"><span data-stu-id="52343-167">Name</span></span>                     | <span data-ttu-id="52343-168">Descripción</span><span class="sxs-lookup"><span data-stu-id="52343-168">Description</span></span>                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52343-169">D2D1 \_ modo de borde \_ \_ flexible</span><span class="sxs-lookup"><span data-stu-id="52343-169">D2D1\_BORDER\_MODE\_SOFT</span></span> | <span data-ttu-id="52343-170">El efecto rellena la imagen con píxeles negros transparentes mientras se interpola, lo que da lugar a un borde flexible.</span><span class="sxs-lookup"><span data-stu-id="52343-170">The effect pads the image with transparent black pixels as it interpolates, resulting in a soft edge.</span></span><br/> |
| <span data-ttu-id="52343-171">D2D1 \_ del \_ modo de borde \_</span><span class="sxs-lookup"><span data-stu-id="52343-171">D2D1\_BORDER\_MODE\_HARD</span></span> | <span data-ttu-id="52343-172">El efecto fija la salida al tamaño de la imagen de entrada.</span><span class="sxs-lookup"><span data-stu-id="52343-172">The effect clamps the output to the size of the input image.</span></span> <br/>                                         |



 

## <a name="4x4-transform-matrix-class"></a><span data-ttu-id="52343-173">4x4 Transform Matrix (clase)</span><span class="sxs-lookup"><span data-stu-id="52343-173">4x4 Transform Matrix Class</span></span>

<span data-ttu-id="52343-174">Direct2D proporciona una clase de matriz 4x4 para proporcionar funciones auxiliares para transformar la imagen en tres dimensiones.</span><span class="sxs-lookup"><span data-stu-id="52343-174">Direct2D provides a 4x4 matrix class to provide helper functions for transforming the image in 3 dimensions.</span></span> <span data-ttu-id="52343-175">Vea el tema [**Matrix4x4F**](/windows/desktop/api/d2d1_1helper/nl-d2d1_1helper-matrix4x4f) para obtener más información y una descripción de todos los miembros de clase.</span><span class="sxs-lookup"><span data-stu-id="52343-175">See the [**Matrix4x4F**](/windows/desktop/api/d2d1_1helper/nl-d2d1_1helper-matrix4x4f) topic for more info and a description of all the class members.</span></span>



| <span data-ttu-id="52343-176">Función</span><span class="sxs-lookup"><span data-stu-id="52343-176">Function</span></span>                                | <span data-ttu-id="52343-177">Descripción</span><span class="sxs-lookup"><span data-stu-id="52343-177">Description</span></span>                                                                                    | <span data-ttu-id="52343-178">Matrix</span><span class="sxs-lookup"><span data-stu-id="52343-178">Matrix</span></span>                                                 |
|-----------------------------------------|------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="52343-179">Matrix4x4F:: Scale (X, Y, Z)</span><span class="sxs-lookup"><span data-stu-id="52343-179">Matrix4x4F::Scale(X, Y, Z)</span></span>              | <span data-ttu-id="52343-180">Genera una matriz de transformación que escala el plano de proyección en la dirección X, y y/o Z.</span><span class="sxs-lookup"><span data-stu-id="52343-180">Generates a transform matrix that scales the projection plane in the X, Y, and/or Z direction.</span></span> | ![matriz scale3d](images/3d-transform-matrix2.png)     |
| <span data-ttu-id="52343-182">SkewX (X)</span><span class="sxs-lookup"><span data-stu-id="52343-182">SkewX(X)</span></span>                                | <span data-ttu-id="52343-183">Genera una matriz de transformación que sesga el plano de proyección en la dirección X.</span><span class="sxs-lookup"><span data-stu-id="52343-183">Generates a transform matrix that skews the projection plane in the X direction.</span></span>               | ![Muestra una matriz de sesgo en la dirección X.](images/matrix4x4-skewx.png)             |
| <span data-ttu-id="52343-185">Sesgado (Y)</span><span class="sxs-lookup"><span data-stu-id="52343-185">SkewY(Y)</span></span>                                | <span data-ttu-id="52343-186">Genera una matriz de transformación que sesga el plano de proyección en la dirección Y.</span><span class="sxs-lookup"><span data-stu-id="52343-186">Generates a transform matrix that skews the projection plane in the Y direction.</span></span>               | ![matriz de sesgo](images/matrix4x4-skewy.png)             |
| <span data-ttu-id="52343-188">Traducción (X, Y, Z)</span><span class="sxs-lookup"><span data-stu-id="52343-188">Translation(X, Y, Z)</span></span>                    | <span data-ttu-id="52343-189">Genera una matriz de transformación que convierte el plano de proyección en la dirección X, Y o Z.</span><span class="sxs-lookup"><span data-stu-id="52343-189">Generates a transform matrix that translates the projection plane in the X, Y, or Z direction.</span></span> | ![convertir matriz](images/3d-transform-matrix4.png)   |
| <span data-ttu-id="52343-191">RotationX (X)</span><span class="sxs-lookup"><span data-stu-id="52343-191">RotationX(X)</span></span>                            | <span data-ttu-id="52343-192">Genera una matriz de transformación que gira el plano de proyección sobre el eje X.</span><span class="sxs-lookup"><span data-stu-id="52343-192">Generates a transform matrix that rotates the projection plane about the X axis.</span></span>               | ![rotar matriz x](images/3d-transform-matrix5.png)    |
| <span data-ttu-id="52343-194">Rotación (Y)</span><span class="sxs-lookup"><span data-stu-id="52343-194">RotationY(Y)</span></span>                            | <span data-ttu-id="52343-195">Genera una matriz de transformación que gira el plano de proyección sobre el eje Y.</span><span class="sxs-lookup"><span data-stu-id="52343-195">Generates a transform matrix that rotates the projection plane about the Y axis.</span></span>               | ![rotar matriz y](images/3d-transform-matrix6.png)    |
| <span data-ttu-id="52343-197">RotationZ (Z)</span><span class="sxs-lookup"><span data-stu-id="52343-197">RotationZ(Z)</span></span>                            | <span data-ttu-id="52343-198">Genera una matriz de transformación que gira el plano de proyección sobre el eje Z.</span><span class="sxs-lookup"><span data-stu-id="52343-198">Generates a transform matrix that rotates the projection plane about the Z axis.</span></span>               | ![rotar matriz z](images/3d-transform-matrix7.png)    |
| <span data-ttu-id="52343-200">PerspectiveProjection (D)</span><span class="sxs-lookup"><span data-stu-id="52343-200">PerspectiveProjection(D)</span></span>                | <span data-ttu-id="52343-201">Transformación de perspectiva con un valor de profundidad de D.</span><span class="sxs-lookup"><span data-stu-id="52343-201">A perspective transformation with a depth value of D.</span></span>                                          | ![matriz de perspectiva](images/3d-transform-matrix8.png) |
| <span data-ttu-id="52343-203">RotationArbitraryAxis (X, Y, Z, grados)</span><span class="sxs-lookup"><span data-stu-id="52343-203">RotationArbitraryAxis(X, Y, Z, degrees)</span></span> | <span data-ttu-id="52343-204">Gira el plano de proyección sobre el eje especificado.</span><span class="sxs-lookup"><span data-stu-id="52343-204">Rotates the projection plane about the axis you specify.</span></span>                                       |                                                        |



 

## <a name="requirements"></a><span data-ttu-id="52343-205">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52343-205">Requirements</span></span>



| <span data-ttu-id="52343-206">Requisito</span><span class="sxs-lookup"><span data-stu-id="52343-206">Requirement</span></span> | <span data-ttu-id="52343-207">Value</span><span class="sxs-lookup"><span data-stu-id="52343-207">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="52343-208">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52343-208">Minimum supported client</span></span> | <span data-ttu-id="52343-209">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="52343-209">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="52343-210">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52343-210">Minimum supported server</span></span> | <span data-ttu-id="52343-211">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="52343-211">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="52343-212">Encabezado</span><span class="sxs-lookup"><span data-stu-id="52343-212">Header</span></span>                   | <span data-ttu-id="52343-213">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="52343-213">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="52343-214">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="52343-214">Library</span></span>                  | <span data-ttu-id="52343-215">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="52343-215">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="52343-216">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="52343-216">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52343-217">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="52343-217">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

