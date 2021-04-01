---
title: Efecto de transformación de perspectiva 3D
description: Use el efecto transformación de perspectiva 3D para girar la imagen en tres dimensiones, como si se viera desde una distancia.
ms.assetid: 0E1A940E-2DCA-4772-BB68-7E5EF5CEF833
keywords:
- efecto de transformación de perspectiva 3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ed2b1c5131319dd711d2c7802a0bfabceaaa32e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905671"
---
# <a name="3d-perspective-transform-effect"></a><span data-ttu-id="66ff3-104">Efecto de transformación de perspectiva 3D</span><span class="sxs-lookup"><span data-stu-id="66ff3-104">3D perspective transform effect</span></span>

<span data-ttu-id="66ff3-105">Use el efecto transformación de perspectiva 3D para girar la imagen en tres dimensiones, como si se viera desde una distancia.</span><span class="sxs-lookup"><span data-stu-id="66ff3-105">Use the 3D perspective transform effect to rotate the image in 3 dimensions as if viewed from a distance.</span></span>

<span data-ttu-id="66ff3-106">La transformación perspectiva 3D es más cómoda que el efecto transformación 3D, pero solo expone un subconjunto de la funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="66ff3-106">The 3D perspective transform is more convenient than the 3D transform effect, but only exposes a subset of the functionality.</span></span> <span data-ttu-id="66ff3-107">Puede calcular una matriz de transformación 3D completa y aplicar una matriz de transformación más arbitraria a una imagen mediante el efecto [transformación 3D](3d-transform.md) .</span><span class="sxs-lookup"><span data-stu-id="66ff3-107">You can compute a full 3D transformation matrix and apply a more arbitrary transform matrix to an image using the [3D transform](3d-transform.md) effect.</span></span>

<span data-ttu-id="66ff3-108">El CLSID para este efecto es CLSID \_ D2D13DPerspectiveTransform.</span><span class="sxs-lookup"><span data-stu-id="66ff3-108">The CLSID for this effect is CLSID\_D2D13DPerspectiveTransform.</span></span>

