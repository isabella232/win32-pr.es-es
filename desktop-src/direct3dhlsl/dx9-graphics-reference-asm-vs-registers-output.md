---
title: Registros de salida
description: Registros de salida
ms.assetid: 44148185-1051-44b9-afde-a2ecd76c829f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e4a0b397d17b841877796bd9c33432896208ed6d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104996744"
---
# <a name="output-registers"></a><span data-ttu-id="b1fdf-103">Registros de salida</span><span class="sxs-lookup"><span data-stu-id="b1fdf-103">Output Registers</span></span>

-   <span data-ttu-id="b1fdf-104">Registro de color de vértice</span><span class="sxs-lookup"><span data-stu-id="b1fdf-104">Vertex Color Register</span></span>
-   <span data-ttu-id="b1fdf-105">Registro de niebla</span><span class="sxs-lookup"><span data-stu-id="b1fdf-105">Fog Register</span></span>
-   <span data-ttu-id="b1fdf-106">Registro de posición \_</span><span class="sxs-lookup"><span data-stu-id="b1fdf-106">Position\_Register</span></span>
-   <span data-ttu-id="b1fdf-107">\_Registro de tamaño de punto \_</span><span class="sxs-lookup"><span data-stu-id="b1fdf-107">Point\_Size\_Register</span></span>
-   <span data-ttu-id="b1fdf-108">\_Registro de coordenadas de textura \_</span><span class="sxs-lookup"><span data-stu-id="b1fdf-108">Texture\_Coordinate\_Register</span></span>

<span data-ttu-id="b1fdf-109">Los nombres de registro están precedidos por una letra minúscula o, lo que indica que los registros de salida son de solo escritura.</span><span class="sxs-lookup"><span data-stu-id="b1fdf-109">Register names are preceded by a lowercase letter o, indicating that the output registers are write-only.</span></span>

## <a name="vertex-color-register---od0-od1"></a><span data-ttu-id="b1fdf-110">Color de vértice registro: oD0, oD1</span><span class="sxs-lookup"><span data-stu-id="b1fdf-110">Vertex Color Register - oD0, oD1</span></span>

<span data-ttu-id="b1fdf-111">oD0 es el registro de color difuso.</span><span class="sxs-lookup"><span data-stu-id="b1fdf-111">oD0 is the diffuse color register.</span></span> <span data-ttu-id="b1fdf-112">oD1 es el registro de color especular.</span><span class="sxs-lookup"><span data-stu-id="b1fdf-112">oD1 is the specular color register.</span></span> <span data-ttu-id="b1fdf-113">El valor de oD0 se interpola y se escribe en el registro de color de entrada 0 (V0) del sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="b1fdf-113">The oD0 value is interpolated and is written to the input color register 0 (v0) of the pixel shader.</span></span> <span data-ttu-id="b1fdf-114">El valor oD1 se interpola y se escribe en el registro del color de entrada 1 (V1) del sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="b1fdf-114">The oD1 value is interpolated and written to the input color register 1 (v1) of the pixel shader.</span></span> <span data-ttu-id="b1fdf-115">Para obtener más información sobre los registros de color del sombreador de píxeles, consulte registros.</span><span class="sxs-lookup"><span data-stu-id="b1fdf-115">For more information about pixel shader color registers, see Registers.</span></span>



| <span data-ttu-id="b1fdf-116">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="b1fdf-116">Vertex shader versions</span></span> | <span data-ttu-id="b1fdf-117">1\_1</span><span class="sxs-lookup"><span data-stu-id="b1fdf-117">1\_1</span></span> | <span data-ttu-id="b1fdf-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b1fdf-118">2\_0</span></span> | <span data-ttu-id="b1fdf-119">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b1fdf-119">2\_sw</span></span> | <span data-ttu-id="b1fdf-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b1fdf-120">2\_x</span></span> | <span data-ttu-id="b1fdf-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b1fdf-121">3\_0</span></span> | <span data-ttu-id="b1fdf-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b1fdf-122">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="b1fdf-123">Registro de color de vértice</span><span class="sxs-lookup"><span data-stu-id="b1fdf-123">Vertex Color Register</span></span>  | <span data-ttu-id="b1fdf-124">x</span><span class="sxs-lookup"><span data-stu-id="b1fdf-124">x</span></span>    | <span data-ttu-id="b1fdf-125">x</span><span class="sxs-lookup"><span data-stu-id="b1fdf-125">x</span></span>    | <span data-ttu-id="b1fdf-126">x</span><span class="sxs-lookup"><span data-stu-id="b1fdf-126">x</span></span>     | <span data-ttu-id="b1fdf-127">x</span><span class="sxs-lookup"><span data-stu-id="b1fdf-127">x</span></span>    |      |       |



 

