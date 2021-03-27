---
title: texm3x3vspec-PS
description: Realiza una multiplicación de una matriz de 3x3 y utiliza el resultado para realizar una búsqueda de textura.
ms.assetid: 3798bc23-2929-48fe-93ae-5aa025823714
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 28f1ee1ddb0193f9ccdaa4976e4963e748091f37
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103994837"
---
# <a name="texm3x3vspec---ps"></a><span data-ttu-id="f550a-103">texm3x3vspec-PS</span><span class="sxs-lookup"><span data-stu-id="f550a-103">texm3x3vspec - ps</span></span>

<span data-ttu-id="f550a-104">Realiza una multiplicación de una matriz de 3x3 y utiliza el resultado para realizar una búsqueda de textura.</span><span class="sxs-lookup"><span data-stu-id="f550a-104">Performs a 3x3 matrix multiply and uses the result to perform a texture lookup.</span></span> <span data-ttu-id="f550a-105">Se puede usar para la reflexión especular y la asignación de entorno, donde el vector de rayo no es constante.</span><span class="sxs-lookup"><span data-stu-id="f550a-105">This can be used for specular reflection and environment mapping where the eye-ray vector is not constant.</span></span> <span data-ttu-id="f550a-106">texm3x3vspec debe usarse junto con dos instrucciones [de texm3x3pad-PS](texm3x3pad---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="f550a-106">texm3x3vspec must be used in conjunction with two [texm3x3pad - ps](texm3x3pad---ps.md) instructions.</span></span> <span data-ttu-id="f550a-107">Si el vector de rayo es constante, la instrucción [texm3x3spec-PS](texm3x3spec---ps.md) realizará la misma multiplicación de la matriz y la búsqueda de textura.</span><span class="sxs-lookup"><span data-stu-id="f550a-107">If the eye-ray vector is constant, the [texm3x3spec - ps](texm3x3spec---ps.md) instruction will perform the same matrix multiply and texture lookup.</span></span>

## <a name="syntax"></a><span data-ttu-id="f550a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f550a-108">Syntax</span></span>



| <span data-ttu-id="f550a-109">texm3x3vspec DST, src</span><span class="sxs-lookup"><span data-stu-id="f550a-109">texm3x3vspec dst, src</span></span> |
|-----------------------|



 

<span data-ttu-id="f550a-110">, donde</span><span class="sxs-lookup"><span data-stu-id="f550a-110">where</span></span>

-   <span data-ttu-id="f550a-111">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="f550a-111">dst is the destination register.</span></span>
-   <span data-ttu-id="f550a-112">src es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="f550a-112">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="f550a-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f550a-113">Remarks</span></span>



| <span data-ttu-id="f550a-114">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="f550a-114">Pixel shader versions</span></span> | <span data-ttu-id="f550a-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="f550a-115">1\_1</span></span> | <span data-ttu-id="f550a-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="f550a-116">1\_2</span></span> | <span data-ttu-id="f550a-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="f550a-117">1\_3</span></span> | <span data-ttu-id="f550a-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="f550a-118">1\_4</span></span> | <span data-ttu-id="f550a-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f550a-119">2\_0</span></span> | <span data-ttu-id="f550a-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="f550a-120">2\_x</span></span> | <span data-ttu-id="f550a-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f550a-121">2\_sw</span></span> | <span data-ttu-id="f550a-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f550a-122">3\_0</span></span> | <span data-ttu-id="f550a-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f550a-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="f550a-124">texm3x3vspec</span><span class="sxs-lookup"><span data-stu-id="f550a-124">texm3x3vspec</span></span>          | <span data-ttu-id="f550a-125">x</span><span class="sxs-lookup"><span data-stu-id="f550a-125">x</span></span>    | <span data-ttu-id="f550a-126">x</span><span class="sxs-lookup"><span data-stu-id="f550a-126">x</span></span>    | <span data-ttu-id="f550a-127">x</span><span class="sxs-lookup"><span data-stu-id="f550a-127">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="f550a-128">Esta instrucción realiza la fila final de una operación de multiplicación de una matriz de 3x3, interpreta el vector resultante como un vector normal para reflejar un vector de rayo y, a continuación, usa el vector reflejado como una dirección de textura para una búsqueda de textura.</span><span class="sxs-lookup"><span data-stu-id="f550a-128">This instruction performs the final row of a 3x3 matrix multiply operation, interprets the resulting vector as a normal vector to reflect an eye-ray vector, and then uses the reflected vector as a texture address for a texture lookup.</span></span> <span data-ttu-id="f550a-129">Funciona igual que [texm3x3spec-PS](texm3x3spec---ps.md), salvo que el vector de rayo se toma del cuarto componente de las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="f550a-129">It works just like [texm3x3spec - ps](texm3x3spec---ps.md), except that the eye-ray vector is taken from the fourth component of the texture coordinates.</span></span> <span data-ttu-id="f550a-130">La multiplicación de la matriz de 3x3 suele ser útil para orientar un vector normal al espacio de tangente correcto para la superficie que se representa.</span><span class="sxs-lookup"><span data-stu-id="f550a-130">The 3x3 matrix multiply is typically useful for orienting a normal vector to the correct tangent space for the surface being rendered.</span></span>

<span data-ttu-id="f550a-131">La matriz de 3x3 se compone de las coordenadas de textura de la tercera fase de textura y las dos fases de textura anteriores.</span><span class="sxs-lookup"><span data-stu-id="f550a-131">The 3x3 matrix is comprised of the texture coordinates of the third texture stage and the two preceding texture stages.</span></span> <span data-ttu-id="f550a-132">El vector de reflexión posterior resultante (UVW) se usa para realizar el muestreo de la textura en la fase 3.</span><span class="sxs-lookup"><span data-stu-id="f550a-132">The resulting post-reflection vector (UVW) is used to sample the texture in stage 3.</span></span> <span data-ttu-id="f550a-133">Se omite cualquier textura asignada a las dos fases de textura anteriores.</span><span class="sxs-lookup"><span data-stu-id="f550a-133">Any texture assigned to the preceding two texture stages is ignored.</span></span>

<span data-ttu-id="f550a-134">Esta instrucción debe usarse con la instrucción texm3x3pad.</span><span class="sxs-lookup"><span data-stu-id="f550a-134">This instruction must be used with the texm3x3pad instruction.</span></span> <span data-ttu-id="f550a-135">Los registros de texturas deben usar la siguiente secuencia.</span><span class="sxs-lookup"><span data-stu-id="f550a-135">Texture registers must use the following sequence.</span></span>


```
tex t(n)                    // Define tn as a standard 3-vector (tn must
                            //   be defined in some way before it is used)
texm3x3pad   t(m),   t(n)   // where m > n
                            // Perform first row of matrix multiply
texm3x3pad   t(m+1), t(n)   // Perform second row of matrix multiply
texm3x3vspec t(m+2), t(n)   // Perform third row of matrix multiply
                            // Then do a texture lookup on the texture
                            // associated with texture stage m+2
```



<span data-ttu-id="f550a-136">La primera instrucción texm3x3pad realiza la primera fila de Multiply para buscar u<sup>'</sup>.</span><span class="sxs-lookup"><span data-stu-id="f550a-136">The first texm3x3pad instruction performs the first row of the multiply to find u<sup>'</sup>.</span></span>

<span data-ttu-id="f550a-137">u<sup>'</sup> = TextureCoordinates (Stage m)<sub>UVW</sub> \* t (n) <sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="f550a-137">u<sup>'</sup> = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n) <sub>RGB</sub></span></span>

