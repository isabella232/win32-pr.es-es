---
description: Después de ajustar la intensidad de la luz para cualquier efecto de atenuación, el motor de iluminación calcula la parte de la luz restante que se refleja de un vértice, dado el ángulo del vértice normal y la dirección de la luz del incidente.
ms.assetid: 29280a02-1c26-4b54-8468-707dd96dea1d
title: Luz difusa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51e45093786348aaa115ec38c420acec471f718
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104151954"
---
# <a name="diffuse-lighting-direct3d-9"></a><span data-ttu-id="577a0-103">Luz difusa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="577a0-103">Diffuse Lighting (Direct3D 9)</span></span>

<span data-ttu-id="577a0-104">Después de ajustar la intensidad de la luz para cualquier efecto de atenuación, el motor de iluminación calcula la parte de la luz restante que se refleja de un vértice, dado el ángulo del vértice normal y la dirección de la luz del incidente.</span><span class="sxs-lookup"><span data-stu-id="577a0-104">After adjusting the light intensity for any attenuation effects, the lighting engine computes how much of the remaining light reflects from a vertex, given the angle of the vertex normal and the direction of the incident light.</span></span> <span data-ttu-id="577a0-105">El motor de iluminación salta a este paso para las luces direccionales porque no se atenúan a lo largo de la distancia.</span><span class="sxs-lookup"><span data-stu-id="577a0-105">The lighting engine skips to this step for directional lights because they do not attenuate over distance.</span></span> <span data-ttu-id="577a0-106">El sistema considera dos tipos de reflexión, difuso y especular, y utiliza una fórmula diferente para determinar cuánta luz se refleja para cada una.</span><span class="sxs-lookup"><span data-stu-id="577a0-106">The system considers two reflection types, diffuse and specular, and uses a different formula to determine how much light is reflected for each.</span></span> <span data-ttu-id="577a0-107">Después de calcular los importes de la luz reflejada, Direct3D aplica estos nuevos valores a las propiedades de reflexión difusa y especular del material actual.</span><span class="sxs-lookup"><span data-stu-id="577a0-107">After calculating the amounts of light reflected, Direct3D applies these new values to the diffuse and specular reflectance properties of the current material.</span></span> <span data-ttu-id="577a0-108">Los valores de color resultantes son los componentes difusos y especulares que el rasterizador utiliza para generar el sombreado Gouraud y el resaltado especular.</span><span class="sxs-lookup"><span data-stu-id="577a0-108">The resulting color values are the diffuse and specular components that the rasterizer uses to produce Gouraud shading and specular highlighting.</span></span>

<span data-ttu-id="577a0-109">La iluminación difusa se describe en la siguiente ecuación.</span><span class="sxs-lookup"><span data-stu-id="577a0-109">Diffuse lighting is described by the following equation.</span></span>

<span data-ttu-id="577a0-110">Luz difusa = suma \[ C<sub>d</sub> \* L<sub>d</sub> \* (N<sup>.</sup> L<sub>dir</sub>) \* ATTEN \*\]</span><span class="sxs-lookup"><span data-stu-id="577a0-110">Diffuse Lighting = sum\[C<sub>d</sub>\*L<sub>d</sub>\*(N<sup>.</sup>L<sub>dir</sub>)\*Atten\*Spot\]</span></span>