## <a name="fog-register---ofog"></a><span data-ttu-id="b1fdf-128">Registro de niebla: oFog</span><span class="sxs-lookup"><span data-stu-id="b1fdf-128">Fog Register - oFog</span></span>

<span data-ttu-id="b1fdf-129">El valor de niebla de salida se registra.</span><span class="sxs-lookup"><span data-stu-id="b1fdf-129">The output fog value registers.</span></span> <span data-ttu-id="b1fdf-130">El valor es el factor de niebla que se va a interpolar y, a continuación, enrutar a la tabla de niebla.</span><span class="sxs-lookup"><span data-stu-id="b1fdf-130">The value is the fog factor to be interpolated and then routed to the fog table.</span></span> <span data-ttu-id="b1fdf-131">Solo se usa el componente x escalar de la niebla.</span><span class="sxs-lookup"><span data-stu-id="b1fdf-131">Only the scalar x-component of the fog is used.</span></span> <span data-ttu-id="b1fdf-132">Los valores se fijan entre cero y uno antes de pasar al rasterizador.</span><span class="sxs-lookup"><span data-stu-id="b1fdf-132">Values are clamped between zero and one before passing to the rasterizer.</span></span>



| <span data-ttu-id="b1fdf-133">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="b1fdf-133">Vertex shader versions</span></span> | <span data-ttu-id="b1fdf-134">1\_1</span><span class="sxs-lookup"><span data-stu-id="b1fdf-134">1\_1</span></span> | <span data-ttu-id="b1fdf-135">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b1fdf-135">2\_0</span></span> | <span data-ttu-id="b1fdf-136">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b1fdf-136">2\_sw</span></span> | <span data-ttu-id="b1fdf-137">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b1fdf-137">2\_x</span></span> | <span data-ttu-id="b1fdf-138">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b1fdf-138">3\_0</span></span> | <span data-ttu-id="b1fdf-139">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b1fdf-139">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="b1fdf-140">Registro de niebla</span><span class="sxs-lookup"><span data-stu-id="b1fdf-140">Fog Register</span></span>           | <span data-ttu-id="b1fdf-141">x</span><span class="sxs-lookup"><span data-stu-id="b1fdf-141">x</span></span>    | <span data-ttu-id="b1fdf-142">x</span><span class="sxs-lookup"><span data-stu-id="b1fdf-142">x</span></span>    | <span data-ttu-id="b1fdf-143">x</span><span class="sxs-lookup"><span data-stu-id="b1fdf-143">x</span></span>     | <span data-ttu-id="b1fdf-144">x</span><span class="sxs-lookup"><span data-stu-id="b1fdf-144">x</span></span>    |      |       |



 

## <a name="position-register---opos"></a><span data-ttu-id="b1fdf-145">Posición Register-oPos</span><span class="sxs-lookup"><span data-stu-id="b1fdf-145">Position Register - oPos</span></span>

<span data-ttu-id="b1fdf-146">La posición de salida se registra.</span><span class="sxs-lookup"><span data-stu-id="b1fdf-146">The output position registers.</span></span> <span data-ttu-id="b1fdf-147">El valor es la posición en el espacio de recorte homogéneo.</span><span class="sxs-lookup"><span data-stu-id="b1fdf-147">The value is the position in homogeneous clipping space.</span></span> <span data-ttu-id="b1fdf-148">Este valor debe escribirse en el sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="b1fdf-148">This value must be written by the vertex shader.</span></span>



| <span data-ttu-id="b1fdf-149">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="b1fdf-149">Vertex shader versions</span></span> | <span data-ttu-id="b1fdf-150">1\_1</span><span class="sxs-lookup"><span data-stu-id="b1fdf-150">1\_1</span></span> | <span data-ttu-id="b1fdf-151">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b1fdf-151">2\_0</span></span> | <span data-ttu-id="b1fdf-152">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b1fdf-152">2\_sw</span></span> | <span data-ttu-id="b1fdf-153">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b1fdf-153">2\_x</span></span> | <span data-ttu-id="b1fdf-154">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b1fdf-154">3\_0</span></span> | <span data-ttu-id="b1fdf-155">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b1fdf-155">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="b1fdf-156">Registro de posición</span><span class="sxs-lookup"><span data-stu-id="b1fdf-156">Position Register</span></span>      | <span data-ttu-id="b1fdf-157">x</span><span class="sxs-lookup"><span data-stu-id="b1fdf-157">x</span></span>    | <span data-ttu-id="b1fdf-158">x</span><span class="sxs-lookup"><span data-stu-id="b1fdf-158">x</span></span>    | <span data-ttu-id="b1fdf-159">x</span><span class="sxs-lookup"><span data-stu-id="b1fdf-159">x</span></span>     | <span data-ttu-id="b1fdf-160">x</span><span class="sxs-lookup"><span data-stu-id="b1fdf-160">x</span></span>    |      |       |



 