<span data-ttu-id="f550a-138">La segunda instrucción texm3x3pad realiza la segunda fila de la multiplicación para encontrar v<sup>'</sup>.</span><span class="sxs-lookup"><span data-stu-id="f550a-138">The second texm3x3pad instruction performs the second row of the multiply to find v<sup>'</sup>.</span></span>

<span data-ttu-id="f550a-139">v<sup>'</sup> = TextureCoordinates (Stage m + 1)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="f550a-139">v<sup>'</sup> = TextureCoordinates(stage m+1)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="f550a-140">La instrucción texm3x3spec realiza la tercera fila de Multiply para buscar w<sup>'</sup>.</span><span class="sxs-lookup"><span data-stu-id="f550a-140">The texm3x3spec instruction performs the third row of the multiply to find w<sup>'</sup>.</span></span>

<span data-ttu-id="f550a-141">w<sup>'</sup> = TextureCoordinates (fase m + 2)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="f550a-141">w<sup>'</sup> = TextureCoordinates(stage m+2)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="f550a-142">La instrucción texm3x3vspec también realiza un cálculo de reflexión.</span><span class="sxs-lookup"><span data-stu-id="f550a-142">The texm3x3vspec instruction also does a reflection calculation.</span></span>

<span data-ttu-id="f550a-143">(u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) = 2 \* \[ (n \* E)/(n \* n) \] \* N-E</span><span class="sxs-lookup"><span data-stu-id="f550a-143">(u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) = 2\*\[(N\*E)/(N\*N)\]\*N - E</span></span>

