---
title: texm3x3spec-PS
description: Realiza una multiplicación de una matriz de 3x3 y utiliza el resultado para realizar una búsqueda de textura. Se puede usar para la reflexión especular y la asignación de entorno. texm3x3spec debe usarse junto con dos instrucciones de texm3x3pad-PS.
ms.assetid: 74269bcf-de1d-48b4-a4d0-aa08fd54b8e6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d872a5f9ebf716142fb5bc506edb77bb0b66850a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419915"
---
# <a name="texm3x3spec---ps"></a><span data-ttu-id="d9cb2-105">texm3x3spec-PS</span><span class="sxs-lookup"><span data-stu-id="d9cb2-105">texm3x3spec - ps</span></span>

<span data-ttu-id="d9cb2-106">Realiza una multiplicación de una matriz de 3x3 y utiliza el resultado para realizar una búsqueda de textura.</span><span class="sxs-lookup"><span data-stu-id="d9cb2-106">Performs a 3x3 matrix multiply and uses the result to perform a texture lookup.</span></span> <span data-ttu-id="d9cb2-107">Se puede usar para la reflexión especular y la asignación de entorno.</span><span class="sxs-lookup"><span data-stu-id="d9cb2-107">This can be used for specular reflection and environment mapping.</span></span> <span data-ttu-id="d9cb2-108">texm3x3spec debe usarse junto con dos instrucciones [de texm3x3pad-PS](texm3x3pad---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="d9cb2-108">texm3x3spec must be used in conjunction with two [texm3x3pad - ps](texm3x3pad---ps.md) instructions.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9cb2-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d9cb2-109">Syntax</span></span>



| <span data-ttu-id="d9cb2-110">texm3x3spec DST, src0, SRC1</span><span class="sxs-lookup"><span data-stu-id="d9cb2-110">texm3x3spec dst, src0, src1</span></span> |
|-----------------------------|



 

<span data-ttu-id="d9cb2-111">, donde</span><span class="sxs-lookup"><span data-stu-id="d9cb2-111">where</span></span>

-   <span data-ttu-id="d9cb2-112">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="d9cb2-112">dst is the destination register.</span></span>
-   <span data-ttu-id="d9cb2-113">src0 y SRC1 son registros de origen.</span><span class="sxs-lookup"><span data-stu-id="d9cb2-113">src0 and src1 are source registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9cb2-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d9cb2-114">Remarks</span></span>



| <span data-ttu-id="d9cb2-115">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="d9cb2-115">Pixel shader versions</span></span> | <span data-ttu-id="d9cb2-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="d9cb2-116">1\_1</span></span> | <span data-ttu-id="d9cb2-117">1\_2</span><span class="sxs-lookup"><span data-stu-id="d9cb2-117">1\_2</span></span> | <span data-ttu-id="d9cb2-118">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="d9cb2-118">1\_3</span></span> | <span data-ttu-id="d9cb2-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="d9cb2-119">1\_4</span></span> | <span data-ttu-id="d9cb2-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d9cb2-120">2\_0</span></span> | <span data-ttu-id="d9cb2-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="d9cb2-121">2\_x</span></span> | <span data-ttu-id="d9cb2-122">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="d9cb2-122">2\_sw</span></span> | <span data-ttu-id="d9cb2-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d9cb2-123">3\_0</span></span> | <span data-ttu-id="d9cb2-124">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="d9cb2-124">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="d9cb2-125">texm3x3spec</span><span class="sxs-lookup"><span data-stu-id="d9cb2-125">texm3x3spec</span></span>           | <span data-ttu-id="d9cb2-126">x</span><span class="sxs-lookup"><span data-stu-id="d9cb2-126">x</span></span>    | <span data-ttu-id="d9cb2-127">x</span><span class="sxs-lookup"><span data-stu-id="d9cb2-127">x</span></span>    | <span data-ttu-id="d9cb2-128">x</span><span class="sxs-lookup"><span data-stu-id="d9cb2-128">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="d9cb2-129">Esta instrucción realiza una multiplicación de la fila final de una matriz de 3x3, usa el vector resultante como vector normal para reflejar un vector de rayo y, a continuación, usa el vector reflejado para realizar una búsqueda de textura.</span><span class="sxs-lookup"><span data-stu-id="d9cb2-129">This instruction performs the final row of a 3x3 matrix multiply, uses the resulting vector as a normal vector to reflect an eye-ray vector, and then uses the reflected vector to perform a texture lookup.</span></span> <span data-ttu-id="d9cb2-130">El sombreador lee el vector de rayo de un registro constante.</span><span class="sxs-lookup"><span data-stu-id="d9cb2-130">The shader reads the eye-ray vector from a constant register.</span></span> <span data-ttu-id="d9cb2-131">La multiplicación de la matriz de 3x3 suele ser útil para orientar un vector normal al espacio de tangente correcto para la superficie que se representa.</span><span class="sxs-lookup"><span data-stu-id="d9cb2-131">The 3x3 matrix multiply is typically useful for orienting a normal vector to the correct tangent space for the surface being rendered.</span></span>

<span data-ttu-id="d9cb2-132">La matriz de 3x3 se compone de las coordenadas de textura de la tercera fase de textura y las dos fases de textura anteriores.</span><span class="sxs-lookup"><span data-stu-id="d9cb2-132">The 3x3 matrix is comprised of the texture coordinates of the third texture stage and the two preceding texture stages.</span></span> <span data-ttu-id="d9cb2-133">El vector de reflexión post resultante (u, v, w) se usa para mostrar la textura en la fase de textura final.</span><span class="sxs-lookup"><span data-stu-id="d9cb2-133">The resulting post reflection vector (u,v,w) is used to sample the texture on the final texture stage.</span></span> <span data-ttu-id="d9cb2-134">Se omite cualquier textura asignada a las dos fases de textura anteriores.</span><span class="sxs-lookup"><span data-stu-id="d9cb2-134">Any texture assigned to the preceding two texture stages is ignored.</span></span>

<span data-ttu-id="d9cb2-135">Esta instrucción debe usarse con dos instrucciones texm3x3pad.</span><span class="sxs-lookup"><span data-stu-id="d9cb2-135">This instruction must be used with two texm3x3pad instructions.</span></span> <span data-ttu-id="d9cb2-136">Los registros de texturas deben usar la siguiente secuencia.</span><span class="sxs-lookup"><span data-stu-id="d9cb2-136">Texture registers must use the following sequence.</span></span>


```
 
tex t(n)                      // Define tn as a standard 3-vector (tn must
                              //   be defined in some way before it is used)
texm3x3pad t(m),   t(n)       //   where m > n
                              // Perform first row of matrix multiply
texm3x3pad  t(m+1), t(n)      // Perform second row of matrix multiply
texm3x3spec t(m+2), t(n), c0  // Perform third row of matrix multiply
                              // Then do a texture lookup on the texture
                              //   associated with texture stage m+2
```



<span data-ttu-id="d9cb2-137">La primera instrucción texm3x3pad realiza la primera fila de Multiply para buscar u<sup>'</sup>.</span><span class="sxs-lookup"><span data-stu-id="d9cb2-137">The first texm3x3pad instruction performs the first row of the multiply to find u<sup>'</sup>.</span></span>

<span data-ttu-id="d9cb2-138">u<sup>'</sup> = TextureCoordinates (Stage m)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="d9cb2-138">u<sup>'</sup> = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="d9cb2-139">La segunda instrucción texm3x3pad realiza la segunda fila de la multiplicación para encontrar v<sup>'</sup>.</span><span class="sxs-lookup"><span data-stu-id="d9cb2-139">The second texm3x3pad instruction performs the second row of the multiply to find v<sup>'</sup>.</span></span>

<span data-ttu-id="d9cb2-140">v<sup>'</sup> = TextureCoordinates (Stage m + 1)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="d9cb2-140">v<sup>'</sup> = TextureCoordinates(stage m+1)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="d9cb2-141">La instrucción texm3x3spec realiza la tercera fila de Multiply para buscar w<sup>'</sup>.</span><span class="sxs-lookup"><span data-stu-id="d9cb2-141">The texm3x3spec instruction performs the third row of the multiply to find w<sup>'</sup>.</span></span>

<span data-ttu-id="d9cb2-142">w<sup>'</sup> = TextureCoordinates (fase m + 2)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="d9cb2-142">w<sup>'</sup> = TextureCoordinates(stage m+2)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="d9cb2-143">A continuación, la instrucción texm3x3spec realiza un cálculo de reflexión.</span><span class="sxs-lookup"><span data-stu-id="d9cb2-143">The texm3x3spec instruction then does a reflection calculation.</span></span>

<span data-ttu-id="d9cb2-144">(u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) = 2 \* \[ (n \* E)/(n \* n) \] \* N-E</span><span class="sxs-lookup"><span data-stu-id="d9cb2-144">(u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) = 2\*\[(N\*E)/(N\*N)\]\*N - E</span></span>

<span data-ttu-id="d9cb2-145">donde se proporciona la N normal.</span><span class="sxs-lookup"><span data-stu-id="d9cb2-145">// where the normal N is given by</span></span>

<span data-ttu-id="d9cb2-146">N = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> )</span><span class="sxs-lookup"><span data-stu-id="d9cb2-146">// N = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> )</span></span>

