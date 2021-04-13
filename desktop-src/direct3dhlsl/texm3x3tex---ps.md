---
title: texm3x3tex-PS
description: Realiza una multiplicación de una matriz de 3x3 y usa el resultado para realizar una búsqueda de textura. texm3x3tex debe usarse con dos instrucciones de texm3x3pad-PS.
ms.assetid: bb61cd6f-57d0-4b2d-9186-f04f7f4d3516
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a228b61dbed22dc8d285e0fdc833de53b16e7be7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104420003"
---
# <a name="texm3x3tex---ps"></a><span data-ttu-id="63a4a-104">texm3x3tex-PS</span><span class="sxs-lookup"><span data-stu-id="63a4a-104">texm3x3tex - ps</span></span>

<span data-ttu-id="63a4a-105">Realiza una multiplicación de una matriz de 3x3 y usa el resultado para realizar una búsqueda de textura.</span><span class="sxs-lookup"><span data-stu-id="63a4a-105">Performs a 3x3 matrix multiply and uses the result to do a texture lookup.</span></span> <span data-ttu-id="63a4a-106">texm3x3tex debe usarse con dos instrucciones [de texm3x3pad-PS](texm3x3pad---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="63a4a-106">texm3x3tex must be used with two [texm3x3pad - ps](texm3x3pad---ps.md) instructions.</span></span>

## <a name="syntax"></a><span data-ttu-id="63a4a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="63a4a-107">Syntax</span></span>



| <span data-ttu-id="63a4a-108">texm3x3tex DST, src</span><span class="sxs-lookup"><span data-stu-id="63a4a-108">texm3x3tex dst, src</span></span> |
|---------------------|



 

<span data-ttu-id="63a4a-109">, donde</span><span class="sxs-lookup"><span data-stu-id="63a4a-109">where</span></span>

-   <span data-ttu-id="63a4a-110">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="63a4a-110">dst is the destination register.</span></span>
-   <span data-ttu-id="63a4a-111">src es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="63a4a-111">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="63a4a-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="63a4a-112">Remarks</span></span>



| <span data-ttu-id="63a4a-113">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="63a4a-113">Pixel shader versions</span></span> | <span data-ttu-id="63a4a-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="63a4a-114">1\_1</span></span> | <span data-ttu-id="63a4a-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="63a4a-115">1\_2</span></span> | <span data-ttu-id="63a4a-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="63a4a-116">1\_3</span></span> | <span data-ttu-id="63a4a-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="63a4a-117">1\_4</span></span> | <span data-ttu-id="63a4a-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="63a4a-118">2\_0</span></span> | <span data-ttu-id="63a4a-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="63a4a-119">2\_x</span></span> | <span data-ttu-id="63a4a-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="63a4a-120">2\_sw</span></span> | <span data-ttu-id="63a4a-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="63a4a-121">3\_0</span></span> | <span data-ttu-id="63a4a-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="63a4a-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="63a4a-123">texm3x3tex</span><span class="sxs-lookup"><span data-stu-id="63a4a-123">texm3x3tex</span></span>            | <span data-ttu-id="63a4a-124">x</span><span class="sxs-lookup"><span data-stu-id="63a4a-124">x</span></span>    | <span data-ttu-id="63a4a-125">x</span><span class="sxs-lookup"><span data-stu-id="63a4a-125">x</span></span>    | <span data-ttu-id="63a4a-126">x</span><span class="sxs-lookup"><span data-stu-id="63a4a-126">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="63a4a-127">Esta instrucción se utiliza como final de tres instrucciones que representan una operación de multiplicación de la matriz de 3x3, seguida de una búsqueda de textura.</span><span class="sxs-lookup"><span data-stu-id="63a4a-127">This instruction is used as the final of three instructions representing a 3x3 matrix multiply operation, followed by a texture lookup.</span></span> <span data-ttu-id="63a4a-128">La matriz de 3x3 se compone de las coordenadas de textura de la tercera fase de textura y las dos fases de textura anteriores.</span><span class="sxs-lookup"><span data-stu-id="63a4a-128">The 3x3 matrix is comprised of the texture coordinates of the third texture stage and the two preceding texture stages.</span></span> <span data-ttu-id="63a4a-129">El vector de tres componentes resultante (u, v, w) se usa para mostrar la textura en la fase 3.</span><span class="sxs-lookup"><span data-stu-id="63a4a-129">The resulting three-component vector (u,v,w) is used to sample the texture in stage 3.</span></span> <span data-ttu-id="63a4a-130">Se omite cualquier textura asignada a las dos fases de textura anteriores.</span><span class="sxs-lookup"><span data-stu-id="63a4a-130">Any texture assigned to the preceding two texture stages is ignored.</span></span> <span data-ttu-id="63a4a-131">La multiplicación de la matriz de 3x3 suele ser útil para orientar un vector normal al espacio de tangente correcto para la superficie que se representa.</span><span class="sxs-lookup"><span data-stu-id="63a4a-131">The 3x3 matrix multiply is typically useful for orienting a normal vector to the correct tangent space for the surface being rendered.</span></span>

<span data-ttu-id="63a4a-132">Esta instrucción debe usarse con la instrucción texm3x3pad.</span><span class="sxs-lookup"><span data-stu-id="63a4a-132">This instruction must be used with the texm3x3pad instruction.</span></span> <span data-ttu-id="63a4a-133">Los registros de texturas deben usar la siguiente secuencia.</span><span class="sxs-lookup"><span data-stu-id="63a4a-133">Texture registers must use the following sequence.</span></span>


```
 
tex t(n)                 // Define tn as a standard 3-vector (tn must
                         //   be defined in some way before it is used)
texm3x3pad t(m),   t(n)  //   where m > n
                         // Perform first row of matrix multiply
texm3x3pad t(m+1), t(n)  // Perform second row of matrix multiply
texm3x3tex t(m+2), t(n)  // Perform third row of matrix multiply to get a
                         //   3-vector with which to sample texture
                         //   associated with texture stage m+2
```



<span data-ttu-id="63a4a-134">Aquí encontrará más detalles sobre cómo se realiza la multiplicación de 3x3.</span><span class="sxs-lookup"><span data-stu-id="63a4a-134">Here is more detail about how the 3x3 multiply is accomplished.</span></span>

<span data-ttu-id="63a4a-135">La primera instrucción texm3x3pad realiza la primera fila de Multiply para buscar u<sup>'</sup>.</span><span class="sxs-lookup"><span data-stu-id="63a4a-135">The first texm3x3pad instruction performs the first row of the multiply to find u<sup>'</sup>.</span></span>

<span data-ttu-id="63a4a-136">u<sup>'</sup> = TextureCoordinates (Stage m)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="63a4a-136">u<sup>'</sup> = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="63a4a-137">La segunda instrucción texm3x3pad realiza la segunda fila de la multiplicación para encontrar v<sup>'</sup>.</span><span class="sxs-lookup"><span data-stu-id="63a4a-137">The second texm3x3pad instruction performs the second row of the multiply to find v<sup>'</sup>.</span></span>

<span data-ttu-id="63a4a-138">v<sup>'</sup> = TextureCoordinates (Stage m + 1)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="63a4a-138">v<sup>'</sup> = TextureCoordinates(stage m+1)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="63a4a-139">La instrucción texm3x3spec realiza la tercera fila de Multiply para buscar w<sup>'</sup>.</span><span class="sxs-lookup"><span data-stu-id="63a4a-139">The texm3x3spec instruction performs the third row of the multiply to find w<sup>'</sup>.</span></span>

<span data-ttu-id="63a4a-140">w<sup>'</sup> = TextureCoordinates (fase m + 2)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="63a4a-140">w<sup>'</sup> = TextureCoordinates(stage m+2)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="63a4a-141">Por último, la instrucción texm3x3tex muestrea t (m + 2) con (u<sup>'</sup>, v<sup>'</sup>, w<sup>'</sup>) y almacena el resultado en t (m + 2).</span><span class="sxs-lookup"><span data-stu-id="63a4a-141">Lastly, the texm3x3tex instruction samples t(m+2) with (u<sup>'</sup>,v<sup>'</sup>,w<sup>'</sup>) and stores the result in t(m+2).</span></span>

<span data-ttu-id="63a4a-142">t (m + 2)<sub>RGBA</sub> = TextureSample (fase m + 2)<sub>RGBA</sub> usando (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) como coordenadas.</span><span class="sxs-lookup"><span data-stu-id="63a4a-142">t(m+2)<sub>RGBA</sub> = TextureSample(stage m+2)<sub>RGBA</sub> using (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) as coordinates.</span></span>

## <a name="examples"></a><span data-ttu-id="63a4a-143">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="63a4a-143">Examples</span></span>

<span data-ttu-id="63a4a-144">A continuación se muestra un sombreador de ejemplo con los mapas de textura identificados y las fases de textura identificadas.</span><span class="sxs-lookup"><span data-stu-id="63a4a-144">Here is an example shader with the texture maps identified and the texture stages identified.</span></span>


```
ps_1_1
tex t0                // Bind texture in stage 0 to register t0
texm3x3pad  t1,  t0   // First row of matrix multiply
texm3x3pad  t2,  t0   // Second row of matrix multiply
texm3x3tex  t3,  t0   // Third row of matrix multiply to get a
                      // 3-vector with which to sample texture at 
mov r0, t3            // stage 3 output result
```



<span data-ttu-id="63a4a-145">Este ejemplo requiere la siguiente configuración de la fase de textura.</span><span class="sxs-lookup"><span data-stu-id="63a4a-145">This example requires the following texture stage setup.</span></span>

-   <span data-ttu-id="63a4a-146">A la fase 0 se le asigna un mapa de textura con datos normales.</span><span class="sxs-lookup"><span data-stu-id="63a4a-146">Stage 0 is assigned a texture map with normal data.</span></span> <span data-ttu-id="63a4a-147">Esto se conoce a menudo como un mapa de rugosidad.</span><span class="sxs-lookup"><span data-stu-id="63a4a-147">This is often referred to as a bump map.</span></span> <span data-ttu-id="63a4a-148">Los datos son normales (XYZ) para cada textura.</span><span class="sxs-lookup"><span data-stu-id="63a4a-148">The data is (XYZ) normals for each texel.</span></span> <span data-ttu-id="63a4a-149">El conjunto de coordenadas de textura 0 define cómo se muestra este mapa normal.</span><span class="sxs-lookup"><span data-stu-id="63a4a-149">Texture coordinate set 0 defines how to sample this normal map.</span></span>
-   <span data-ttu-id="63a4a-150">El conjunto de coordenadas de textura 1 se asigna a la fila 1 de la matriz de 3x3.</span><span class="sxs-lookup"><span data-stu-id="63a4a-150">Texture coordinate set 1 is assigned to row 1 of the 3x3 matrix.</span></span> <span data-ttu-id="63a4a-151">Se omite cualquier textura asignada a la fase 1.</span><span class="sxs-lookup"><span data-stu-id="63a4a-151">Any texture assigned to stage 1 is ignored.</span></span>
-   <span data-ttu-id="63a4a-152">El conjunto de coordenadas de textura 2 se asigna a la fila 2 de la matriz de 3x3.</span><span class="sxs-lookup"><span data-stu-id="63a4a-152">Texture coordinate set 2 is assigned to row 2 of the 3x3 matrix.</span></span> <span data-ttu-id="63a4a-153">Se omite cualquier textura asignada a la fase 2.</span><span class="sxs-lookup"><span data-stu-id="63a4a-153">Any texture assigned to stage 2 is ignored.</span></span>
-   <span data-ttu-id="63a4a-154">El conjunto de coordenadas de textura 3 se asigna a la fila 3 de la matriz de 3x3.</span><span class="sxs-lookup"><span data-stu-id="63a4a-154">Texture coordinate set 3 is assigned to row 3 of the 3x3 matrix.</span></span> <span data-ttu-id="63a4a-155">Un volumen o textura de cubo debe establecerse en la fase 3 para que lo busque el vector 3D transformado.</span><span class="sxs-lookup"><span data-stu-id="63a4a-155">A volume or cube texture should be set to stage 3 for lookup by the transformed 3D vector.</span></span>

## <a name="related-topics"></a><span data-ttu-id="63a4a-156">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="63a4a-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63a4a-157">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="63a4a-157">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