<span data-ttu-id="f550a-144">donde se proporciona la N normal.</span><span class="sxs-lookup"><span data-stu-id="f550a-144">// where the normal N is given by</span></span>

<span data-ttu-id="f550a-145">N = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> )</span><span class="sxs-lookup"><span data-stu-id="f550a-145">// N = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> )</span></span>

<span data-ttu-id="f550a-146">y el vector E de Ray</span><span class="sxs-lookup"><span data-stu-id="f550a-146">// and the eye-ray vector E is given by</span></span>

<span data-ttu-id="f550a-147">E = (TextureCoordinates (fase m)<sub>Q</sub> ,</span><span class="sxs-lookup"><span data-stu-id="f550a-147">// E = (TextureCoordinates(stage m)<sub>Q</sub> ,</span></span>

<span data-ttu-id="f550a-148">TextureCoordinates (fase m + 1)<sub>Q</sub> ,</span><span class="sxs-lookup"><span data-stu-id="f550a-148">// TextureCoordinates(stage m+1)<sub>Q</sub> ,</span></span>

<span data-ttu-id="f550a-149">TextureCoordinates (fase m + 2)<sub>Q</sub> )</span><span class="sxs-lookup"><span data-stu-id="f550a-149">// TextureCoordinates(stage m+2)<sub>Q</sub> )</span></span>

<span data-ttu-id="f550a-150">Por último, la instrucción texm3x3vspec muestrea t (m + 2) con (u<sup>'</sup>, v<sup>'</sup>, w<sup>'</sup>) y almacena el resultado en t (m + 2).</span><span class="sxs-lookup"><span data-stu-id="f550a-150">Lastly, the texm3x3vspec instruction samples t(m+2) with (u<sup>'</sup>,v<sup>'</sup>,w<sup>'</sup>)and stores the result in t(m+2).</span></span>

<span data-ttu-id="f550a-151">t (m + 2)<sub>RGBA</sub> = TextureSample (fase m + 2)<sub>RGBA</sub> mediante (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) como coordenadas</span><span class="sxs-lookup"><span data-stu-id="f550a-151">t(m+2)<sub>RGBA</sub> = TextureSample(stage m+2)<sub>RGBA</sub> using (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) as coordinates</span></span>

## <a name="examples"></a><span data-ttu-id="f550a-152">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f550a-152">Examples</span></span>

<span data-ttu-id="f550a-153">A continuación se muestra un sombreador de ejemplo con los mapas de textura identificados y las fases de textura identificadas.</span><span class="sxs-lookup"><span data-stu-id="f550a-153">Here is an example shader with the texture maps identified and the texture stages identified.</span></span>