| <span data-ttu-id="577a0-111">Parámetro</span><span class="sxs-lookup"><span data-stu-id="577a0-111">Parameter</span></span>       | <span data-ttu-id="577a0-112">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="577a0-112">Default value</span></span> | <span data-ttu-id="577a0-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="577a0-113">Type</span></span>          | <span data-ttu-id="577a0-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="577a0-114">Description</span></span>                                                                                                   |
|-----------------|---------------|---------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="577a0-115">Sum</span><span class="sxs-lookup"><span data-stu-id="577a0-115">sum</span></span>             | <span data-ttu-id="577a0-116">N/D</span><span class="sxs-lookup"><span data-stu-id="577a0-116">N/A</span></span>           | <span data-ttu-id="577a0-117">N/D</span><span class="sxs-lookup"><span data-stu-id="577a0-117">N/A</span></span>           | <span data-ttu-id="577a0-118">Suma de cada componente difuso de la luz.</span><span class="sxs-lookup"><span data-stu-id="577a0-118">Summation of each light's diffuse component.</span></span>                                                                  |
| <span data-ttu-id="577a0-119">C<sub>d</sub></span><span class="sxs-lookup"><span data-stu-id="577a0-119">C<sub>d</sub></span></span>   | <span data-ttu-id="577a0-120">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="577a0-120">(0,0,0,0)</span></span>     | <span data-ttu-id="577a0-121">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="577a0-121">D3DCOLORVALUE</span></span> | <span data-ttu-id="577a0-122">Color difuso.</span><span class="sxs-lookup"><span data-stu-id="577a0-122">Diffuse color.</span></span>                                                                                                |
| <span data-ttu-id="577a0-123">L<sub>d</sub></span><span class="sxs-lookup"><span data-stu-id="577a0-123">L<sub>d</sub></span></span>   | <span data-ttu-id="577a0-124">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="577a0-124">(0,0,0,0)</span></span>     | <span data-ttu-id="577a0-125">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="577a0-125">D3DCOLORVALUE</span></span> | <span data-ttu-id="577a0-126">Color difuso de luz.</span><span class="sxs-lookup"><span data-stu-id="577a0-126">Light diffuse color.</span></span>                                                                                          |
| <span data-ttu-id="577a0-127">N</span><span class="sxs-lookup"><span data-stu-id="577a0-127">N</span></span>               | <span data-ttu-id="577a0-128">N/D</span><span class="sxs-lookup"><span data-stu-id="577a0-128">N/A</span></span>           | <span data-ttu-id="577a0-129">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="577a0-129">D3DVECTOR</span></span>     | <span data-ttu-id="577a0-130">Vértice normal</span><span class="sxs-lookup"><span data-stu-id="577a0-130">Vertex normal</span></span>                                                                                                 |
| <span data-ttu-id="577a0-131"><sub>Directorio</sub> L</span><span class="sxs-lookup"><span data-stu-id="577a0-131">L<sub>dir</sub></span></span> | <span data-ttu-id="577a0-132">N/D</span><span class="sxs-lookup"><span data-stu-id="577a0-132">N/A</span></span>           | <span data-ttu-id="577a0-133">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="577a0-133">D3DVECTOR</span></span>     | <span data-ttu-id="577a0-134">Vector de dirección desde el vértice del objeto hasta la luz.</span><span class="sxs-lookup"><span data-stu-id="577a0-134">Direction vector from object vertex to the light.</span></span>                                                             |
| <span data-ttu-id="577a0-135">Atten</span><span class="sxs-lookup"><span data-stu-id="577a0-135">Atten</span></span>           | <span data-ttu-id="577a0-136">N/D</span><span class="sxs-lookup"><span data-stu-id="577a0-136">N/A</span></span>           | <span data-ttu-id="577a0-137">FLOAT</span><span class="sxs-lookup"><span data-stu-id="577a0-137">FLOAT</span></span>         | <span data-ttu-id="577a0-138">Atenuación ligera.</span><span class="sxs-lookup"><span data-stu-id="577a0-138">Light attenuation.</span></span> <span data-ttu-id="577a0-139">Vea [atenuación y factor de Spotlight (Direct3D 9)](attenuation-and-spotlight-factor.md).</span><span class="sxs-lookup"><span data-stu-id="577a0-139">See [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span> |
| <span data-ttu-id="577a0-140">Zona</span><span class="sxs-lookup"><span data-stu-id="577a0-140">Spot</span></span>            | <span data-ttu-id="577a0-141">N/D</span><span class="sxs-lookup"><span data-stu-id="577a0-141">N/A</span></span>           | <span data-ttu-id="577a0-142">FLOAT</span><span class="sxs-lookup"><span data-stu-id="577a0-142">FLOAT</span></span>         | <span data-ttu-id="577a0-143">Factor destacado.</span><span class="sxs-lookup"><span data-stu-id="577a0-143">Spotlight factor.</span></span> <span data-ttu-id="577a0-144">Vea [atenuación y factor de Spotlight (Direct3D 9)](attenuation-and-spotlight-factor.md).</span><span class="sxs-lookup"><span data-stu-id="577a0-144">See [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span>  |



 

<span data-ttu-id="577a0-145">El valor de C<sub>d</sub> es:</span><span class="sxs-lookup"><span data-stu-id="577a0-145">The value for C<sub>d</sub> is either:</span></span>

-   <span data-ttu-id="577a0-146">Vertex color1, si DIFFUSEMATERIALSOURCE = D3DMCS \_ color1, y el primer color de vértice se proporciona en la declaración de vértices.</span><span class="sxs-lookup"><span data-stu-id="577a0-146">vertex color1, if DIFFUSEMATERIALSOURCE = D3DMCS\_COLOR1, and the first vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="577a0-147">Vertex color2, si DIFFUSEMATERIALSOURCE = D3DMCS \_ color2, y el segundo color de vértice se proporciona en la declaración de vértices.</span><span class="sxs-lookup"><span data-stu-id="577a0-147">vertex color2, if DIFFUSEMATERIALSOURCE = D3DMCS\_COLOR2, and the second vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="577a0-148">color difuso de material</span><span class="sxs-lookup"><span data-stu-id="577a0-148">material diffuse color</span></span>

> [!Note]  
> <span data-ttu-id="577a0-149">Si se usa la opción DIFFUSEMATERIALSOURCE y no se proporciona el color del vértice, se usa el color difuso de material.</span><span class="sxs-lookup"><span data-stu-id="577a0-149">If either DIFFUSEMATERIALSOURCE option is used, and the vertex color is not provided, the material diffuse color is used.</span></span>

 

<span data-ttu-id="577a0-150">Para calcular la atenuación (ATTEN) o las características destacadas (spot), vea [atenuación y factor de Spotlight (Direct3D 9)](attenuation-and-spotlight-factor.md).</span><span class="sxs-lookup"><span data-stu-id="577a0-150">To calculate the attenuation (Atten) or the spotlight characteristics (Spot), see [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span>

<span data-ttu-id="577a0-151">Los componentes difusos se fijan de 0 a 255, una vez que todas las luces se procesan y se interpolan por separado.</span><span class="sxs-lookup"><span data-stu-id="577a0-151">Diffuse components are clamped to be from 0 to 255, after all lights are processed and interpolated separately.</span></span> <span data-ttu-id="577a0-152">El valor de iluminación difusa resultante es una combinación de los valores de las luces ambiente, difusa y emisor.</span><span class="sxs-lookup"><span data-stu-id="577a0-152">The resulting diffuse lighting value is a combination of the ambient, diffuse and emissive light values.</span></span>

## <a name="example"></a><span data-ttu-id="577a0-153">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="577a0-153">Example</span></span>

<span data-ttu-id="577a0-154">En este ejemplo, el objeto se colorea utilizando el color difuso de luz y un color difuso de material.</span><span class="sxs-lookup"><span data-stu-id="577a0-154">In this example, the object is colored using the light diffuse color and a material diffuse color.</span></span> <span data-ttu-id="577a0-155">A continuación se muestra el código.</span><span class="sxs-lookup"><span data-stu-id="577a0-155">The code is shown below.</span></span>


```
D3DMATERIAL9 mtrl;
ZeroMemory( &mtrl, sizeof(mtrl) );

D3DLIGHT9 light;
ZeroMemory( &light, sizeof(light) );
light.Type = D3DLIGHT_DIRECTIONAL;

D3DXVECTOR3 vecDir;
vecDir = D3DXVECTOR3(0.5f, 0.0f, -0.5f);
D3DXVec3Normalize( (D3DXVECTOR3*)&light.Direction, &vecDir );

// set directional light diffuse color
light.Diffuse.r = 1.0f;
light.Diffuse.g = 1.0f;
light.Diffuse.b = 1.0f;
light.Diffuse.a = 1.0f;
m_pd3dDevice->SetLight( 0, &light );
m_pd3dDevice->LightEnable( 0, TRUE );

// if a material is used, SetRenderState must be used
// vertex color = light diffuse color * material diffuse color
mtrl.Diffuse.r = 0.75f;
mtrl.Diffuse.g = 0.0f;
mtrl.Diffuse.b = 0.0f;
mtrl.Diffuse.a = 0.0f;
m_pd3dDevice->SetMaterial( &mtrl );
m_pd3dDevice->SetRenderState(D3DRS_DIFFUSEMATERIALSOURCE, D3DMCS_MATERIAL);
```



<span data-ttu-id="577a0-156">Según la ecuación, el color resultante para los vértices del objeto es una combinación del color del material y el color claro.</span><span class="sxs-lookup"><span data-stu-id="577a0-156">According to the equation, the resulting color for the object vertices is a combination of the material color and the light color.</span></span>

<span data-ttu-id="577a0-157">En las dos ilustraciones siguientes se muestra el color del material, que está atenuado y el color claro, que es rojo brillante.</span><span class="sxs-lookup"><span data-stu-id="577a0-157">The following two illustrations show the material color, which is gray, and the light color, which is bright red.</span></span>

![Ilustración de una esfera gris](images/amb1.jpg)![Ilustración de una esfera roja](images/lightred.jpg)

<span data-ttu-id="577a0-160">La escena resultante se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="577a0-160">The resulting scene is shown in the following illustration.</span></span> <span data-ttu-id="577a0-161">El único objeto de la escena es una esfera.</span><span class="sxs-lookup"><span data-stu-id="577a0-161">The only object in the scene is a sphere.</span></span> <span data-ttu-id="577a0-162">El cálculo de iluminación difusa toma el color y la luz difusa y lo modifica por el ángulo entre la dirección de la luz y el vértice normal mediante el producto de punto.</span><span class="sxs-lookup"><span data-stu-id="577a0-162">The diffuse lighting calculation takes the material and light diffuse color and modifies it by the angle between the light direction and the vertex normal using the dot product.</span></span> <span data-ttu-id="577a0-163">Como resultado, el parte posterior de la esfera se oscurece a medida que la superficie de la esfera se curva fuera de la luz.</span><span class="sxs-lookup"><span data-stu-id="577a0-163">As a result, the backside of the sphere gets darker as the surface of the sphere curves away from the light.</span></span>

![Ilustración de una esfera con iluminación difusa](images/lightd.jpg)

<span data-ttu-id="577a0-165">La combinación de la iluminación difusa con la iluminación ambiente del ejemplo anterior sombrea toda la superficie del objeto.</span><span class="sxs-lookup"><span data-stu-id="577a0-165">Combining the diffuse lighting with the ambient lighting from the previous example shades the entire surface of the object.</span></span> <span data-ttu-id="577a0-166">La luz ambiente sombrea toda la superficie y la luz difusa ayuda a revelar la forma 3D del objeto, tal y como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="577a0-166">The ambient light shades the entire surface and the diffuse light helps reveal the object's 3D shape, as shown in the following illustration.</span></span>

![Ilustración de una esfera con iluminación ambiente y luz difusa](images/lightad.jpg)

<span data-ttu-id="577a0-168">La iluminación difusa es más intensiva para calcular que la iluminación ambiente.</span><span class="sxs-lookup"><span data-stu-id="577a0-168">Diffuse lighting is more intensive to calculate than ambient lighting.</span></span> <span data-ttu-id="577a0-169">Dado que depende de las normales de vértices y de la dirección luminosa, puede ver la geometría de los objetos en el espacio 3D, lo que produce una iluminación más realista que la iluminación ambiente.</span><span class="sxs-lookup"><span data-stu-id="577a0-169">Because it depends on the vertex normals and light direction, you can see the objects geometry in 3D space, which produces a more realistic lighting than ambient lighting.</span></span> <span data-ttu-id="577a0-170">Puede usar los reflejos especulares para lograr un aspecto más realista.</span><span class="sxs-lookup"><span data-stu-id="577a0-170">You can use specular highlights to achieve a more realistic look.</span></span>

## <a name="related-topics"></a><span data-ttu-id="577a0-171">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="577a0-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="577a0-172">Matemáticas de iluminación</span><span class="sxs-lookup"><span data-stu-id="577a0-172">Mathematics of Lighting</span></span>](mathematics-of-lighting.md)
</dt> </dl>

 

 