## <a name="point-size-register---opts"></a><span data-ttu-id="b1fdf-161">Registro de tamaño de punto: OPC</span><span class="sxs-lookup"><span data-stu-id="b1fdf-161">Point Size Register - oPts</span></span>

<span data-ttu-id="b1fdf-162">Los registros de tamaño de punto de salida.</span><span class="sxs-lookup"><span data-stu-id="b1fdf-162">The output point-size registers.</span></span> <span data-ttu-id="b1fdf-163">Solo se usa el componente x escalar del tamaño de punto.</span><span class="sxs-lookup"><span data-stu-id="b1fdf-163">Only the scalar x-component of the point size is used.</span></span>



| <span data-ttu-id="b1fdf-164">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="b1fdf-164">Vertex shader versions</span></span> | <span data-ttu-id="b1fdf-165">1\_1</span><span class="sxs-lookup"><span data-stu-id="b1fdf-165">1\_1</span></span> | <span data-ttu-id="b1fdf-166">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b1fdf-166">2\_0</span></span> | <span data-ttu-id="b1fdf-167">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b1fdf-167">2\_sw</span></span> | <span data-ttu-id="b1fdf-168">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b1fdf-168">2\_x</span></span> | <span data-ttu-id="b1fdf-169">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b1fdf-169">3\_0</span></span> | <span data-ttu-id="b1fdf-170">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b1fdf-170">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="b1fdf-171">Registro de tamaño de punto</span><span class="sxs-lookup"><span data-stu-id="b1fdf-171">Point Size Register</span></span>    | <span data-ttu-id="b1fdf-172">x</span><span class="sxs-lookup"><span data-stu-id="b1fdf-172">x</span></span>    | <span data-ttu-id="b1fdf-173">x</span><span class="sxs-lookup"><span data-stu-id="b1fdf-173">x</span></span>    | <span data-ttu-id="b1fdf-174">x</span><span class="sxs-lookup"><span data-stu-id="b1fdf-174">x</span></span>     | <span data-ttu-id="b1fdf-175">x</span><span class="sxs-lookup"><span data-stu-id="b1fdf-175">x</span></span>    |      |       |



 

## <a name="texture-coordinate-register---ot0-to-ot7"></a><span data-ttu-id="b1fdf-176">Coordenada de textura Register-oT0 a oT7</span><span class="sxs-lookup"><span data-stu-id="b1fdf-176">Texture Coordinate Register - oT0 to oT7</span></span>

<span data-ttu-id="b1fdf-177">La textura de salida coordina los registros.</span><span class="sxs-lookup"><span data-stu-id="b1fdf-177">The output texture coordinates registers.</span></span> <span data-ttu-id="b1fdf-178">En concreto, se trata de una matriz de registros de datos de salida que se iteran y usan como coordenadas de textura por las fases de muestreo de textura que enrutan los datos al sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="b1fdf-178">Specifically, these are an array of output data registers that are iterated and used as texture coordinates by the texture sampling stages routing data to the pixel shader.</span></span>



| <span data-ttu-id="b1fdf-179">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="b1fdf-179">Vertex shader versions</span></span>      | <span data-ttu-id="b1fdf-180">1\_1</span><span class="sxs-lookup"><span data-stu-id="b1fdf-180">1\_1</span></span> | <span data-ttu-id="b1fdf-181">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b1fdf-181">2\_0</span></span> | <span data-ttu-id="b1fdf-182">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b1fdf-182">2\_sw</span></span> | <span data-ttu-id="b1fdf-183">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b1fdf-183">2\_x</span></span> | <span data-ttu-id="b1fdf-184">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b1fdf-184">3\_0</span></span> | <span data-ttu-id="b1fdf-185">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b1fdf-185">3\_sw</span></span> |
|-----------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="b1fdf-186">Registro de coordenadas de textura</span><span class="sxs-lookup"><span data-stu-id="b1fdf-186">Texture Coordinate Register</span></span> | <span data-ttu-id="b1fdf-187">x</span><span class="sxs-lookup"><span data-stu-id="b1fdf-187">x</span></span>    | <span data-ttu-id="b1fdf-188">x</span><span class="sxs-lookup"><span data-stu-id="b1fdf-188">x</span></span>    | <span data-ttu-id="b1fdf-189">x</span><span class="sxs-lookup"><span data-stu-id="b1fdf-189">x</span></span>     | <span data-ttu-id="b1fdf-190">x</span><span class="sxs-lookup"><span data-stu-id="b1fdf-190">x</span></span>    |      |       |



 