```
ps_1_1
tex t0                // Bind texture in stage 0 to register t0
texm3x3pad   t1,  t0  // First row of matrix multiply
texm3x3pad   t2,  t0  // Second row of matrix multiply
texm3x3vspec t3,  t0  // Third row of matrix multiply to get a 3-vector
                      // Reflect 3-vector by the eye-ray vector
                      // Use reflected vector to do a texture lookup
                      //   at stage 3
mov r0, t3            // Output the result
```



<span data-ttu-id="f550a-154">Este ejemplo requiere la siguiente configuración de la fase de textura.</span><span class="sxs-lookup"><span data-stu-id="f550a-154">This example requires the following texture stage setup.</span></span>

-   <span data-ttu-id="f550a-155">A la fase 0 se le asigna un mapa de textura con datos normales.</span><span class="sxs-lookup"><span data-stu-id="f550a-155">Stage 0 is assigned a texture map with normal data.</span></span> <span data-ttu-id="f550a-156">Esto se conoce a menudo como un mapa de rugosidad.</span><span class="sxs-lookup"><span data-stu-id="f550a-156">This is often referred to as a bump map.</span></span> <span data-ttu-id="f550a-157">Los datos son normales (XYZ) para cada textura.</span><span class="sxs-lookup"><span data-stu-id="f550a-157">The data is (XYZ) normals for each texel.</span></span> <span data-ttu-id="f550a-158">Las coordenadas de textura de la fase n definen cómo se muestra este mapa normal.</span><span class="sxs-lookup"><span data-stu-id="f550a-158">Texture coordinates at stage n defines how to sample this normal map.</span></span>
-   <span data-ttu-id="f550a-159">El conjunto de coordenadas de textura m se asigna a la fila 1 de la matriz de 3x3.</span><span class="sxs-lookup"><span data-stu-id="f550a-159">Texture coordinate set m is assigned to row 1 of the 3x3 matrix.</span></span> <span data-ttu-id="f550a-160">Se omite cualquier textura asignada a la fase m.</span><span class="sxs-lookup"><span data-stu-id="f550a-160">Any texture assigned to stage m is ignored.</span></span>
-   <span data-ttu-id="f550a-161">El conjunto de coordenadas de textura m + 1 se asigna a la fila 2 de la matriz de 3x3.</span><span class="sxs-lookup"><span data-stu-id="f550a-161">Texture coordinate set m+1 is assigned to row 2 of the 3x3 matrix.</span></span> <span data-ttu-id="f550a-162">Se omite cualquier textura asignada a la fase m + 1.</span><span class="sxs-lookup"><span data-stu-id="f550a-162">Any texture assigned to stage m+1 is ignored.</span></span>
-   <span data-ttu-id="f550a-163">El conjunto de coordenadas de textura m + 2 se asigna a la fila 3 de la matriz de 3x3.</span><span class="sxs-lookup"><span data-stu-id="f550a-163">Texture coordinate set m+2 is assigned to row 3 of the 3x3 matrix.</span></span> <span data-ttu-id="f550a-164">A la fase m + 2 se le asigna un volumen o un mapa de textura del cubo.</span><span class="sxs-lookup"><span data-stu-id="f550a-164">Stage m+2 is assigned a volume or cube texture map.</span></span> <span data-ttu-id="f550a-165">La textura proporciona datos de color (RGBA).</span><span class="sxs-lookup"><span data-stu-id="f550a-165">The texture provides color data (RGBA).</span></span>
-   <span data-ttu-id="f550a-166">El vector E de rayo se pasa a la instrucción del cuarto componente (q) de los datos de coordenadas de textura en las fases m, m + 1 y m + 2.</span><span class="sxs-lookup"><span data-stu-id="f550a-166">The eye-ray vector E is passed into the instruction in the fourth component (q) of the texture coordinate data at stages m, m+1, and m+2.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f550a-167">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f550a-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f550a-168">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="f550a-168">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