-   [<span data-ttu-id="66ff3-109">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="66ff3-109">Example image</span></span>](#example-image)
-   [<span data-ttu-id="66ff3-110">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="66ff3-110">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="66ff3-111">Modos de interpolación</span><span class="sxs-lookup"><span data-stu-id="66ff3-111">Interpolation modes</span></span>](#interpolation-modes)
-   [<span data-ttu-id="66ff3-112">Modos de borde</span><span class="sxs-lookup"><span data-stu-id="66ff3-112">Border modes</span></span>](#border-modes)
-   [<span data-ttu-id="66ff3-113">Mapa de bits de salida</span><span class="sxs-lookup"><span data-stu-id="66ff3-113">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="66ff3-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66ff3-114">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="66ff3-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="66ff3-115">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="66ff3-116">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="66ff3-116">Example image</span></span>



| <span data-ttu-id="66ff3-117">Antes</span><span class="sxs-lookup"><span data-stu-id="66ff3-117">Before</span></span>                                                               |
|----------------------------------------------------------------------|
| ![imagen anterior al efecto.](images/default-before.jpg)           |
| <span data-ttu-id="66ff3-119">Después</span><span class="sxs-lookup"><span data-stu-id="66ff3-119">After</span></span>                                                                |
| ![la imagen después del efecto.](images/23-3dperspectivetransform.png) |



 


```C++
ComPtr<ID2D1Effect> perspectiveTransformEffect;
m_d2dContext->CreateEffect(CLSID_D2D13DPerspectiveTransform, &perspectiveTransformEffect);

perspectiveTransformEffect->SetInput(0, bitmap);

perspectiveTransformEffect->SetValue(D2D1_3DPERSPECTIVETRANSFORM_PROP_PERSPECTIVE_ORIGIN, D2D1::Vector3F(0.0f, 192.0f, 0.0f));
perspectiveTransformEffect->SetValue(D2D1_3DPERSPECTIVETRANSFORM_PROP_ROTATION, D2D1::Vector3F(0.0f, 30.0f, 0.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(perspectiveTransformEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="66ff3-121">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="66ff3-121">Effect properties</span></span>



| <span data-ttu-id="66ff3-122">Enumeración de índice y nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="66ff3-122">Display name and index enumeration</span></span>                                                              | <span data-ttu-id="66ff3-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="66ff3-123">Description</span></span>                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66ff3-124">InterpolationMode</span><span class="sxs-lookup"><span data-stu-id="66ff3-124">InterpolationMode</span></span><br/> <span data-ttu-id="66ff3-125">\_Modo de \_ \_ interpolación de \_ propiedades de D2D1 3DPERSPECTIVETRANSFORM</span><span class="sxs-lookup"><span data-stu-id="66ff3-125">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_INTERPOLATION\_MODE</span></span><br/> | <span data-ttu-id="66ff3-126">El modo de interpolación que el efecto usa en la imagen.</span><span class="sxs-lookup"><span data-stu-id="66ff3-126">The interpolation mode the effect uses on the image.</span></span> <span data-ttu-id="66ff3-127">Hay 5 modos de escala que abarcan la calidad y la velocidad.</span><span class="sxs-lookup"><span data-stu-id="66ff3-127">There are 5 scale modes that range in quality and speed.</span></span><br/> <span data-ttu-id="66ff3-128">El tipo es D2D1 \_ 3DPERSPECTIVETRANSFORM \_ modo de interpolación \_ .</span><span class="sxs-lookup"><span data-stu-id="66ff3-128">Type is D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE.</span></span><br/> <span data-ttu-id="66ff3-129">El valor predeterminado es D2D1 \_ 3DPERSPECTIVETRANSFORM \_ modo de interpolación \_ \_ lineal.</span><span class="sxs-lookup"><span data-stu-id="66ff3-129">Default value is D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE\_LINEAR.</span></span><br/>              |
| <span data-ttu-id="66ff3-130">BorderMode</span><span class="sxs-lookup"><span data-stu-id="66ff3-130">BorderMode</span></span><br/> <span data-ttu-id="66ff3-131">D2D1 \_ 3DPERSPECTIVETRANSFORM \_ \_ modo de borde \_ de la Prop</span><span class="sxs-lookup"><span data-stu-id="66ff3-131">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_BORDER\_MODE</span></span><br/>               | <span data-ttu-id="66ff3-132">El modo que se usa para calcular el borde de la imagen, es decir, es flexible o difícil.</span><span class="sxs-lookup"><span data-stu-id="66ff3-132">The mode used to calculate the border of the image, soft or hard.</span></span> <span data-ttu-id="66ff3-133">Vea [modos de borde](https://www.bing.com/search?q=Border+modes) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="66ff3-133">See [Border modes](https://www.bing.com/search?q=Border+modes) for more info.</span></span><br/> <span data-ttu-id="66ff3-134">El tipo es D2D1 \_ Border \_ mode.</span><span class="sxs-lookup"><span data-stu-id="66ff3-134">Type is D2D1\_BORDER\_MODE.</span></span><br/> <span data-ttu-id="66ff3-135">El valor predeterminado es el \_ modo de borde D2D1 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="66ff3-135">Default value is D2D1\_BORDER\_MODE\_SOFT.</span></span><br/>                                                              |
| <span data-ttu-id="66ff3-136">Profundidad</span><span class="sxs-lookup"><span data-stu-id="66ff3-136">Depth</span></span><br/> <span data-ttu-id="66ff3-137">Profundidad de la D2D1 \_ 3DPERSPECTIVETRANSFORM \_ \_</span><span class="sxs-lookup"><span data-stu-id="66ff3-137">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_DEPTH</span></span><br/>                           | <span data-ttu-id="66ff3-138">Distancia entre el *PerspectiveOrigin* y el plano de proyección.</span><span class="sxs-lookup"><span data-stu-id="66ff3-138">The distance from the *PerspectiveOrigin* to the projection plane.</span></span> <span data-ttu-id="66ff3-139">El valor especificado en DIP y debe ser mayor que 0.</span><span class="sxs-lookup"><span data-stu-id="66ff3-139">The value specified in DIPs and must be greater than 0.</span></span><br/> <span data-ttu-id="66ff3-140">El tipo es FLOAT.</span><span class="sxs-lookup"><span data-stu-id="66ff3-140">Type is FLOAT.</span></span><br/> <span data-ttu-id="66ff3-141">El valor predeterminado es 1000.0 f.</span><span class="sxs-lookup"><span data-stu-id="66ff3-141">Default value is 1000.0f.</span></span><br/>                                                                                               |
| <span data-ttu-id="66ff3-142">PerspectiveOrigin</span><span class="sxs-lookup"><span data-stu-id="66ff3-142">PerspectiveOrigin</span></span><br/> <span data-ttu-id="66ff3-143">Origen de la perspectiva de D2D1 \_ 3DPERSPECTIVETRANSFORM \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="66ff3-143">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_PERSPECTIVE\_ORIGIN</span></span><br/> | <span data-ttu-id="66ff3-144">La ubicación X e y del visor en la escena 3D.</span><span class="sxs-lookup"><span data-stu-id="66ff3-144">The X and Y location of the viewer in the 3D scene.</span></span> <span data-ttu-id="66ff3-145">Esta propiedad es un vector D2D1 se \_ \_ define como: (punto X, punto Y).</span><span class="sxs-lookup"><span data-stu-id="66ff3-145">This property is a D2D1\_VECTOR\_2F defined as: (point X, point Y).</span></span> <span data-ttu-id="66ff3-146">Las unidades están en DIP.</span><span class="sxs-lookup"><span data-stu-id="66ff3-146">The units are in DIPs.</span></span><br/> <span data-ttu-id="66ff3-147">Establezca el valor Z con la propiedad *Depth* .</span><span class="sxs-lookup"><span data-stu-id="66ff3-147">You set the Z value with the *Depth* property.</span></span><br/> <span data-ttu-id="66ff3-148">El tipo es \_ Vector D2D1 \_ 2F.</span><span class="sxs-lookup"><span data-stu-id="66ff3-148">Type is D2D1\_VECTOR\_2F.</span></span><br/> <span data-ttu-id="66ff3-149">El valor predeterminado es {0.0 f, 0.0 f}.</span><span class="sxs-lookup"><span data-stu-id="66ff3-149">Default value is {0.0f, 0.0f}.</span></span><br/> |
| <span data-ttu-id="66ff3-150">LocalOffset</span><span class="sxs-lookup"><span data-stu-id="66ff3-150">LocalOffset</span></span><br/> <span data-ttu-id="66ff3-151">D2D1 \_ 3DPERSPECTIVETRANSFORM \_ prop \_ \_ desplazamiento local</span><span class="sxs-lookup"><span data-stu-id="66ff3-151">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_LOCAL\_OFFSET</span></span><br/>             | <span data-ttu-id="66ff3-152">Traducción que realiza el efecto antes de girar el plano de proyección.</span><span class="sxs-lookup"><span data-stu-id="66ff3-152">A translation the effect performs before it rotates the projection plane.</span></span> <span data-ttu-id="66ff3-153">Esta propiedad es una D2D1 \_ Vector \_ 3F definida como: (X, Y, Z).</span><span class="sxs-lookup"><span data-stu-id="66ff3-153">This property is a D2D1\_VECTOR\_3F defined as: (X, Y, Z).</span></span> <span data-ttu-id="66ff3-154">Las unidades están en DIP.</span><span class="sxs-lookup"><span data-stu-id="66ff3-154">The units are in DIPs.</span></span><br/> <span data-ttu-id="66ff3-155">El tipo es D2D1 \_ Vector \_ 3F.</span><span class="sxs-lookup"><span data-stu-id="66ff3-155">Type is D2D1\_VECTOR\_3F.</span></span><br/> <span data-ttu-id="66ff3-156">El valor predeterminado es {0.0 f, 0.0 f, 0.0 f}.</span><span class="sxs-lookup"><span data-stu-id="66ff3-156">Default value is {0.0f, 0.0f, 0.0f}.</span></span><br/>                                        |
| <span data-ttu-id="66ff3-157">GlobalOffset</span><span class="sxs-lookup"><span data-stu-id="66ff3-157">GlobalOffset</span></span><br/> <span data-ttu-id="66ff3-158">\_ \_ \_ Desplazamiento global de prop \_ de D2D1 3DPERSPECTIVETRANSFORM</span><span class="sxs-lookup"><span data-stu-id="66ff3-158">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_GLOBAL\_OFFSET</span></span><br/>           | <span data-ttu-id="66ff3-159">Traducción que realiza el efecto después de girar el plano de proyección.</span><span class="sxs-lookup"><span data-stu-id="66ff3-159">A translation the effect performs after it rotates the projection plane.</span></span> <span data-ttu-id="66ff3-160">Esta propiedad es una D2D1 \_ Vector \_ 3F definida como: (X, Y, Z).</span><span class="sxs-lookup"><span data-stu-id="66ff3-160">This property is a D2D1\_VECTOR\_3F defined as: (X, Y, Z).</span></span> <span data-ttu-id="66ff3-161">Las unidades están en DIP.</span><span class="sxs-lookup"><span data-stu-id="66ff3-161">The units are in DIPs.</span></span><br/> <span data-ttu-id="66ff3-162">El tipo es D2D1 \_ Vector \_ 3F.</span><span class="sxs-lookup"><span data-stu-id="66ff3-162">Type is D2D1\_VECTOR\_3F.</span></span><br/> <span data-ttu-id="66ff3-163">El valor predeterminado es {0.0 f, 0.0 f, 0.0 f}.</span><span class="sxs-lookup"><span data-stu-id="66ff3-163">Default value is {0.0f, 0.0f, 0.0f}.</span></span><br/>                                         |
| <span data-ttu-id="66ff3-164">RotationOrigin</span><span class="sxs-lookup"><span data-stu-id="66ff3-164">RotationOrigin</span></span><br/> <span data-ttu-id="66ff3-165">\_Origen de \_ rotación de propiedades \_ \_ de D2D1 3DPERSPECTIVETRANSFORM</span><span class="sxs-lookup"><span data-stu-id="66ff3-165">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_ROTATION\_ORIGIN</span></span><br/>       | <span data-ttu-id="66ff3-166">Punto central de la rotación que realiza el efecto.</span><span class="sxs-lookup"><span data-stu-id="66ff3-166">The center point of the rotation the effect performs.</span></span> <span data-ttu-id="66ff3-167">Esta propiedad es una D2D1 \_ Vector \_ 3F definida como: (X, Y, Z).</span><span class="sxs-lookup"><span data-stu-id="66ff3-167">This property is a D2D1\_VECTOR\_3F defined as: (X, Y, Z).</span></span> <span data-ttu-id="66ff3-168">Las unidades están en DIP.</span><span class="sxs-lookup"><span data-stu-id="66ff3-168">The units are in DIPs.</span></span><br/> <span data-ttu-id="66ff3-169">El tipo es D2D1 \_ Vector \_ 3F.</span><span class="sxs-lookup"><span data-stu-id="66ff3-169">Type is D2D1\_VECTOR\_3F.</span></span><br/> <span data-ttu-id="66ff3-170">El valor predeterminado es {0.0 f, 0.0 f, 0.0 f}.</span><span class="sxs-lookup"><span data-stu-id="66ff3-170">Default value is {0.0f, 0.0f, 0.0f}.</span></span><br/>                                                            |
| <span data-ttu-id="66ff3-171">Rotación</span><span class="sxs-lookup"><span data-stu-id="66ff3-171">Rotation</span></span><br/> <span data-ttu-id="66ff3-172">D2D1 \_ 3DPERSPECTIVETRANSFORM \_ prop \_ giro</span><span class="sxs-lookup"><span data-stu-id="66ff3-172">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_ROTATION</span></span><br/>                     | <span data-ttu-id="66ff3-173">Ángulos de rotación de cada eje.</span><span class="sxs-lookup"><span data-stu-id="66ff3-173">The angles of rotation for each axis.</span></span> <span data-ttu-id="66ff3-174">Esta propiedad es una D2D1 \_ Vector \_ 3F definida como: (X, Y, Z).</span><span class="sxs-lookup"><span data-stu-id="66ff3-174">This property is a D2D1\_VECTOR\_3F defined as: (X, Y, Z).</span></span> <span data-ttu-id="66ff3-175">Las unidades están en grados.</span><span class="sxs-lookup"><span data-stu-id="66ff3-175">The units are in degrees.</span></span><br/> <span data-ttu-id="66ff3-176">El tipo es D2D1 \_ Vector \_ 3F.</span><span class="sxs-lookup"><span data-stu-id="66ff3-176">Type is D2D1\_VECTOR\_3F.</span></span><br/> <span data-ttu-id="66ff3-177">El valor predeterminado es {0.0 f, 0.0 f, 0.0 f}.</span><span class="sxs-lookup"><span data-stu-id="66ff3-177">Default value is {0.0f, 0.0f, 0.0f}.</span></span><br/>                                                                         |



 

## <a name="interpolation-modes"></a><span data-ttu-id="66ff3-178">Modos de interpolación</span><span class="sxs-lookup"><span data-stu-id="66ff3-178">Interpolation modes</span></span>



| <span data-ttu-id="66ff3-179">Enumeración</span><span class="sxs-lookup"><span data-stu-id="66ff3-179">Enumeration</span></span>                                                              | <span data-ttu-id="66ff3-180">Descripción</span><span class="sxs-lookup"><span data-stu-id="66ff3-180">Description</span></span>                                                                                                                                                |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66ff3-181">D2D1 \_ el \_ modo de interpolación 3DPERSPECTIVETRANSFORM \_ \_ más cercano \_</span><span class="sxs-lookup"><span data-stu-id="66ff3-181">D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE\_NEAREST\_NEIGHBOR</span></span>     | <span data-ttu-id="66ff3-182">Muestrea el punto único más cercano y lo usa.</span><span class="sxs-lookup"><span data-stu-id="66ff3-182">Samples the nearest single point and uses that.</span></span> <span data-ttu-id="66ff3-183">Este modo utiliza menos tiempo de procesamiento, pero genera la imagen de menor calidad.</span><span class="sxs-lookup"><span data-stu-id="66ff3-183">This mode uses less processing time, but outputs the lowest quality image.</span></span>                                 |
| <span data-ttu-id="66ff3-184">D2D1 \_ \_ modo de interpolación 3DPERSPECTIVETRANSFORM \_ \_ lineal</span><span class="sxs-lookup"><span data-stu-id="66ff3-184">D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE\_LINEAR</span></span>                | <span data-ttu-id="66ff3-185">Utiliza un ejemplo de cuatro puntos y una interpolación lineal.</span><span class="sxs-lookup"><span data-stu-id="66ff3-185">Uses a four point sample and linear interpolation.</span></span> <span data-ttu-id="66ff3-186">Este modo usa más tiempo de procesamiento que el modo vecino más cercano, pero genera una imagen de mayor calidad.</span><span class="sxs-lookup"><span data-stu-id="66ff3-186">This mode uses more processing time than the nearest neighbor mode, but outputs a higher quality image.</span></span> |
| <span data-ttu-id="66ff3-187">D2D1 \_ \_ modo de interpolación 3DPERSPECTIVETRANSFORM \_ \_ cúbico</span><span class="sxs-lookup"><span data-stu-id="66ff3-187">D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE\_CUBIC</span></span>                 | <span data-ttu-id="66ff3-188">Usa un kernel cúbico de ejemplo 16 para la interpolación.</span><span class="sxs-lookup"><span data-stu-id="66ff3-188">Uses a 16 sample cubic kernel for interpolation.</span></span> <span data-ttu-id="66ff3-189">Este modo utiliza la mayor parte del tiempo de procesamiento, pero genera una imagen de mayor calidad.</span><span class="sxs-lookup"><span data-stu-id="66ff3-189">This mode uses the most processing time, but outputs a higher quality image.</span></span>                              |
| <span data-ttu-id="66ff3-190">D2D1 \_ 3DPERSPECTIVETRANSFORM \_ modo de interpolación \_ \_ lineal de varios \_ ejemplos \_</span><span class="sxs-lookup"><span data-stu-id="66ff3-190">D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE\_MULTI\_SAMPLE\_LINEAR</span></span> | <span data-ttu-id="66ff3-191">Usa 4 muestras lineales dentro de un solo píxel para el suavizado de contorno adecuado.</span><span class="sxs-lookup"><span data-stu-id="66ff3-191">Uses 4 linear samples within a single pixel for good edge anti-aliasing.</span></span> <span data-ttu-id="66ff3-192">Este modo es adecuado para reducir verticalmente en pequeñas cantidades de imágenes con pocos píxeles.</span><span class="sxs-lookup"><span data-stu-id="66ff3-192">This mode is good for scaling down by small amounts on images with few pixels.</span></span>    |
| <span data-ttu-id="66ff3-193">D2D1 \_ \_ modo de interpolación 3DPERSPECTIVETRANSFORM \_ \_ anisotrópico</span><span class="sxs-lookup"><span data-stu-id="66ff3-193">D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE\_ANISOTROPIC</span></span>           | <span data-ttu-id="66ff3-194">Utiliza el filtrado anisotrópico para muestrear un patrón según la forma transformada del mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="66ff3-194">Uses anisotropic filtering to sample a pattern according to the transformed shape of the bitmap.</span></span>                                                           |



 

> [!Note]  
> <span data-ttu-id="66ff3-195">Si no selecciona un modo, el efecto tiene como valor predeterminado el \_ \_ modo de interpolación D2D1 3DPERSPECTIVETRANSFORM \_ \_ lineal.</span><span class="sxs-lookup"><span data-stu-id="66ff3-195">If you don't select a mode, the effect defaults to D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE\_LINEAR.</span></span>

 

> [!Note]  
> <span data-ttu-id="66ff3-196">El modo anisotrópico genera mapas MIP al escalar; sin embargo, si establece la propiedad **Cached** en true en los efectos que se aplican a este efecto, no se generarán los mapas MIP cada vez para imágenes suficientemente pequeñas.</span><span class="sxs-lookup"><span data-stu-id="66ff3-196">Anisotropic mode generates mipmaps when scaling, however, if you set the **Cached** property to true on the effects that are input to this effect, the mipmaps won't be generated every time for sufficiently small images.</span></span>

 

## <a name="border-modes"></a><span data-ttu-id="66ff3-197">Modos de borde</span><span class="sxs-lookup"><span data-stu-id="66ff3-197">Border modes</span></span>



| <span data-ttu-id="66ff3-198">Nombre</span><span class="sxs-lookup"><span data-stu-id="66ff3-198">Name</span></span>                     | <span data-ttu-id="66ff3-199">Descripción</span><span class="sxs-lookup"><span data-stu-id="66ff3-199">Description</span></span>                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66ff3-200">D2D1 \_ modo de borde \_ \_ flexible</span><span class="sxs-lookup"><span data-stu-id="66ff3-200">D2D1\_BORDER\_MODE\_SOFT</span></span> | <span data-ttu-id="66ff3-201">El efecto rellena la imagen con píxeles negros transparentes mientras se interpola, lo que da lugar a un borde flexible.</span><span class="sxs-lookup"><span data-stu-id="66ff3-201">The effect pads the image with transparent black pixels as it interpolates, resulting in a soft edge.</span></span><br/> |
| <span data-ttu-id="66ff3-202">D2D1 \_ del \_ modo de borde \_</span><span class="sxs-lookup"><span data-stu-id="66ff3-202">D2D1\_BORDER\_MODE\_HARD</span></span> | <span data-ttu-id="66ff3-203">El efecto fija la salida al tamaño de la imagen de entrada.</span><span class="sxs-lookup"><span data-stu-id="66ff3-203">The effect clamps the output to the size of the input image.</span></span> <br/>                                         |



 

## <a name="output-bitmap"></a><span data-ttu-id="66ff3-204">Mapa de bits de salida</span><span class="sxs-lookup"><span data-stu-id="66ff3-204">Output bitmap</span></span>

<span data-ttu-id="66ff3-205">El tamaño del mapa de bits de salida depende de la matriz de transformación que se aplica a la imagen.</span><span class="sxs-lookup"><span data-stu-id="66ff3-205">The size of the output bitmap depends on the transform matrix that is applied to the image.</span></span>

<span data-ttu-id="66ff3-206">El efecto realiza la operación de transformación y, a continuación, aplica un cuadro de límite alrededor del resultado.</span><span class="sxs-lookup"><span data-stu-id="66ff3-206">The effect performs the transform operation and then applies a bounding box around the result.</span></span> <span data-ttu-id="66ff3-207">El mapa de bits de salida es el tamaño del cuadro de límite.</span><span class="sxs-lookup"><span data-stu-id="66ff3-207">The output bitmap is the size of the bounding box.</span></span>

## <a name="requirements"></a><span data-ttu-id="66ff3-208">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66ff3-208">Requirements</span></span>



| <span data-ttu-id="66ff3-209">Requisito</span><span class="sxs-lookup"><span data-stu-id="66ff3-209">Requirement</span></span> | <span data-ttu-id="66ff3-210">Value</span><span class="sxs-lookup"><span data-stu-id="66ff3-210">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="66ff3-211">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66ff3-211">Minimum supported client</span></span> | <span data-ttu-id="66ff3-212">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="66ff3-212">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="66ff3-213">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66ff3-213">Minimum supported server</span></span> | <span data-ttu-id="66ff3-214">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="66ff3-214">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="66ff3-215">Encabezado</span><span class="sxs-lookup"><span data-stu-id="66ff3-215">Header</span></span>                   | <span data-ttu-id="66ff3-216">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="66ff3-216">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="66ff3-217">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="66ff3-217">Library</span></span>                  | <span data-ttu-id="66ff3-218">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="66ff3-218">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="66ff3-219">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="66ff3-219">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66ff3-220">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="66ff3-220">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

