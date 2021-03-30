---
description: Los componentes de iluminación difusa y especular de la ecuación de iluminación global contienen términos que describen la atenuación de luz y el cono de foco. Estos términos se describen a continuación.
ms.assetid: 960b5fc2-3074-4e51-b3de-5ed370379b01
title: Atenuación y factor de Spotlight (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 623bb3cb2b1c2a3ee9e0e5d9419ff71dd9a303b6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104552825"
---
# <a name="attenuation-and-spotlight-factor-direct3d-9"></a><span data-ttu-id="4446b-104">Atenuación y factor de Spotlight (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="4446b-104">Attenuation and Spotlight Factor (Direct3D 9)</span></span>

<span data-ttu-id="4446b-105">Los componentes de iluminación difusa y especular de la ecuación de iluminación global contienen términos que describen la atenuación de luz y el cono de foco.</span><span class="sxs-lookup"><span data-stu-id="4446b-105">The diffuse and specular lighting components of the global illumination equation contain terms that describe light attenuation and the spotlight cone.</span></span> <span data-ttu-id="4446b-106">Estos términos se describen a continuación.</span><span class="sxs-lookup"><span data-stu-id="4446b-106">These terms are described below.</span></span>

## <a name="attenuation"></a><span data-ttu-id="4446b-107">Atenuación</span><span class="sxs-lookup"><span data-stu-id="4446b-107">Attenuation</span></span>

<span data-ttu-id="4446b-108">La atenuación de una luz depende del tipo de luz y de la distancia entre la luz y la posición del vértice.</span><span class="sxs-lookup"><span data-stu-id="4446b-108">The attenuation of a light depends on the type of light and the distance between the light and the vertex position.</span></span> <span data-ttu-id="4446b-109">Para calcular la atenuación, use una de las siguientes ecuaciones.</span><span class="sxs-lookup"><span data-stu-id="4446b-109">To calculate attenuation, use one of the following equations.</span></span>

<span data-ttu-id="4446b-110">ATTEN = 1/(att0<sub>i</sub> + Att1<sub>i</sub> \* d + Att2<sub>i</sub> \* d ²)</span><span class="sxs-lookup"><span data-stu-id="4446b-110">Atten = 1/( att0<sub>i</sub> + att1<sub>i</sub> \* d + att2<sub>i</sub> \* d²)</span></span>

<span data-ttu-id="4446b-111">Donde:</span><span class="sxs-lookup"><span data-stu-id="4446b-111">Where:</span></span>



| <span data-ttu-id="4446b-112">Parámetro</span><span class="sxs-lookup"><span data-stu-id="4446b-112">Parameter</span></span>        | <span data-ttu-id="4446b-113">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="4446b-113">Default value</span></span> | <span data-ttu-id="4446b-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="4446b-114">Type</span></span>  | <span data-ttu-id="4446b-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="4446b-115">Description</span></span>                                     | <span data-ttu-id="4446b-116">Intervalo</span><span class="sxs-lookup"><span data-stu-id="4446b-116">Range</span></span>          |
|------------------|---------------|-------|-------------------------------------------------|----------------|
| <span data-ttu-id="4446b-117">att0<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="4446b-117">att0<sub>i</sub></span></span> | <span data-ttu-id="4446b-118">0,0</span><span class="sxs-lookup"><span data-stu-id="4446b-118">0.0</span></span>           | <span data-ttu-id="4446b-119">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4446b-119">FLOAT</span></span> | <span data-ttu-id="4446b-120">Factor de atenuación constante</span><span class="sxs-lookup"><span data-stu-id="4446b-120">Constant attenuation factor</span></span>                     | <span data-ttu-id="4446b-121">de 0 a + infinito</span><span class="sxs-lookup"><span data-stu-id="4446b-121">0 to +infinity</span></span> |
| <span data-ttu-id="4446b-122">Att1<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="4446b-122">att1<sub>i</sub></span></span> | <span data-ttu-id="4446b-123">0,0</span><span class="sxs-lookup"><span data-stu-id="4446b-123">0.0</span></span>           | <span data-ttu-id="4446b-124">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4446b-124">FLOAT</span></span> | <span data-ttu-id="4446b-125">Factor de atenuación lineal</span><span class="sxs-lookup"><span data-stu-id="4446b-125">Linear attenuation factor</span></span>                       | <span data-ttu-id="4446b-126">de 0 a + infinito</span><span class="sxs-lookup"><span data-stu-id="4446b-126">0 to +infinity</span></span> |
| <span data-ttu-id="4446b-127">Att2<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="4446b-127">att2<sub>i</sub></span></span> | <span data-ttu-id="4446b-128">0,0</span><span class="sxs-lookup"><span data-stu-id="4446b-128">0.0</span></span>           | <span data-ttu-id="4446b-129">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4446b-129">FLOAT</span></span> | <span data-ttu-id="4446b-130">Factor de atenuación cuadrático</span><span class="sxs-lookup"><span data-stu-id="4446b-130">Quadratic attenuation factor</span></span>                    | <span data-ttu-id="4446b-131">de 0 a + infinito</span><span class="sxs-lookup"><span data-stu-id="4446b-131">0 to +infinity</span></span> |
| <span data-ttu-id="4446b-132">d</span><span class="sxs-lookup"><span data-stu-id="4446b-132">d</span></span>                | <span data-ttu-id="4446b-133">N/D</span><span class="sxs-lookup"><span data-stu-id="4446b-133">N/A</span></span>           | <span data-ttu-id="4446b-134">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4446b-134">FLOAT</span></span> | <span data-ttu-id="4446b-135">Distancia desde la posición del vértice hasta la posición de la luz</span><span class="sxs-lookup"><span data-stu-id="4446b-135">Distance from vertex position to light position</span></span> | <span data-ttu-id="4446b-136">N/D</span><span class="sxs-lookup"><span data-stu-id="4446b-136">N/A</span></span>            |



 

-   <span data-ttu-id="4446b-137">ATTEN = 1, si la luz es una luz direccional.</span><span class="sxs-lookup"><span data-stu-id="4446b-137">Atten = 1, if the light is a directional light.</span></span>
-   <span data-ttu-id="4446b-138">ATTEN = 0, si la distancia entre la luz y el vértice supera el intervalo de la luz.</span><span class="sxs-lookup"><span data-stu-id="4446b-138">Atten = 0, if the distance between the light and the vertex exceeds the light's range.</span></span>

<span data-ttu-id="4446b-139">Los valores att0, Att1, Att2 se especifican mediante los miembros Attenuation0, Attenuation1 y Attenuation2 de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="4446b-139">The att0, att1, att2 values are specified by the Attenuation0, Attenuation1, and Attenuation2 members of [**D3DLIGHT9**](d3dlight9.md).</span></span>

<span data-ttu-id="4446b-140">La distancia entre la luz y la posición del vértice siempre es positiva.</span><span class="sxs-lookup"><span data-stu-id="4446b-140">The distance between the light and the vertex position is always positive.</span></span>

<span data-ttu-id="4446b-141">d = \| <sub>directorio</sub> L \|</span><span class="sxs-lookup"><span data-stu-id="4446b-141">d = \| L<sub>dir</sub> \|</span></span>

<span data-ttu-id="4446b-142">Donde:</span><span class="sxs-lookup"><span data-stu-id="4446b-142">Where:</span></span>



| <span data-ttu-id="4446b-143">Parámetro</span><span class="sxs-lookup"><span data-stu-id="4446b-143">Parameter</span></span>       | <span data-ttu-id="4446b-144">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="4446b-144">Default value</span></span> | <span data-ttu-id="4446b-145">Tipo</span><span class="sxs-lookup"><span data-stu-id="4446b-145">Type</span></span>      | <span data-ttu-id="4446b-146">Descripción</span><span class="sxs-lookup"><span data-stu-id="4446b-146">Description</span></span>                                                 |
|-----------------|---------------|-----------|-------------------------------------------------------------|
| <span data-ttu-id="4446b-147"><sub>Directorio</sub> L</span><span class="sxs-lookup"><span data-stu-id="4446b-147">L<sub>dir</sub></span></span> | <span data-ttu-id="4446b-148">N/D</span><span class="sxs-lookup"><span data-stu-id="4446b-148">N/A</span></span>           | <span data-ttu-id="4446b-149">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="4446b-149">D3DVECTOR</span></span> | <span data-ttu-id="4446b-150">Vector de dirección desde la posición del vértice hasta la posición de la luz</span><span class="sxs-lookup"><span data-stu-id="4446b-150">Direction vector from vertex position to the light position</span></span> |



 

<span data-ttu-id="4446b-151">Si d es mayor que el intervalo de la luz, es decir, el miembro del intervalo de una estructura [**D3DLIGHT9**](d3dlight9.md) , Direct3D no realiza más cálculos de atenuación y no aplica ningún efecto de la luz al vértice.</span><span class="sxs-lookup"><span data-stu-id="4446b-151">If d is greater than the light's range, that is, the Range member of a [**D3DLIGHT9**](d3dlight9.md) structure, Direct3D makes no further attenuation calculations and applies no effects from the light to the vertex.</span></span>

<span data-ttu-id="4446b-152">Las constantes de atenuación actúan como coeficientes en la fórmula; puede generar diversas curvas de atenuación realizando ajustes sencillos en ellas.</span><span class="sxs-lookup"><span data-stu-id="4446b-152">The attenuation constants act as coefficients in the formula - you can produce a variety of attenuation curves by making simple adjustments to them.</span></span> <span data-ttu-id="4446b-153">Puede establecer Attenuation1 en 1,0 para crear una luz que no se atenuará pero que siga limitada por el intervalo, o puede experimentar con valores diferentes para lograr distintos efectos de atenuación.</span><span class="sxs-lookup"><span data-stu-id="4446b-153">You can set Attenuation1 to 1.0 to create a light that doesn't attenuate but is still limited by range, or you can experiment with different values to achieve various attenuation effects.</span></span>

<span data-ttu-id="4446b-154">La atenuación en el intervalo máximo de la luz no es 0,0.</span><span class="sxs-lookup"><span data-stu-id="4446b-154">The attenuation at the maximum range of the light is not 0.0.</span></span> <span data-ttu-id="4446b-155">Para evitar que las luces aparezcan repentinamente cuando están en el intervalo de luz, una aplicación puede aumentar el intervalo de luz.</span><span class="sxs-lookup"><span data-stu-id="4446b-155">To prevent lights from suddenly appearing when they are at the light range, an application can increase the light range.</span></span> <span data-ttu-id="4446b-156">O bien, la aplicación puede configurar constantes de atenuación para que el factor de atenuación esté cerca de 0,0 en el intervalo de luz.</span><span class="sxs-lookup"><span data-stu-id="4446b-156">Or, the application can set up attenuation constants so that the attenuation factor is close to 0.0 at the light range.</span></span> <span data-ttu-id="4446b-157">El valor de atenuación se multiplica por los componentes rojo, verde y azul del color de la luz para escalar la intensidad de la luz como un factor de la luz de distancia que se desplaza a un vértice.</span><span class="sxs-lookup"><span data-stu-id="4446b-157">The attenuation value is multiplied by the red, green, and blue components of the light's color to scale the light's intensity as a factor of the distance light travels to a vertex.</span></span>

## <a name="spotlight-factor"></a><span data-ttu-id="4446b-158">Factor destacado</span><span class="sxs-lookup"><span data-stu-id="4446b-158">Spotlight Factor</span></span>

<span data-ttu-id="4446b-159">La siguiente ecuación especifica el factor destacado.</span><span class="sxs-lookup"><span data-stu-id="4446b-159">The following equation specifies the spotlight factor.</span></span>

![ecuación del factor de Spotlight](images/dx8light9.png)



| <span data-ttu-id="4446b-161">Parámetro</span><span class="sxs-lookup"><span data-stu-id="4446b-161">Parameter</span></span>         | <span data-ttu-id="4446b-162">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="4446b-162">Default value</span></span> | <span data-ttu-id="4446b-163">Tipo</span><span class="sxs-lookup"><span data-stu-id="4446b-163">Type</span></span>  | <span data-ttu-id="4446b-164">Descripción</span><span class="sxs-lookup"><span data-stu-id="4446b-164">Description</span></span>                              | <span data-ttu-id="4446b-165">Intervalo</span><span class="sxs-lookup"><span data-stu-id="4446b-165">Range</span></span>                    |
|-------------------|---------------|-------|------------------------------------------|--------------------------|
| <span data-ttu-id="4446b-166">Rho<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="4446b-166">rho<sub>i</sub></span></span>   | <span data-ttu-id="4446b-167">N/D</span><span class="sxs-lookup"><span data-stu-id="4446b-167">N/A</span></span>           | <span data-ttu-id="4446b-168">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4446b-168">FLOAT</span></span> | <span data-ttu-id="4446b-169">coseno (ángulo) para los focos</span><span class="sxs-lookup"><span data-stu-id="4446b-169">cosine(angle) for spotlight i</span></span>            | <span data-ttu-id="4446b-170">N/D</span><span class="sxs-lookup"><span data-stu-id="4446b-170">N/A</span></span>                      |
| <span data-ttu-id="4446b-171">Phi<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="4446b-171">phi<sub>i</sub></span></span>   | <span data-ttu-id="4446b-172">0,0</span><span class="sxs-lookup"><span data-stu-id="4446b-172">0.0</span></span>           | <span data-ttu-id="4446b-173">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4446b-173">FLOAT</span></span> | <span data-ttu-id="4446b-174">Penumbra ángulo de foco i en radianes</span><span class="sxs-lookup"><span data-stu-id="4446b-174">Penumbra angle of spotlight i in radians</span></span> | <span data-ttu-id="4446b-175">\[Theta<sub>i</sub>, PI)</span><span class="sxs-lookup"><span data-stu-id="4446b-175">\[theta<sub>i</sub>, pi)</span></span> |
| <span data-ttu-id="4446b-176">Theta<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="4446b-176">theta<sub>i</sub></span></span> | <span data-ttu-id="4446b-177">0,0</span><span class="sxs-lookup"><span data-stu-id="4446b-177">0.0</span></span>           | <span data-ttu-id="4446b-178">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4446b-178">FLOAT</span></span> | <span data-ttu-id="4446b-179">Umbra ángulo de foco i en radianes</span><span class="sxs-lookup"><span data-stu-id="4446b-179">Umbra angle of spotlight i in radians</span></span>    | <span data-ttu-id="4446b-180">\[0, PI)</span><span class="sxs-lookup"><span data-stu-id="4446b-180">\[0, pi)</span></span>                 |
| <span data-ttu-id="4446b-181">disminución</span><span class="sxs-lookup"><span data-stu-id="4446b-181">falloff</span></span>           | <span data-ttu-id="4446b-182">0,0</span><span class="sxs-lookup"><span data-stu-id="4446b-182">0.0</span></span>           | <span data-ttu-id="4446b-183">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4446b-183">FLOAT</span></span> | <span data-ttu-id="4446b-184">Factor de difuminación</span><span class="sxs-lookup"><span data-stu-id="4446b-184">Falloff factor</span></span>                           | <span data-ttu-id="4446b-185">(-Infinity, + infinito)</span><span class="sxs-lookup"><span data-stu-id="4446b-185">(-infinity, +infinity)</span></span>   |



 

<span data-ttu-id="4446b-186">Donde:</span><span class="sxs-lookup"><span data-stu-id="4446b-186">Where:</span></span>

<span data-ttu-id="4446b-187">Rho = norma (L<sub>DC</sub>)<sup>.</sup> norma (L<sub>dir</sub>)</span><span class="sxs-lookup"><span data-stu-id="4446b-187">rho = norm(L<sub>dcs</sub>)<sup>.</sup>norm(L<sub>dir</sub>)</span></span>

<span data-ttu-id="4446b-188">y:</span><span class="sxs-lookup"><span data-stu-id="4446b-188">and:</span></span>



| <span data-ttu-id="4446b-189">Parámetro</span><span class="sxs-lookup"><span data-stu-id="4446b-189">Parameter</span></span>       | <span data-ttu-id="4446b-190">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="4446b-190">Default value</span></span> | <span data-ttu-id="4446b-191">Tipo</span><span class="sxs-lookup"><span data-stu-id="4446b-191">Type</span></span>      | <span data-ttu-id="4446b-192">Descripción</span><span class="sxs-lookup"><span data-stu-id="4446b-192">Description</span></span>                                                 |
|-----------------|---------------|-----------|-------------------------------------------------------------|
| <span data-ttu-id="4446b-193"><sub>DC</sub> de L</span><span class="sxs-lookup"><span data-stu-id="4446b-193">L<sub>dcs</sub></span></span> | <span data-ttu-id="4446b-194">N/D</span><span class="sxs-lookup"><span data-stu-id="4446b-194">N/A</span></span>           | <span data-ttu-id="4446b-195">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="4446b-195">D3DVECTOR</span></span> | <span data-ttu-id="4446b-196">El negativo de la dirección de la luz en el espacio de la cámara</span><span class="sxs-lookup"><span data-stu-id="4446b-196">The negative of the light direction in camera space</span></span>         |
| <span data-ttu-id="4446b-197"><sub>Directorio</sub> L</span><span class="sxs-lookup"><span data-stu-id="4446b-197">L<sub>dir</sub></span></span> | <span data-ttu-id="4446b-198">N/D</span><span class="sxs-lookup"><span data-stu-id="4446b-198">N/A</span></span>           | <span data-ttu-id="4446b-199">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="4446b-199">D3DVECTOR</span></span> | <span data-ttu-id="4446b-200">Vector de dirección desde la posición del vértice hasta la posición de la luz</span><span class="sxs-lookup"><span data-stu-id="4446b-200">Direction vector from vertex position to the light position</span></span> |



 

<span data-ttu-id="4446b-201">Después de calcular la atenuación de luz, Direct3D también tiene en cuenta los efectos destacados, si procede, el ángulo que la luz refleja de una superficie y la reflectancia del material actual para calcular los componentes difusos y especulares para ese vértice.</span><span class="sxs-lookup"><span data-stu-id="4446b-201">After computing the light attenuation, Direct3D also considers spotlight effects if applicable, the angle that the light reflects from a surface, and the reflectance of the current material to calculate the diffuse and specular components for that vertex.</span></span> <span data-ttu-id="4446b-202">Para obtener más información, consulte [Spotlight](light-types.md).</span><span class="sxs-lookup"><span data-stu-id="4446b-202">For more information, see [SpotLight](light-types.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4446b-203">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4446b-203">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4446b-204">Matemáticas de iluminación</span><span class="sxs-lookup"><span data-stu-id="4446b-204">Mathematics of Lighting</span></span>](mathematics-of-lighting.md)
</dt> </dl>

 

 



