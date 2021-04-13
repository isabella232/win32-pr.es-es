---
description: La iluminación ambiente proporciona iluminación constante para una escena.
ms.assetid: 327095a7-f4e0-48c2-9e4d-bec8493fe37e
title: Iluminación ambiente (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e991981a9c1d7d24714e7014d08cefeaa94fe20f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539033"
---
# <a name="ambient-lighting-direct3d-9"></a><span data-ttu-id="9e4ed-103">Iluminación ambiente (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="9e4ed-103">Ambient Lighting (Direct3D 9)</span></span>

<span data-ttu-id="9e4ed-104">La iluminación ambiente proporciona iluminación constante para una escena.</span><span class="sxs-lookup"><span data-stu-id="9e4ed-104">Ambient lighting provides constant lighting for a scene.</span></span> <span data-ttu-id="9e4ed-105">Ilumina todos los vértices de objeto de la misma forma porque no depende de ningún otro factor de iluminación, como las normales de vértice, la dirección clara, la posición de la luz, el intervalo o la atenuación.</span><span class="sxs-lookup"><span data-stu-id="9e4ed-105">It lights all object vertices the same because it is not dependent on any other lighting factors such as vertex normals, light direction, light position, range, or attenuation.</span></span> <span data-ttu-id="9e4ed-106">Es el tipo de iluminación más rápido, pero genera los resultados menos realistas.</span><span class="sxs-lookup"><span data-stu-id="9e4ed-106">It is the fastest type of lighting but it produces the least realistic results.</span></span> <span data-ttu-id="9e4ed-107">Direct3D contiene una única propiedad de luz ambiente global que puede usar sin crear ninguna luz.</span><span class="sxs-lookup"><span data-stu-id="9e4ed-107">Direct3D contains a single global ambient light property that you can use without creating any light.</span></span> <span data-ttu-id="9e4ed-108">Como alternativa, puede establecer cualquier objeto de luz para proporcionar iluminación ambiente.</span><span class="sxs-lookup"><span data-stu-id="9e4ed-108">Alternatively, you can set any light object to provide ambient lighting.</span></span> <span data-ttu-id="9e4ed-109">La iluminación ambiente para una escena se describe en la siguiente ecuación.</span><span class="sxs-lookup"><span data-stu-id="9e4ed-109">The ambient lighting for a scene is described by the following equation.</span></span>

<span data-ttu-id="9e4ed-110">Iluminación ambiente = C ₐ \* \[ g ₐ + SUM (ATTEN<sub>i</sub>i i i e \* <sub></sub> \* <sub>IA</sub>)\]</span><span class="sxs-lookup"><span data-stu-id="9e4ed-110">Ambient Lighting = Cₐ\*\[Gₐ + sum(Atten<sub>i</sub>\*Spot<sub>i</sub>\*L<sub>ai</sub>)\]</span></span>

<span data-ttu-id="9e4ed-111">Donde:</span><span class="sxs-lookup"><span data-stu-id="9e4ed-111">Where:</span></span>



| <span data-ttu-id="9e4ed-112">Parámetro</span><span class="sxs-lookup"><span data-stu-id="9e4ed-112">Parameter</span></span>         | <span data-ttu-id="9e4ed-113">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="9e4ed-113">Default value</span></span> | <span data-ttu-id="9e4ed-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="9e4ed-114">Type</span></span>          | <span data-ttu-id="9e4ed-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="9e4ed-115">Description</span></span>                                                                                                                    |
|-------------------|---------------|---------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e4ed-116">C ₐ</span><span class="sxs-lookup"><span data-stu-id="9e4ed-116">Cₐ</span></span>                | <span data-ttu-id="9e4ed-117">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="9e4ed-117">(0,0,0,0)</span></span>     | <span data-ttu-id="9e4ed-118">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="9e4ed-118">D3DCOLORVALUE</span></span> | <span data-ttu-id="9e4ed-119">Color ambiental de material</span><span class="sxs-lookup"><span data-stu-id="9e4ed-119">Material ambient color</span></span>                                                                                                         |
| <span data-ttu-id="9e4ed-120">G ₐ</span><span class="sxs-lookup"><span data-stu-id="9e4ed-120">Gₐ</span></span>                | <span data-ttu-id="9e4ed-121">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="9e4ed-121">(0,0,0,0)</span></span>     | <span data-ttu-id="9e4ed-122">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="9e4ed-122">D3DCOLORVALUE</span></span> | <span data-ttu-id="9e4ed-123">Color ambiente global</span><span class="sxs-lookup"><span data-stu-id="9e4ed-123">Global ambient color</span></span>                                                                                                           |
| <span data-ttu-id="9e4ed-124">ATTEN<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="9e4ed-124">Atten<sub>i</sub></span></span> | <span data-ttu-id="9e4ed-125">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="9e4ed-125">(0,0,0,0)</span></span>     | <span data-ttu-id="9e4ed-126">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="9e4ed-126">D3DCOLORVALUE</span></span> | <span data-ttu-id="9e4ed-127">Atenuación de la luz i.</span><span class="sxs-lookup"><span data-stu-id="9e4ed-127">Light attenuation of the ith light.</span></span> <span data-ttu-id="9e4ed-128">Vea [atenuación y factor de Spotlight (Direct3D 9)](attenuation-and-spotlight-factor.md).</span><span class="sxs-lookup"><span data-stu-id="9e4ed-128">See [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span> |
| <span data-ttu-id="9e4ed-129">Puntual<sub></sub></span><span class="sxs-lookup"><span data-stu-id="9e4ed-129">Spot<sub>i</sub></span></span>  | <span data-ttu-id="9e4ed-130">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="9e4ed-130">(0,0,0,0)</span></span>     | <span data-ttu-id="9e4ed-131">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="9e4ed-131">D3DVECTOR</span></span>     | <span data-ttu-id="9e4ed-132">Factor destacado de la luz i.</span><span class="sxs-lookup"><span data-stu-id="9e4ed-132">Spotlight factor of the ith light.</span></span> <span data-ttu-id="9e4ed-133">Vea [atenuación y factor de Spotlight (Direct3D 9)](attenuation-and-spotlight-factor.md).</span><span class="sxs-lookup"><span data-stu-id="9e4ed-133">See [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span>  |
| <span data-ttu-id="9e4ed-134">Sum</span><span class="sxs-lookup"><span data-stu-id="9e4ed-134">sum</span></span>               | <span data-ttu-id="9e4ed-135">N/D</span><span class="sxs-lookup"><span data-stu-id="9e4ed-135">N/A</span></span>           | <span data-ttu-id="9e4ed-136">N/D</span><span class="sxs-lookup"><span data-stu-id="9e4ed-136">N/A</span></span>           | <span data-ttu-id="9e4ed-137">Suma de la luz ambiente</span><span class="sxs-lookup"><span data-stu-id="9e4ed-137">Sum of the ambient light</span></span>                                                                                                       |
| <span data-ttu-id="9e4ed-138">L<sub>AI</sub></span><span class="sxs-lookup"><span data-stu-id="9e4ed-138">L<sub>ai</sub></span></span>    | <span data-ttu-id="9e4ed-139">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="9e4ed-139">(0,0,0,0)</span></span>     | <span data-ttu-id="9e4ed-140">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="9e4ed-140">D3DVECTOR</span></span>     | <span data-ttu-id="9e4ed-141">Color ambiente claro de la luz iésimo</span><span class="sxs-lookup"><span data-stu-id="9e4ed-141">Light ambient color of the ith light</span></span>                                                                                           |



 

<span data-ttu-id="9e4ed-142">El valor de C ₐ es:</span><span class="sxs-lookup"><span data-stu-id="9e4ed-142">The value for Cₐ is either:</span></span>

-   <span data-ttu-id="9e4ed-143">Vertex color1, si AMBIENTMATERIALSOURCE = D3DMCS \_ color1, y el primer color de vértice se proporciona en la declaración de vértices.</span><span class="sxs-lookup"><span data-stu-id="9e4ed-143">vertex color1, if AMBIENTMATERIALSOURCE = D3DMCS\_COLOR1, and the first vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="9e4ed-144">Vertex color2, si AMBIENTMATERIALSOURCE = D3DMCS \_ color2, y el segundo color de vértice se proporciona en la declaración de vértices.</span><span class="sxs-lookup"><span data-stu-id="9e4ed-144">vertex color2, if AMBIENTMATERIALSOURCE = D3DMCS\_COLOR2, and the second vertex color is supplied in vertex declaration.</span></span>
-   <span data-ttu-id="9e4ed-145">color ambiente de material.</span><span class="sxs-lookup"><span data-stu-id="9e4ed-145">material ambient color.</span></span>

> [!Note]  
> <span data-ttu-id="9e4ed-146">Si se usa la opción AMBIENTMATERIALSOURCE y no se proporciona el color del vértice, se usa el color ambiente del material.</span><span class="sxs-lookup"><span data-stu-id="9e4ed-146">If either AMBIENTMATERIALSOURCE option is used, and the vertex color is not provided, then the material ambient color is used.</span></span>

 

<span data-ttu-id="9e4ed-147">Para usar el color ambiente de material, use SetMaterial como se muestra en el código de ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="9e4ed-147">To use the material ambient color, use SetMaterial as shown in the example code below.</span></span>

<span data-ttu-id="9e4ed-148">G ₐ es el color ambiente global.</span><span class="sxs-lookup"><span data-stu-id="9e4ed-148">Gₐ is the global ambient color.</span></span> <span data-ttu-id="9e4ed-149">Se establece mediante SetRenderState (D3DRS \_ ambiente).</span><span class="sxs-lookup"><span data-stu-id="9e4ed-149">It is set using SetRenderState(D3DRS\_AMBIENT).</span></span> <span data-ttu-id="9e4ed-150">Hay un color ambiente global en una escena de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="9e4ed-150">There is one global ambient color in a Direct3D scene.</span></span> <span data-ttu-id="9e4ed-151">Este parámetro no está asociado a un objeto de Direct3D Light.</span><span class="sxs-lookup"><span data-stu-id="9e4ed-151">This parameter is not associated with a Direct3D light object.</span></span>

<span data-ttu-id="9e4ed-152">L<sub>AI</sub> es el color ambiente de la luz iésimo de la escena.</span><span class="sxs-lookup"><span data-stu-id="9e4ed-152">L<sub>ai</sub> is the ambient color of the ith light in the scene.</span></span> <span data-ttu-id="9e4ed-153">Cada luz de Direct3D tiene un conjunto de propiedades, uno de los cuales es el color ambiente.</span><span class="sxs-lookup"><span data-stu-id="9e4ed-153">Each Direct3D light has a set of properties, one of which is the ambient color.</span></span> <span data-ttu-id="9e4ed-154">El término SUM (L<sub>AI</sub>) es una suma de todos los colores de ambiente de la escena.</span><span class="sxs-lookup"><span data-stu-id="9e4ed-154">The term, sum(L<sub>ai</sub>) is a sum of all the ambient colors in the scene.</span></span>

## <a name="example"></a><span data-ttu-id="9e4ed-155">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9e4ed-155">Example</span></span>

<span data-ttu-id="9e4ed-156">En este ejemplo, el objeto se colorea utilizando la luz ambiente de la escena y un color ambiente de material.</span><span class="sxs-lookup"><span data-stu-id="9e4ed-156">In this example, the object is colored using the scene ambient light and a material ambient color.</span></span>


```
#define GRAY_COLOR  0x00bfbfbf

// create material
D3DMATERIAL9 mtrl;
ZeroMemory(&mtrl, sizeof(mtrl));
mtrl.Ambient.r = 0.75f;
mtrl.Ambient.g = 0.0f;
mtrl.Ambient.b = 0.0f;
mtrl.Ambient.a = 0.0f;
m_pd3dDevice->SetMaterial(&mtrl);
m_pd3dDevice->SetRenderState(D3DRS_AMBIENT, GRAY_COLOR);
```



<span data-ttu-id="9e4ed-157">Según la ecuación, el color resultante para los vértices del objeto es una combinación del color del material y el color claro.</span><span class="sxs-lookup"><span data-stu-id="9e4ed-157">According to the equation, the resulting color for the object vertices is a combination of the material color and the light color.</span></span>

<span data-ttu-id="9e4ed-158">En las dos ilustraciones siguientes se muestra el color del material, que está atenuado y el color claro, que es rojo brillante.</span><span class="sxs-lookup"><span data-stu-id="9e4ed-158">The following two illustrations show the material color, which is gray, and the light color, which is bright red.</span></span>

![Ilustración de una esfera gris](images/amb1.jpg)![Ilustración de una esfera roja](images/lightred.jpg)

<span data-ttu-id="9e4ed-161">La escena resultante se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="9e4ed-161">The resulting scene is shown in the following illustration.</span></span> <span data-ttu-id="9e4ed-162">El único objeto de la escena es una esfera.</span><span class="sxs-lookup"><span data-stu-id="9e4ed-162">The only object in the scene is a sphere.</span></span> <span data-ttu-id="9e4ed-163">Luz ambiente ilumina todos los vértices de objetos con el mismo color.</span><span class="sxs-lookup"><span data-stu-id="9e4ed-163">Ambient light lights all object vertices with the same color.</span></span> <span data-ttu-id="9e4ed-164">No depende de la dirección de la luz o del vértice normal.</span><span class="sxs-lookup"><span data-stu-id="9e4ed-164">It is not dependent on the vertex normal or the light direction.</span></span> <span data-ttu-id="9e4ed-165">Como resultado, la esfera tiene el aspecto de un círculo 2D porque no hay ninguna diferencia en el sombreado en torno a la superficie del objeto.</span><span class="sxs-lookup"><span data-stu-id="9e4ed-165">As a result, the sphere looks like a 2D circle because there is no difference in shading around the surface of the object.</span></span>

![Ilustración de una esfera con iluminación ambiente](images/lighta.jpg)

<span data-ttu-id="9e4ed-167">Para dar una apariencia más realista a los objetos, aplique la iluminación difusa o especular además de la iluminación ambiente.</span><span class="sxs-lookup"><span data-stu-id="9e4ed-167">To give objects a more realistic look, apply diffuse or specular lighting in addition to ambient lighting.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9e4ed-168">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9e4ed-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e4ed-169">Matemáticas de iluminación</span><span class="sxs-lookup"><span data-stu-id="9e4ed-169">Mathematics of Lighting</span></span>](mathematics-of-lighting.md)
</dt> </dl>

 

 