<span data-ttu-id="d9cb2-147">Además, el vector de rayo se proporciona mediante el registro de constantes</span><span class="sxs-lookup"><span data-stu-id="d9cb2-147">// and the eye-ray vector E is given by the constant register</span></span>

<span data-ttu-id="d9cb2-148">E = c \# (se puede usar cualquier registro constante--C0, C1, C2, etc.)</span><span class="sxs-lookup"><span data-stu-id="d9cb2-148">// E = c\# (Any constant register--c0, c1, c2, etc.--can be used)</span></span>

<span data-ttu-id="d9cb2-149">Por último, la instrucción texm3x3spec muestrea t (m + 2) con (u<sup>'</sup>, v<sup>'</sup>, w<sup>'</sup>) y almacena el resultado en t (m + 2).</span><span class="sxs-lookup"><span data-stu-id="d9cb2-149">Lastly, the texm3x3spec instruction samples t(m+2) with (u<sup>'</sup>,v<sup>'</sup>,w<sup>'</sup>) and stores the result in t(m+2).</span></span>

<span data-ttu-id="d9cb2-150">t (m + 2)<sub>RGBA</sub> = TextureSample (fase m + 2)<sub>RGBA</sub> mediante (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) como coordenadas</span><span class="sxs-lookup"><span data-stu-id="d9cb2-150">t(m+2)<sub>RGBA</sub> = TextureSample(stage m+2)<sub>RGBA</sub> using (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) as coordinates</span></span>