<span data-ttu-id="b1fdf-191">Al escribir en un registro de coordenadas de textura, se recomienda pasar solo tantos valores de punto flotante como la dimensión del mapa de textura correspondiente.</span><span class="sxs-lookup"><span data-stu-id="b1fdf-191">When writing to a texture coordinate register, it is recommended to pass only as many floating point values as the dimension of the corresponding texture map.</span></span> <span data-ttu-id="b1fdf-192">Controlan los valores que se pasan con un modificador.</span><span class="sxs-lookup"><span data-stu-id="b1fdf-192">Control the values passed with a modifier.</span></span> <span data-ttu-id="b1fdf-193">Por ejemplo, use. XY para un mapa de textura 2D.</span><span class="sxs-lookup"><span data-stu-id="b1fdf-193">For example, use .xy for a 2D texture map.</span></span>

<span data-ttu-id="b1fdf-194">Cuando se habilita la proyección de textura para una fase de textura, los cuatro valores de punto flotante se deben escribir en el registro de textura correspondiente.</span><span class="sxs-lookup"><span data-stu-id="b1fdf-194">When texture projection is enabled for a texture stage, all four floating point values must be written to the corresponding texture register.</span></span>

<span data-ttu-id="b1fdf-195">Cualquiera de las marcas de D3DTTFF \* Texture Transform debe ser cero cuando se utiliza la canalización programable.</span><span class="sxs-lookup"><span data-stu-id="b1fdf-195">Any of the D3DTTFF\* texture transform flags should be zero when the programmable pipeline is being used.</span></span>

### <a name="texture-coordinate-range"></a><span data-ttu-id="b1fdf-196">Rango de coordenadas de textura</span><span class="sxs-lookup"><span data-stu-id="b1fdf-196">Texture Coordinate Range</span></span>

<span data-ttu-id="b1fdf-197">Los datos de vértices de objeto proporcionan coordenadas de textura de entrada.</span><span class="sxs-lookup"><span data-stu-id="b1fdf-197">Object vertex data supplies input texture coordinates.</span></span> <span data-ttu-id="b1fdf-198">Los objetos que no usan texturas en mosaico suelen tener coordenadas de textura en el intervalo de \[ 0 a 1 \] .</span><span class="sxs-lookup"><span data-stu-id="b1fdf-198">Objects that do not used tiled textures commonly have texture coordinates in the range \[0,1\].</span></span> <span data-ttu-id="b1fdf-199">Los objetos que usan texturas en mosaico, como Terrain, normalmente tienen coordenadas de textura que van desde \[ -?, +? \] Where?</span><span class="sxs-lookup"><span data-stu-id="b1fdf-199">Objects that use tiled textures, such as terrain, typically have texture coordinates that range from \[-?,+?\] where ?</span></span> <span data-ttu-id="b1fdf-200">puede ser un número de punto flotante de gran tamaño.</span><span class="sxs-lookup"><span data-stu-id="b1fdf-200">can be a large floating point number.</span></span>

<span data-ttu-id="b1fdf-201">La interpolación de coordenadas de textura se realiza en los datos de vértices para la rasterización.</span><span class="sxs-lookup"><span data-stu-id="b1fdf-201">Texture coordinate interpolation is performed on vertex data for rasterization.</span></span> <span data-ttu-id="b1fdf-202">Durante la rasterización, las coordenadas de textura se interpolan entre los vértices de objetos, modificados por ajuste de textura y escalado por el tamaño de textura (también con el modo de dirección de textura de la cuenta) para generar un índice de entero.</span><span class="sxs-lookup"><span data-stu-id="b1fdf-202">During rasterization, texture coordinates are interpolated between object vertices, modified by texture wrapping and scaled by the texture size (also taking into account texture address mode) to produce an integer index.</span></span> <span data-ttu-id="b1fdf-203">A continuación, el índice se utiliza para realizar una búsqueda de textura.</span><span class="sxs-lookup"><span data-stu-id="b1fdf-203">The index is then used to perform a texture lookup.</span></span> <span data-ttu-id="b1fdf-204">MaxTextureRepeat se puede usar para determinar el número de veces que se puede poner en mosaico una textura.</span><span class="sxs-lookup"><span data-stu-id="b1fdf-204">MaxTextureRepeat can be used to determine how many times a texture can be tiled.</span></span>

<span data-ttu-id="b1fdf-205">Si las coordenadas de textura se leen directamente en un sombreador de píxeles (mediante texcoord o texcrd), el intervalo de coordenadas de textura depende de la instrucción y la versión del sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="b1fdf-205">If texture coordinates are read directly into a pixel shader (using texcoord or texcrd), the texture coordinate range depends on the instruction and the pixel shader version.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b1fdf-206">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b1fdf-206">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1fdf-207">Registros del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="b1fdf-207">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




