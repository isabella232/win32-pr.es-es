---
title: texm3x2tex-PS
description: Realiza la última fila de una matriz 3x2 multiplica y usa el resultado para realizar una búsqueda de textura. texm3x2tex se debe usar junto con la instrucción texm3x2pad-PS.
ms.assetid: c6cfbf75-4a63-4c82-9fb6-286b51b7f883
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 62206bc4ef1e1b64ec760a240a087ec13526d896
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996913"
---
# <a name="texm3x2tex---ps"></a><span data-ttu-id="793f0-104">texm3x2tex-PS</span><span class="sxs-lookup"><span data-stu-id="793f0-104">texm3x2tex - ps</span></span>

<span data-ttu-id="793f0-105">Realiza la última fila de una matriz 3x2 multiplica y usa el resultado para realizar una búsqueda de textura.</span><span class="sxs-lookup"><span data-stu-id="793f0-105">Performs the final row of a 3x2 matrix multiply and uses the result to do a texture lookup.</span></span> <span data-ttu-id="793f0-106">texm3x2tex se debe usar junto con la instrucción [texm3x2pad-PS](texm3x2pad---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="793f0-106">texm3x2tex must be used in conjunction with the [texm3x2pad - ps](texm3x2pad---ps.md) instruction.</span></span>

## <a name="syntax"></a><span data-ttu-id="793f0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="793f0-107">Syntax</span></span>



| <span data-ttu-id="793f0-108">texm3x2tex DST, src</span><span class="sxs-lookup"><span data-stu-id="793f0-108">texm3x2tex dst, src</span></span> |
|---------------------|



 

<span data-ttu-id="793f0-109">, donde</span><span class="sxs-lookup"><span data-stu-id="793f0-109">where</span></span>

-   <span data-ttu-id="793f0-110">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="793f0-110">dst is the destination register.</span></span>
-   <span data-ttu-id="793f0-111">src es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="793f0-111">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="793f0-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="793f0-112">Remarks</span></span>



| <span data-ttu-id="793f0-113">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="793f0-113">Pixel shader versions</span></span> | <span data-ttu-id="793f0-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="793f0-114">1\_1</span></span> | <span data-ttu-id="793f0-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="793f0-115">1\_2</span></span> | <span data-ttu-id="793f0-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="793f0-116">1\_3</span></span> | <span data-ttu-id="793f0-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="793f0-117">1\_4</span></span> | <span data-ttu-id="793f0-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="793f0-118">2\_0</span></span> | <span data-ttu-id="793f0-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="793f0-119">2\_x</span></span> | <span data-ttu-id="793f0-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="793f0-120">2\_sw</span></span> | <span data-ttu-id="793f0-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="793f0-121">3\_0</span></span> | <span data-ttu-id="793f0-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="793f0-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="793f0-123">texm3x2tex</span><span class="sxs-lookup"><span data-stu-id="793f0-123">texm3x2tex</span></span>            | <span data-ttu-id="793f0-124">x</span><span class="sxs-lookup"><span data-stu-id="793f0-124">x</span></span>    | <span data-ttu-id="793f0-125">x</span><span class="sxs-lookup"><span data-stu-id="793f0-125">x</span></span>    | <span data-ttu-id="793f0-126">x</span><span class="sxs-lookup"><span data-stu-id="793f0-126">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="793f0-127">La instrucción se utiliza como una de las dos instrucciones que representan una operación de multiplicación de la matriz 3x2.</span><span class="sxs-lookup"><span data-stu-id="793f0-127">The instruction is used as one of two instructions representing a 3x2 matrix multiply operation.</span></span> <span data-ttu-id="793f0-128">Esta instrucción debe usarse con la instrucción [texm3x2pad-PS](texm3x2pad---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="793f0-128">This instruction must be used with the [texm3x2pad - ps](texm3x2pad---ps.md) instruction.</span></span>

<span data-ttu-id="793f0-129">Al utilizar estas dos instrucciones, los registros de textura deben usar la siguiente secuencia.</span><span class="sxs-lookup"><span data-stu-id="793f0-129">When using these two instructions, texture registers must use the following sequence.</span></span>


```
 
tex t(n)                      // Define tn as a standard 3-vector (tn must 
                              // be defined in some way before it is used)
texm3x2pad  t(m),   t(n)      // where m > n
                              // Perform first row of matrix multiply
texm3x2tex  t(m+1), t(n)      // Perform second row of matrix multiply 
                              // to get (u,v) to sample texture 
                              // associated with stage m+1
```



<span data-ttu-id="793f0-130">Aquí encontrará más detalles sobre cómo se realiza la multiplicación de 3x2.</span><span class="sxs-lookup"><span data-stu-id="793f0-130">Here is more detail about how the 3x2 multiply is accomplished.</span></span>

<span data-ttu-id="793f0-131">La instrucción texm3x2pad realiza la primera fila de Multiply para buscar u<sup>'</sup>.</span><span class="sxs-lookup"><span data-stu-id="793f0-131">The texm3x2pad instruction performs the first row of the multiply to find u<sup>'</sup>.</span></span>

<span data-ttu-id="793f0-132">u<sup>'</sup> = t (n)<sub>RGB</sub> \* TextureCoordinates (fase m)<sub>UVW</sub></span><span class="sxs-lookup"><span data-stu-id="793f0-132">u<sup>'</sup> = t(n)<sub>RGB</sub> \* TextureCoordinates(stage m)<sub>UVW</sub></span></span>

<span data-ttu-id="793f0-133">La instrucción texm3x2tex realiza la segunda fila de la multiplicación para encontrar v<sup>'</sup>.</span><span class="sxs-lookup"><span data-stu-id="793f0-133">The texm3x2tex instruction performs the second row of the multiply to find v<sup>'</sup>.</span></span>

<span data-ttu-id="793f0-134">v<sup>'</sup> = t (n)<sub>RGB</sub> \* TextureCoordinates (fase m + 1)<sub>UVW</sub></span><span class="sxs-lookup"><span data-stu-id="793f0-134">v<sup>'</sup> = t(n)<sub>RGB</sub> \* TextureCoordinates(stage m+1)<sub>UVW</sub></span></span>

<span data-ttu-id="793f0-135">La instrucción texm3x2tex muestrea la textura en la fase (m + 1) con (u<sup>'</sup>, v<sup>'</sup>) y almacena el resultado en t (m + 1).</span><span class="sxs-lookup"><span data-stu-id="793f0-135">The texm3x2tex instruction samples the texture on stage (m+1) with (u<sup>'</sup>,v<sup>'</sup>) and stores the result in t(m+1).</span></span>

<span data-ttu-id="793f0-136">t (m + 1)<sub>RGB</sub> = TextureSample (fase m + 1)<sub>RGB</sub> usando (u<sup>'</sup>, v<sup>'</sup> ) como coordenadas</span><span class="sxs-lookup"><span data-stu-id="793f0-136">t(m+1)<sub>RGB</sub> = TextureSample(stage m+1)<sub>RGB</sub> using (u<sup>'</sup>, v<sup>'</sup> ) as coordinates</span></span>

## <a name="examples"></a><span data-ttu-id="793f0-137">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="793f0-137">Examples</span></span>

<span data-ttu-id="793f0-138">A continuación se muestra un sombreador de ejemplo con los mapas de textura y las fases de textura identificadas.</span><span class="sxs-lookup"><span data-stu-id="793f0-138">Here is an example shader with the texture maps and the texture stages identified.</span></span>


```
ps_1_1
tex t0                // Bind texture in stage 0 to register t0
texm3x2pad  t1,  t0   // First row of matrix multiply
texm3x2tex  t2,  t0   // Second row of matrix multiply to get (u,v)
                      // with which to sample texture in stage 2
mov r0, t2            // Output result
```



<span data-ttu-id="793f0-139">Este ejemplo requiere las siguientes texturas en las siguientes fases de textura.</span><span class="sxs-lookup"><span data-stu-id="793f0-139">This example requires the following textures in the following texture stages.</span></span>

-   <span data-ttu-id="793f0-140">La fase 0 toma un mapa con los datos de Perturbation (x, y, z).</span><span class="sxs-lookup"><span data-stu-id="793f0-140">Stage 0 takes a map with (x,y,z) perturbation data.</span></span>
-   <span data-ttu-id="793f0-141">La fase 1 contiene coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="793f0-141">Stage 1 holds texture coordinates.</span></span> <span data-ttu-id="793f0-142">No se requiere textura en la fase de textura.</span><span class="sxs-lookup"><span data-stu-id="793f0-142">No texture is required in the texture stage.</span></span>
-   <span data-ttu-id="793f0-143">La fase 2 contiene las coordenadas de textura, así como un conjunto de textura 2D en esa fase de textura.</span><span class="sxs-lookup"><span data-stu-id="793f0-143">Stage 2 holds both texture coordinates as well as a 2D texture set at that texture stage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="793f0-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="793f0-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="793f0-145">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="793f0-145">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




