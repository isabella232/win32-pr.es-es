---
description: La reflexión especular de modelado requiere que el sistema no solo sepa en qué dirección viaja la luz, sino también la dirección hacia el ojo del espectador.
ms.assetid: 35da0ac3-4e68-4d37-a987-405fc15d0cbf
title: Iluminación especular (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b16d71bd8d814e104cf8a90d1d1fe9b15ba10f3
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343680"
---
# <a name="specular-lighting-direct3d-9"></a><span data-ttu-id="2ad75-103">Iluminación especular (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2ad75-103">Specular Lighting (Direct3D 9)</span></span>

<span data-ttu-id="2ad75-104">La reflexión especular de modelado requiere que el sistema no solo sepa en qué dirección viaja la luz, sino también la dirección hacia el ojo del espectador.</span><span class="sxs-lookup"><span data-stu-id="2ad75-104">Modeling specular reflection requires that the system not only know in what direction light is traveling, but also the direction to the viewer's eye.</span></span> <span data-ttu-id="2ad75-105">El sistema usa una versión simplificada del modelo de reflexión especular de Phong, que emplea un vector a medio camino para aproximar la intensidad de la reflexión especular.</span><span class="sxs-lookup"><span data-stu-id="2ad75-105">The system uses a simplified version of the Phong specular-reflection model, which employs a halfway vector to approximate the intensity of specular reflection.</span></span>

<span data-ttu-id="2ad75-106">El estado de iluminación predeterminado no calcula los resaltados especulares.</span><span class="sxs-lookup"><span data-stu-id="2ad75-106">The default lighting state does not calculate specular highlights.</span></span> <span data-ttu-id="2ad75-107">Para habilitar la iluminación especular, asegúrese de establecer D3DRS \_ SPECULARENABLE en **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="2ad75-107">To enable specular lighting, be sure to set D3DRS\_SPECULARENABLE to **TRUE**.</span></span>

## <a name="specular-lighting-equation"></a><span data-ttu-id="2ad75-108">Ecuación de iluminación especular</span><span class="sxs-lookup"><span data-stu-id="2ad75-108">Specular Lighting Equation</span></span>

<span data-ttu-id="2ad75-109">La iluminación especular se describe mediante la ecuación siguiente:</span><span class="sxs-lookup"><span data-stu-id="2ad75-109">Specular Lighting is described by the following equation:</span></span>

<span data-ttu-id="2ad75-110">**Iluminación especular = Cs \* sum \[ Ls \* (N · H)<sup>P</sup> \* Atten \* Spot\]**</span><span class="sxs-lookup"><span data-stu-id="2ad75-110">**Specular Lighting = Cₛ \* sum\[Lₛ \* (N · H)<sup>P</sup> \* Atten \* Spot\]**</span></span>



 

<span data-ttu-id="2ad75-111">En la tabla siguiente se identifican las variables, sus tipos y sus intervalos.</span><span class="sxs-lookup"><span data-stu-id="2ad75-111">The following table identifies the variables, their types, and their ranges.</span></span>



| <span data-ttu-id="2ad75-112">Parámetro</span><span class="sxs-lookup"><span data-stu-id="2ad75-112">Parameter</span></span>    | <span data-ttu-id="2ad75-113">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="2ad75-113">Default value</span></span> | <span data-ttu-id="2ad75-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="2ad75-114">Type</span></span>          | <span data-ttu-id="2ad75-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="2ad75-115">Description</span></span>                                                                                                         |
|--------------|---------------|---------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ad75-116">Cs</span><span class="sxs-lookup"><span data-stu-id="2ad75-116">Cₛ</span></span>           | <span data-ttu-id="2ad75-117">(0,0,0,0)</span><span class="sxs-lookup"><span data-stu-id="2ad75-117">(0,0,0,0)</span></span>     | <span data-ttu-id="2ad75-118">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="2ad75-118">D3DCOLORVALUE</span></span> | <span data-ttu-id="2ad75-119">Color especular.</span><span class="sxs-lookup"><span data-stu-id="2ad75-119">Specular color.</span></span>                                                                                                     |
| <span data-ttu-id="2ad75-120">Sum</span><span class="sxs-lookup"><span data-stu-id="2ad75-120">sum</span></span>          | <span data-ttu-id="2ad75-121">N/D</span><span class="sxs-lookup"><span data-stu-id="2ad75-121">N/A</span></span>           | <span data-ttu-id="2ad75-122">N/D</span><span class="sxs-lookup"><span data-stu-id="2ad75-122">N/A</span></span>           | <span data-ttu-id="2ad75-123">Suma del componente especular de cada luz.</span><span class="sxs-lookup"><span data-stu-id="2ad75-123">Summation of each light's specular component.</span></span>                                                                       |
| <span data-ttu-id="2ad75-124">No</span><span class="sxs-lookup"><span data-stu-id="2ad75-124">N</span></span>            | <span data-ttu-id="2ad75-125">N/D</span><span class="sxs-lookup"><span data-stu-id="2ad75-125">N/A</span></span>           | <span data-ttu-id="2ad75-126">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="2ad75-126">D3DVECTOR</span></span>     | <span data-ttu-id="2ad75-127">Vértice normal.</span><span class="sxs-lookup"><span data-stu-id="2ad75-127">Vertex normal.</span></span>                                                                                                      |
| <span data-ttu-id="2ad75-128">H</span><span class="sxs-lookup"><span data-stu-id="2ad75-128">H</span></span>            | <span data-ttu-id="2ad75-129">N/D</span><span class="sxs-lookup"><span data-stu-id="2ad75-129">N/A</span></span>           | <span data-ttu-id="2ad75-130">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="2ad75-130">D3DVECTOR</span></span>     | <span data-ttu-id="2ad75-131">Vector a medio camino.</span><span class="sxs-lookup"><span data-stu-id="2ad75-131">Half way vector.</span></span> <span data-ttu-id="2ad75-132">Consulte la sección sobre el vector a medio camino.</span><span class="sxs-lookup"><span data-stu-id="2ad75-132">See the section on the halfway vector.</span></span>                                                             |
| <span data-ttu-id="2ad75-133"><sup>P</sup></span><span class="sxs-lookup"><span data-stu-id="2ad75-133"><sup>P</sup></span></span> | <span data-ttu-id="2ad75-134">0,0</span><span class="sxs-lookup"><span data-stu-id="2ad75-134">0.0</span></span>           | <span data-ttu-id="2ad75-135">FLOAT</span><span class="sxs-lookup"><span data-stu-id="2ad75-135">FLOAT</span></span>         | <span data-ttu-id="2ad75-136">Potencia de reflexión especular.</span><span class="sxs-lookup"><span data-stu-id="2ad75-136">Specular reflection power.</span></span> <span data-ttu-id="2ad75-137">El intervalo es de 0 a +infinito</span><span class="sxs-lookup"><span data-stu-id="2ad75-137">Range is 0 to +infinity</span></span>                                                                  |
| <span data-ttu-id="2ad75-138">Ls</span><span class="sxs-lookup"><span data-stu-id="2ad75-138">Lₛ</span></span>           | <span data-ttu-id="2ad75-139">(0,0,0,0)</span><span class="sxs-lookup"><span data-stu-id="2ad75-139">(0,0,0,0)</span></span>     | <span data-ttu-id="2ad75-140">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="2ad75-140">D3DCOLORVALUE</span></span> | <span data-ttu-id="2ad75-141">Color especular claro.</span><span class="sxs-lookup"><span data-stu-id="2ad75-141">Light specular color.</span></span>                                                                                               |
| <span data-ttu-id="2ad75-142">Atten</span><span class="sxs-lookup"><span data-stu-id="2ad75-142">Atten</span></span>        | <span data-ttu-id="2ad75-143">N/D</span><span class="sxs-lookup"><span data-stu-id="2ad75-143">N/A</span></span>           | <span data-ttu-id="2ad75-144">FLOAT</span><span class="sxs-lookup"><span data-stu-id="2ad75-144">FLOAT</span></span>         | <span data-ttu-id="2ad75-145">Valor de atenuación de luz.</span><span class="sxs-lookup"><span data-stu-id="2ad75-145">Light attenuation value.</span></span> <span data-ttu-id="2ad75-146">Consulte [Atenuación y factor spotlight (Direct3D 9).](attenuation-and-spotlight-factor.md)</span><span class="sxs-lookup"><span data-stu-id="2ad75-146">See [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span> |
| <span data-ttu-id="2ad75-147">Zona</span><span class="sxs-lookup"><span data-stu-id="2ad75-147">Spot</span></span>         | <span data-ttu-id="2ad75-148">N/D</span><span class="sxs-lookup"><span data-stu-id="2ad75-148">N/A</span></span>           | <span data-ttu-id="2ad75-149">FLOAT</span><span class="sxs-lookup"><span data-stu-id="2ad75-149">FLOAT</span></span>         | <span data-ttu-id="2ad75-150">Factor spotlight.</span><span class="sxs-lookup"><span data-stu-id="2ad75-150">Spotlight factor.</span></span> <span data-ttu-id="2ad75-151">Consulte [Atenuación y factor spotlight (Direct3D 9).](attenuation-and-spotlight-factor.md)</span><span class="sxs-lookup"><span data-stu-id="2ad75-151">See [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span>        |



 

<span data-ttu-id="2ad75-152">El valor de Cs es:</span><span class="sxs-lookup"><span data-stu-id="2ad75-152">The value for Cₛ is either:</span></span>


```
if(SPECULARMATERIALSOURCE == D3DMCS_COLOR1)
  C = color1;
```



-   <span data-ttu-id="2ad75-153">vertex color1, si el origen del material especular es D3DMCS COLOR1 y el primer color de vértice se proporciona \_ en la declaración de vértice.</span><span class="sxs-lookup"><span data-stu-id="2ad75-153">vertex color1, if the specular material source is D3DMCS\_COLOR1, and the first vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="2ad75-154">vertex color2, si el origen del material especular es D3DMCS COLOR2 y el segundo color del vértice se proporciona \_ en la declaración de vértice.</span><span class="sxs-lookup"><span data-stu-id="2ad75-154">vertex color2, if specular material source is D3DMCS\_COLOR2, and the second vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="2ad75-155">color especular de material</span><span class="sxs-lookup"><span data-stu-id="2ad75-155">material specular color</span></span>

> [!Note]  
> <span data-ttu-id="2ad75-156">Si se usa cualquiera de las opciones de origen de material especular y no se proporciona el color del vértice, se usa el color especular del material.</span><span class="sxs-lookup"><span data-stu-id="2ad75-156">If either specular material source option is used and the vertex color is not provided, then the material specular color is used.</span></span>

 

<span data-ttu-id="2ad75-157">Los componentes especulares se fijan para que sean de 0 a 255, una vez que todas las luces se procesan e interpolan por separado.</span><span class="sxs-lookup"><span data-stu-id="2ad75-157">Specular components are clamped to be from 0 to 255, after all lights are processed and interpolated separately.</span></span>

## <a name="the-halfway-vector"></a><span data-ttu-id="2ad75-158">Vector a medio camino</span><span class="sxs-lookup"><span data-stu-id="2ad75-158">The Halfway Vector</span></span>

<span data-ttu-id="2ad75-159">El vector medio (H) existe a medio camino entre dos vectores: el vector de un vértice de objeto a la fuente de luz y el vector de un vértice de objeto a la posición de la cámara.</span><span class="sxs-lookup"><span data-stu-id="2ad75-159">The halfway vector (H) exists midway between two vectors: the vector from an object vertex to the light source, and the vector from an object vertex to the camera position.</span></span> <span data-ttu-id="2ad75-160">Direct3D proporciona dos maneras de calcular el vector medio.</span><span class="sxs-lookup"><span data-stu-id="2ad75-160">Direct3D provides two ways to compute the halfway vector.</span></span> <span data-ttu-id="2ad75-161">Cuando LOCALVIEWER de D3DRS se establece en TRUE, el sistema calcula el vector a medio camino usando la posición de la cámara y la posición del vértice, junto con el vector de dirección de \_ la luz. </span><span class="sxs-lookup"><span data-stu-id="2ad75-161">When D3DRS\_LOCALVIEWER is set to **TRUE**, the system calculates the halfway vector using the position of the camera and the position of the vertex, along with the light's direction vector.</span></span> <span data-ttu-id="2ad75-162">En la fórmula siguiente se muestra esto.</span><span class="sxs-lookup"><span data-stu-id="2ad75-162">The following formula illustrates this.</span></span>

<span data-ttu-id="2ad75-163">**H = norm(norm(Cp - Vp) + L <sub>dir</sub>)**</span><span class="sxs-lookup"><span data-stu-id="2ad75-163">**H = norm(norm(Cₚ - Vₚ) + L<sub>dir</sub>)**</span></span>



 



| <span data-ttu-id="2ad75-164">Parámetro</span><span class="sxs-lookup"><span data-stu-id="2ad75-164">Parameter</span></span>       | <span data-ttu-id="2ad75-165">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="2ad75-165">Default value</span></span> | <span data-ttu-id="2ad75-166">Tipo</span><span class="sxs-lookup"><span data-stu-id="2ad75-166">Type</span></span>      | <span data-ttu-id="2ad75-167">Descripción</span><span class="sxs-lookup"><span data-stu-id="2ad75-167">Description</span></span>                                                  |
|-----------------|---------------|-----------|--------------------------------------------------------------|
| <span data-ttu-id="2ad75-168">Cp</span><span class="sxs-lookup"><span data-stu-id="2ad75-168">Cₚ</span></span>              | <span data-ttu-id="2ad75-169">N/D</span><span class="sxs-lookup"><span data-stu-id="2ad75-169">N/A</span></span>           | <span data-ttu-id="2ad75-170">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="2ad75-170">D3DVECTOR</span></span> | <span data-ttu-id="2ad75-171">Posición de la cámara.</span><span class="sxs-lookup"><span data-stu-id="2ad75-171">Camera position.</span></span>                                             |
| <span data-ttu-id="2ad75-172">Vp</span><span class="sxs-lookup"><span data-stu-id="2ad75-172">Vₚ</span></span>              | <span data-ttu-id="2ad75-173">N/D</span><span class="sxs-lookup"><span data-stu-id="2ad75-173">N/A</span></span>           | <span data-ttu-id="2ad75-174">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="2ad75-174">D3DVECTOR</span></span> | <span data-ttu-id="2ad75-175">Posición del vértice.</span><span class="sxs-lookup"><span data-stu-id="2ad75-175">Vertex position.</span></span>                                             |
| <span data-ttu-id="2ad75-176">L<sub>dir</sub></span><span class="sxs-lookup"><span data-stu-id="2ad75-176">L<sub>dir</sub></span></span> | <span data-ttu-id="2ad75-177">N/D</span><span class="sxs-lookup"><span data-stu-id="2ad75-177">N/A</span></span>           | <span data-ttu-id="2ad75-178">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="2ad75-178">D3DVECTOR</span></span> | <span data-ttu-id="2ad75-179">Vector de dirección desde la posición del vértice a la posición de la luz.</span><span class="sxs-lookup"><span data-stu-id="2ad75-179">Direction vector from vertex position to the light position.</span></span> |



 

<span data-ttu-id="2ad75-180">Determinar el vector medio de esta manera puede ser un proceso intensivo.</span><span class="sxs-lookup"><span data-stu-id="2ad75-180">Determining the halfway vector in this manner can be computationally intensive.</span></span> <span data-ttu-id="2ad75-181">Como alternativa, al establecer D3DRS LOCALVIEWER = FALSE se indica al sistema que actúe como si el punto de vista se encontrara infinitamente alejado en \_ el eje Z. </span><span class="sxs-lookup"><span data-stu-id="2ad75-181">As an alternative, setting D3DRS\_LOCALVIEWER = **FALSE** instructs the system to act as though the viewpoint is infinitely distant on the z-axis.</span></span> <span data-ttu-id="2ad75-182">Esto se refleja en la fórmula siguiente.</span><span class="sxs-lookup"><span data-stu-id="2ad75-182">This is reflected in the following formula.</span></span>

<span data-ttu-id="2ad75-183">**H = norm((0,0,1) + L <sub>dir</sub>)**</span><span class="sxs-lookup"><span data-stu-id="2ad75-183">**H = norm((0,0,1) + L<sub>dir</sub>)**</span></span>



 

<span data-ttu-id="2ad75-184">Esta configuración consume menos cálculos, pero es mucho menos precisa, por lo que es más usada por las aplicaciones que usan proyección ortogonal.</span><span class="sxs-lookup"><span data-stu-id="2ad75-184">This setting is less computationally intensive, but much less accurate, so it is best used by applications that use orthogonal projection.</span></span>

## <a name="example"></a><span data-ttu-id="2ad75-185">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2ad75-185">Example</span></span>

<span data-ttu-id="2ad75-186">En este ejemplo, el objeto se colore con el color claro especular de la escena y un color especular de material.</span><span class="sxs-lookup"><span data-stu-id="2ad75-186">In this example, the object is colored using the scene specular light color and a material specular color.</span></span> <span data-ttu-id="2ad75-187">El código se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="2ad75-187">The code is shown below.</span></span>


```
D3DMATERIAL9 mtrl;
ZeroMemory( &mtrl, sizeof(mtrl) );

D3DLIGHT9 light;
ZeroMemory( &light, sizeof(light) );
light.Type = D3DLIGHT_DIRECTIONAL;

D3DXVECTOR3 vecDir;
vecDir = D3DXVECTOR3(0.5f, 0.0f, -0.5f);
D3DXVec3Normalize( (D3DXVECTOR3*)&light.Direction, &vecDir );

light.Specular.r = 1.0f;
light.Specular.g = 1.0f;
light.Specular.b = 1.0f;
light.Specular.a = 1.0f;

light.Range = 1000;
light.Falloff = 0;
light.Attenuation0 = 1;
light.Attenuation1 = 0;
light.Attenuation2 = 0;
m_pd3dDevice->SetLight( 0, &light );
m_pd3dDevice->LightEnable( 0, TRUE );
m_pd3dDevice->SetRenderState( D3DRS_SPECULARENABLE, TRUE );

mtrl.Specular.r = 0.5f;
mtrl.Specular.g = 0.5f;
mtrl.Specular.b = 0.5f;
mtrl.Specular.a = 0.5f;
mtrl.Power = 20;
m_pd3dDevice->SetMaterial( &mtrl );
m_pd3dDevice->SetRenderState(D3DRS_SPECULARMATERIALSOURCE, D3DMCS_MATERIAL);
```



<span data-ttu-id="2ad75-188">Según la ecuación, el color resultante para los vértices del objeto es una combinación del color del material y el color claro.</span><span class="sxs-lookup"><span data-stu-id="2ad75-188">According to the equation, the resulting color for the object vertices is a combination of the material color and the light color.</span></span>

<span data-ttu-id="2ad75-189">En la siguiente ilustración se muestra el color del material especular, que es gris, y el color claro especular, que es blanco.</span><span class="sxs-lookup"><span data-stu-id="2ad75-189">The following two illustration show the specular material color, which is gray, and the specular light color, which is white.</span></span>

![ilustración de una esfera gris](images/amb1.jpg)![ilustración de una esfera blanca](images/lightwhite.jpg)

<span data-ttu-id="2ad75-192">El resaltado especular resultante se muestra en la ilustración siguiente.</span><span class="sxs-lookup"><span data-stu-id="2ad75-192">The resulting specular highlight is shown in the following illustration.</span></span>

![ilustración del resaltado especular](images/lights.jpg)

<span data-ttu-id="2ad75-194">La combinación del resaltado especular con la iluminación ambiente y difusa genera la ilustración siguiente.</span><span class="sxs-lookup"><span data-stu-id="2ad75-194">Combining the specular highlight with the ambient and diffuse lighting produces the following illustration.</span></span> <span data-ttu-id="2ad75-195">Con los tres tipos de iluminación aplicados, esto se parece más claramente a un objeto realista.</span><span class="sxs-lookup"><span data-stu-id="2ad75-195">With all three types of lighting applied, this more clearly resembles a realistic object.</span></span>

![ilustración de la combinación del resaltado especular, la iluminación ambiente y la iluminación difusa](images/lightads.jpg)

<span data-ttu-id="2ad75-197">La iluminación especular es más intensiva para calcular que la iluminación difusa.</span><span class="sxs-lookup"><span data-stu-id="2ad75-197">Specular lighting is more intensive to calculate than diffuse lighting.</span></span> <span data-ttu-id="2ad75-198">Normalmente se usa para proporcionar pistas visuales sobre el material de superficie.</span><span class="sxs-lookup"><span data-stu-id="2ad75-198">It is typically used to provide visual clues about the surface material.</span></span> <span data-ttu-id="2ad75-199">El resaltado especular varía en tamaño y color con el material de la superficie.</span><span class="sxs-lookup"><span data-stu-id="2ad75-199">The specular highlight varies in size and color with the material of the surface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2ad75-200">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2ad75-200">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ad75-201">Matemáticas de iluminación</span><span class="sxs-lookup"><span data-stu-id="2ad75-201">Mathematics of Lighting</span></span>](mathematics-of-lighting.md)
</dt> </dl>

 

 