## <a name="examples"></a><span data-ttu-id="d9cb2-151">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d9cb2-151">Examples</span></span>

<span data-ttu-id="d9cb2-152">A continuación se muestra un sombreador de ejemplo con los mapas de textura y las fases de textura identificadas.</span><span class="sxs-lookup"><span data-stu-id="d9cb2-152">Here is an example shader with the texture maps and the texture stages identified.</span></span>


```
ps_1_1
tex t0                    // Bind texture in stage 0 to register t0 (tn must
                          //   be defined in some way before it is used)
texm3x3pad  t1,  t0       // First row of matrix multiply
texm3x3pad  t2,  t0       // Second row of matrix multiply
texm3x3spec t3,  t0,  c#  // Third row of matrix multiply to get a 3-vector
                          // Reflect 3-vector by the eye-ray vector in c#  
                          // Use reflected vector to lookup texture in
                          //   stage 3
mov r0, t3                // Output the result
```



<span data-ttu-id="d9cb2-153">Este ejemplo requiere la siguiente configuración de la fase de textura.</span><span class="sxs-lookup"><span data-stu-id="d9cb2-153">This example requires the following texture stage setup.</span></span>

-   <span data-ttu-id="d9cb2-154">A la fase 0 se le asigna un mapa de textura con datos normales.</span><span class="sxs-lookup"><span data-stu-id="d9cb2-154">Stage 0 is assigned a texture map with normal data.</span></span> <span data-ttu-id="d9cb2-155">Esto se conoce a menudo como un mapa de rugosidad.</span><span class="sxs-lookup"><span data-stu-id="d9cb2-155">This is often referred to as a bump map.</span></span> <span data-ttu-id="d9cb2-156">Los datos son normales (XYZ) para cada textura.</span><span class="sxs-lookup"><span data-stu-id="d9cb2-156">The data is (XYZ) normals for each texel.</span></span> <span data-ttu-id="d9cb2-157">Las coordenadas de textura en la fase n define dónde se debe muestrear este mapa normal.</span><span class="sxs-lookup"><span data-stu-id="d9cb2-157">Texture coordinates at stage n defines where to sample this normal map.</span></span>
-   <span data-ttu-id="d9cb2-158">El conjunto de coordenadas de textura m se asigna a la fila 1 de la matriz de 3x3.</span><span class="sxs-lookup"><span data-stu-id="d9cb2-158">Texture coordinate set m is assigned to row 1 of the 3x3 matrix.</span></span> <span data-ttu-id="d9cb2-159">Se omite cualquier textura asignada a la fase m.</span><span class="sxs-lookup"><span data-stu-id="d9cb2-159">Any texture assigned to stage m is ignored.</span></span>
-   <span data-ttu-id="d9cb2-160">El conjunto de coordenadas de textura m + 1 se asigna a la fila 2 de la matriz de 3x3.</span><span class="sxs-lookup"><span data-stu-id="d9cb2-160">Texture coordinate set m+1 is assigned to row 2 of the 3x3 matrix.</span></span> <span data-ttu-id="d9cb2-161">Se omite cualquier textura asignada a la fase m + 1.</span><span class="sxs-lookup"><span data-stu-id="d9cb2-161">Any texture assigned to stage m+1 is ignored.</span></span>
-   <span data-ttu-id="d9cb2-162">El conjunto de coordenadas de textura m + 2 se asigna a la fila 3 de la matriz de 3x3.</span><span class="sxs-lookup"><span data-stu-id="d9cb2-162">Texture coordinate set m+2 is assigned to row 3 of the 3x3 matrix.</span></span> <span data-ttu-id="d9cb2-163">A la fase m + 2 se le asigna un volumen o un mapa de textura del cubo.</span><span class="sxs-lookup"><span data-stu-id="d9cb2-163">Stage m+2 is assigned a volume or cube texture map.</span></span> <span data-ttu-id="d9cb2-164">La textura proporciona datos de color (RGBA).</span><span class="sxs-lookup"><span data-stu-id="d9cb2-164">The texture provides color data (RGBA).</span></span>
-   <span data-ttu-id="d9cb2-165">El vector E de rayo se proporciona mediante un registro constante E = c \# .</span><span class="sxs-lookup"><span data-stu-id="d9cb2-165">The eye-ray vector E is given by a constant register E = c\#.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d9cb2-166">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d9cb2-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9cb2-167">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="d9cb2-167">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




