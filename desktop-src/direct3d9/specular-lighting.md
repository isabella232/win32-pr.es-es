---
description: El modelado de reflexión especular requiere que el sistema no solo sepa en qué dirección se desplaza la luz, sino también la dirección del ojo del espectador.
ms.assetid: 35da0ac3-4e68-4d37-a987-405fc15d0cbf
title: Iluminación especular (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ab378d4ca3f00ef81c5048e6ad6cc85eaeb18ad
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104559524"
---
# <a name="specular-lighting-direct3d-9"></a><span data-ttu-id="1dcb6-103">Iluminación especular (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1dcb6-103">Specular Lighting (Direct3D 9)</span></span>

<span data-ttu-id="1dcb6-104">El modelado de reflexión especular requiere que el sistema no solo sepa en qué dirección se desplaza la luz, sino también la dirección del ojo del espectador.</span><span class="sxs-lookup"><span data-stu-id="1dcb6-104">Modeling specular reflection requires that the system not only know in what direction light is traveling, but also the direction to the viewer's eye.</span></span> <span data-ttu-id="1dcb6-105">El sistema utiliza una versión simplificada del modelo de reflexión especular de Phong, que emplea un vector a la mitad para aproximar la intensidad de reflexión especular.</span><span class="sxs-lookup"><span data-stu-id="1dcb6-105">The system uses a simplified version of the Phong specular-reflection model, which employs a halfway vector to approximate the intensity of specular reflection.</span></span>

<span data-ttu-id="1dcb6-106">El estado de iluminación predeterminado no calcula los reflejos especulares.</span><span class="sxs-lookup"><span data-stu-id="1dcb6-106">The default lighting state does not calculate specular highlights.</span></span> <span data-ttu-id="1dcb6-107">Para habilitar la iluminación especular, asegúrese de establecer D3DRS \_ SPECULARENABLE en **true**.</span><span class="sxs-lookup"><span data-stu-id="1dcb6-107">To enable specular lighting, be sure to set D3DRS\_SPECULARENABLE to **TRUE**.</span></span>

## <a name="specular-lighting-equation"></a><span data-ttu-id="1dcb6-108">Ecuación de iluminación especular</span><span class="sxs-lookup"><span data-stu-id="1dcb6-108">Specular Lighting Equation</span></span>

<span data-ttu-id="1dcb6-109">La iluminación especular se describe mediante la siguiente ecuación.</span><span class="sxs-lookup"><span data-stu-id="1dcb6-109">Specular Lighting is described by the following equation.</span></span>



|                                                                             |
|-----------------------------------------------------------------------------|
| <span data-ttu-id="1dcb6-110">Iluminación especular = CS \* SUM \[ LS \* (N · H)<sup>P</sup> \* ATTEN \*\]</span><span class="sxs-lookup"><span data-stu-id="1dcb6-110">Specular Lighting = Cₛ \* sum\[Lₛ \* (N · H)<sup>P</sup> \* Atten \* Spot\]</span></span> |



 

<span data-ttu-id="1dcb6-111">En la tabla siguiente se identifican las variables, sus tipos y sus intervalos.</span><span class="sxs-lookup"><span data-stu-id="1dcb6-111">The following table identifies the variables, their types, and their ranges.</span></span>



| <span data-ttu-id="1dcb6-112">Parámetro</span><span class="sxs-lookup"><span data-stu-id="1dcb6-112">Parameter</span></span>    | <span data-ttu-id="1dcb6-113">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="1dcb6-113">Default value</span></span> | <span data-ttu-id="1dcb6-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="1dcb6-114">Type</span></span>          | <span data-ttu-id="1dcb6-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="1dcb6-115">Description</span></span>                                                                                                         |
|--------------|---------------|---------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1dcb6-116">Estrategia</span><span class="sxs-lookup"><span data-stu-id="1dcb6-116">Cₛ</span></span>           | <span data-ttu-id="1dcb6-117">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="1dcb6-117">(0,0,0,0)</span></span>     | <span data-ttu-id="1dcb6-118">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="1dcb6-118">D3DCOLORVALUE</span></span> | <span data-ttu-id="1dcb6-119">Color especular.</span><span class="sxs-lookup"><span data-stu-id="1dcb6-119">Specular color.</span></span>                                                                                                     |
| <span data-ttu-id="1dcb6-120">Sum</span><span class="sxs-lookup"><span data-stu-id="1dcb6-120">sum</span></span>          | <span data-ttu-id="1dcb6-121">N/D</span><span class="sxs-lookup"><span data-stu-id="1dcb6-121">N/A</span></span>           | <span data-ttu-id="1dcb6-122">N/D</span><span class="sxs-lookup"><span data-stu-id="1dcb6-122">N/A</span></span>           | <span data-ttu-id="1dcb6-123">Suma del componente especular de cada luz.</span><span class="sxs-lookup"><span data-stu-id="1dcb6-123">Summation of each light's specular component.</span></span>                                                                       |
| <span data-ttu-id="1dcb6-124">N</span><span class="sxs-lookup"><span data-stu-id="1dcb6-124">N</span></span>            | <span data-ttu-id="1dcb6-125">N/D</span><span class="sxs-lookup"><span data-stu-id="1dcb6-125">N/A</span></span>           | <span data-ttu-id="1dcb6-126">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="1dcb6-126">D3DVECTOR</span></span>     | <span data-ttu-id="1dcb6-127">El vértice es normal.</span><span class="sxs-lookup"><span data-stu-id="1dcb6-127">Vertex normal.</span></span>                                                                                                      |
| <span data-ttu-id="1dcb6-128">H</span><span class="sxs-lookup"><span data-stu-id="1dcb6-128">H</span></span>            | <span data-ttu-id="1dcb6-129">N/D</span><span class="sxs-lookup"><span data-stu-id="1dcb6-129">N/A</span></span>           | <span data-ttu-id="1dcb6-130">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="1dcb6-130">D3DVECTOR</span></span>     | <span data-ttu-id="1dcb6-131">Vector medio.</span><span class="sxs-lookup"><span data-stu-id="1dcb6-131">Half way vector.</span></span> <span data-ttu-id="1dcb6-132">Vea la sección sobre el vector a la mitad.</span><span class="sxs-lookup"><span data-stu-id="1dcb6-132">See the section on the halfway vector.</span></span>                                                             |
| <span data-ttu-id="1dcb6-133"><sup>P</sup></span><span class="sxs-lookup"><span data-stu-id="1dcb6-133"><sup>P</sup></span></span> | <span data-ttu-id="1dcb6-134">0,0</span><span class="sxs-lookup"><span data-stu-id="1dcb6-134">0.0</span></span>           | <span data-ttu-id="1dcb6-135">FLOAT</span><span class="sxs-lookup"><span data-stu-id="1dcb6-135">FLOAT</span></span>         | <span data-ttu-id="1dcb6-136">Potencia de reflexión especular.</span><span class="sxs-lookup"><span data-stu-id="1dcb6-136">Specular reflection power.</span></span> <span data-ttu-id="1dcb6-137">El intervalo es de 0 a + infinito</span><span class="sxs-lookup"><span data-stu-id="1dcb6-137">Range is 0 to +infinity</span></span>                                                                  |
| <span data-ttu-id="1dcb6-138">LS</span><span class="sxs-lookup"><span data-stu-id="1dcb6-138">Lₛ</span></span>           | <span data-ttu-id="1dcb6-139">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="1dcb6-139">(0,0,0,0)</span></span>     | <span data-ttu-id="1dcb6-140">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="1dcb6-140">D3DCOLORVALUE</span></span> | <span data-ttu-id="1dcb6-141">Color especular claro.</span><span class="sxs-lookup"><span data-stu-id="1dcb6-141">Light specular color.</span></span>                                                                                               |
| <span data-ttu-id="1dcb6-142">Atten</span><span class="sxs-lookup"><span data-stu-id="1dcb6-142">Atten</span></span>        | <span data-ttu-id="1dcb6-143">N/D</span><span class="sxs-lookup"><span data-stu-id="1dcb6-143">N/A</span></span>           | <span data-ttu-id="1dcb6-144">FLOAT</span><span class="sxs-lookup"><span data-stu-id="1dcb6-144">FLOAT</span></span>         | <span data-ttu-id="1dcb6-145">Valor de atenuación de luz.</span><span class="sxs-lookup"><span data-stu-id="1dcb6-145">Light attenuation value.</span></span> <span data-ttu-id="1dcb6-146">Vea [atenuación y factor de Spotlight (Direct3D 9)](attenuation-and-spotlight-factor.md).</span><span class="sxs-lookup"><span data-stu-id="1dcb6-146">See [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span> |
| <span data-ttu-id="1dcb6-147">Zona</span><span class="sxs-lookup"><span data-stu-id="1dcb6-147">Spot</span></span>         | <span data-ttu-id="1dcb6-148">N/D</span><span class="sxs-lookup"><span data-stu-id="1dcb6-148">N/A</span></span>           | <span data-ttu-id="1dcb6-149">FLOAT</span><span class="sxs-lookup"><span data-stu-id="1dcb6-149">FLOAT</span></span>         | <span data-ttu-id="1dcb6-150">Factor destacado.</span><span class="sxs-lookup"><span data-stu-id="1dcb6-150">Spotlight factor.</span></span> <span data-ttu-id="1dcb6-151">Vea [atenuación y factor de Spotlight (Direct3D 9)](attenuation-and-spotlight-factor.md).</span><span class="sxs-lookup"><span data-stu-id="1dcb6-151">See [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span>        |



 

<span data-ttu-id="1dcb6-152">El valor de CS es:</span><span class="sxs-lookup"><span data-stu-id="1dcb6-152">The value for Cₛ is either:</span></span>


```
if(SPECULARMATERIALSOURCE == D3DMCS_COLOR1)
  C = color1;
```



-   <span data-ttu-id="1dcb6-153">vértice color1, si el origen del material especular es D3DMCS \_ color1 y el primer color de vértice se proporciona en la declaración de vértices.</span><span class="sxs-lookup"><span data-stu-id="1dcb6-153">vertex color1, if the specular material source is D3DMCS\_COLOR1, and the first vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="1dcb6-154">Vertex color2, si el origen del material especular es D3DMCS \_ color2 y el segundo color de vértice se proporciona en la declaración de vértices.</span><span class="sxs-lookup"><span data-stu-id="1dcb6-154">vertex color2, if specular material source is D3DMCS\_COLOR2, and the second vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="1dcb6-155">color especular de material</span><span class="sxs-lookup"><span data-stu-id="1dcb6-155">material specular color</span></span>

> [!Note]  
> <span data-ttu-id="1dcb6-156">Si se usa la opción de origen de material especular y no se proporciona el color de vértice, se usa el color especular de material.</span><span class="sxs-lookup"><span data-stu-id="1dcb6-156">If either specular material source option is used and the vertex color is not provided, then the material specular color is used.</span></span>

 

<span data-ttu-id="1dcb6-157">Los componentes especulares están fijados de 0 a 255, después de que todas las luces se procesan y se interpolan por separado.</span><span class="sxs-lookup"><span data-stu-id="1dcb6-157">Specular components are clamped to be from 0 to 255, after all lights are processed and interpolated separately.</span></span>

## <a name="the-halfway-vector"></a><span data-ttu-id="1dcb6-158">Vector en la mitad</span><span class="sxs-lookup"><span data-stu-id="1dcb6-158">The Halfway Vector</span></span>

<span data-ttu-id="1dcb6-159">El vector medio (H) existe entre dos vectores: el vector de un vértice de objeto a la fuente de luz y el vector de un vértice de objeto a la posición de la cámara.</span><span class="sxs-lookup"><span data-stu-id="1dcb6-159">The halfway vector (H) exists midway between two vectors: the vector from an object vertex to the light source, and the vector from an object vertex to the camera position.</span></span> <span data-ttu-id="1dcb6-160">Direct3D proporciona dos maneras de calcular el vector a la mitad.</span><span class="sxs-lookup"><span data-stu-id="1dcb6-160">Direct3D provides two ways to compute the halfway vector.</span></span> <span data-ttu-id="1dcb6-161">Cuando D3DRS \_ LOCALVIEWER se establece en **true**, el sistema calcula el vector en la mitad con la posición de la cámara y la posición del vértice, junto con el vector de dirección de la luz.</span><span class="sxs-lookup"><span data-stu-id="1dcb6-161">When D3DRS\_LOCALVIEWER is set to **TRUE**, the system calculates the halfway vector using the position of the camera and the position of the vertex, along with the light's direction vector.</span></span> <span data-ttu-id="1dcb6-162">La siguiente fórmula ilustra esto.</span><span class="sxs-lookup"><span data-stu-id="1dcb6-162">The following formula illustrates this.</span></span>



|                                           |
|-------------------------------------------|
| <span data-ttu-id="1dcb6-163">H = norma (Norm (CP-VP) + L<sub>dir</sub>)</span><span class="sxs-lookup"><span data-stu-id="1dcb6-163">H = norm(norm(Cₚ - Vₚ) + L<sub>dir</sub>)</span></span> |



 



| <span data-ttu-id="1dcb6-164">Parámetro</span><span class="sxs-lookup"><span data-stu-id="1dcb6-164">Parameter</span></span>       | <span data-ttu-id="1dcb6-165">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="1dcb6-165">Default value</span></span> | <span data-ttu-id="1dcb6-166">Tipo</span><span class="sxs-lookup"><span data-stu-id="1dcb6-166">Type</span></span>      | <span data-ttu-id="1dcb6-167">Descripción</span><span class="sxs-lookup"><span data-stu-id="1dcb6-167">Description</span></span>                                                  |
|-----------------|---------------|-----------|--------------------------------------------------------------|
| <span data-ttu-id="1dcb6-168">CP</span><span class="sxs-lookup"><span data-stu-id="1dcb6-168">Cₚ</span></span>              | <span data-ttu-id="1dcb6-169">N/D</span><span class="sxs-lookup"><span data-stu-id="1dcb6-169">N/A</span></span>           | <span data-ttu-id="1dcb6-170">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="1dcb6-170">D3DVECTOR</span></span> | <span data-ttu-id="1dcb6-171">Posición de la cámara.</span><span class="sxs-lookup"><span data-stu-id="1dcb6-171">Camera position.</span></span>                                             |
| <span data-ttu-id="1dcb6-172">Expertos</span><span class="sxs-lookup"><span data-stu-id="1dcb6-172">Vₚ</span></span>              | <span data-ttu-id="1dcb6-173">N/D</span><span class="sxs-lookup"><span data-stu-id="1dcb6-173">N/A</span></span>           | <span data-ttu-id="1dcb6-174">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="1dcb6-174">D3DVECTOR</span></span> | <span data-ttu-id="1dcb6-175">Posición del vértice.</span><span class="sxs-lookup"><span data-stu-id="1dcb6-175">Vertex position.</span></span>                                             |
| <span data-ttu-id="1dcb6-176"><sub>Directorio</sub> L</span><span class="sxs-lookup"><span data-stu-id="1dcb6-176">L<sub>dir</sub></span></span> | <span data-ttu-id="1dcb6-177">N/D</span><span class="sxs-lookup"><span data-stu-id="1dcb6-177">N/A</span></span>           | <span data-ttu-id="1dcb6-178">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="1dcb6-178">D3DVECTOR</span></span> | <span data-ttu-id="1dcb6-179">Vector de dirección desde la posición del vértice hasta la posición de la luz.</span><span class="sxs-lookup"><span data-stu-id="1dcb6-179">Direction vector from vertex position to the light position.</span></span> |



 

<span data-ttu-id="1dcb6-180">Determinar el vector a la mitad de esta manera puede consumir un uso intensivo de los cálculos.</span><span class="sxs-lookup"><span data-stu-id="1dcb6-180">Determining the halfway vector in this manner can be computationally intensive.</span></span> <span data-ttu-id="1dcb6-181">Como alternativa, el establecimiento de D3DRS \_ LOCALVIEWER = **false** indica al sistema que actúe como si el punto de vista se distan infinitamente en el eje z.</span><span class="sxs-lookup"><span data-stu-id="1dcb6-181">As an alternative, setting D3DRS\_LOCALVIEWER = **FALSE** instructs the system to act as though the viewpoint is infinitely distant on the z-axis.</span></span> <span data-ttu-id="1dcb6-182">Esto se refleja en la siguiente fórmula.</span><span class="sxs-lookup"><span data-stu-id="1dcb6-182">This is reflected in the following formula.</span></span>



|                                     |
|-------------------------------------|
| <span data-ttu-id="1dcb6-183">H = normal ((0, 0, 1) + L<sub>dir</sub>)</span><span class="sxs-lookup"><span data-stu-id="1dcb6-183">H = norm((0,0,1) + L<sub>dir</sub>)</span></span> |



 

<span data-ttu-id="1dcb6-184">Este valor es menos computacionalmente intensivo, pero es mucho menos preciso, por lo que es mejor para las aplicaciones que usan la proyección ortogonal.</span><span class="sxs-lookup"><span data-stu-id="1dcb6-184">This setting is less computationally intensive, but much less accurate, so it is best used by applications that use orthogonal projection.</span></span>

## <a name="example"></a><span data-ttu-id="1dcb6-185">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1dcb6-185">Example</span></span>

<span data-ttu-id="1dcb6-186">En este ejemplo, el objeto se colorea utilizando el color de luz especular de la escena y un color especular de material.</span><span class="sxs-lookup"><span data-stu-id="1dcb6-186">In this example, the object is colored using the scene specular light color and a material specular color.</span></span> <span data-ttu-id="1dcb6-187">A continuación se muestra el código.</span><span class="sxs-lookup"><span data-stu-id="1dcb6-187">The code is shown below.</span></span>


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



<span data-ttu-id="1dcb6-188">Según la ecuación, el color resultante para los vértices del objeto es una combinación del color del material y el color claro.</span><span class="sxs-lookup"><span data-stu-id="1dcb6-188">According to the equation, the resulting color for the object vertices is a combination of the material color and the light color.</span></span>

<span data-ttu-id="1dcb6-189">En las dos ilustraciones siguientes se muestra el color del material especular, que está atenuado, y el color de luz especular, que es blanco.</span><span class="sxs-lookup"><span data-stu-id="1dcb6-189">The following two illustration show the specular material color, which is gray, and the specular light color, which is white.</span></span>

![Ilustración de una esfera gris](images/amb1.jpg)![Ilustración de una esfera blanca](images/lightwhite.jpg)

<span data-ttu-id="1dcb6-192">El resaltado especular resultante se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="1dcb6-192">The resulting specular highlight is shown in the following illustration.</span></span>

![Ilustración del resaltado especular](images/lights.jpg)

<span data-ttu-id="1dcb6-194">La combinación del resaltado especular con el ambiente y la iluminación difusa produce la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="1dcb6-194">Combining the specular highlight with the ambient and diffuse lighting produces the following illustration.</span></span> <span data-ttu-id="1dcb6-195">Con los tres tipos de iluminación aplicados, esto se parece más claramente a un objeto realista.</span><span class="sxs-lookup"><span data-stu-id="1dcb6-195">With all three types of lighting applied, this more clearly resembles a realistic object.</span></span>

![Ilustración de la combinación del resaltado especular, la iluminación ambiente y la iluminación difusa](images/lightads.jpg)

<span data-ttu-id="1dcb6-197">La iluminación especular es más intensiva para calcular que la luz difusa.</span><span class="sxs-lookup"><span data-stu-id="1dcb6-197">Specular lighting is more intensive to calculate than diffuse lighting.</span></span> <span data-ttu-id="1dcb6-198">Normalmente se usa para proporcionar pistas visuales sobre el material de la superficie.</span><span class="sxs-lookup"><span data-stu-id="1dcb6-198">It is typically used to provide visual clues about the surface material.</span></span> <span data-ttu-id="1dcb6-199">El resaltado especular varía en tamaño y color con el material de la superficie.</span><span class="sxs-lookup"><span data-stu-id="1dcb6-199">The specular highlight varies in size and color with the material of the surface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1dcb6-200">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1dcb6-200">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1dcb6-201">Matemáticas de iluminación</span><span class="sxs-lookup"><span data-stu-id="1dcb6-201">Mathematics of Lighting</span></span>](mathematics-of-lighting.md)
</dt> </dl>

 

 



