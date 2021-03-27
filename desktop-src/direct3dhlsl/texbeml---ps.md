---
title: texbeml-PS
description: Aplicar una transformación de mapa de entorno de rugosidad falsa con corrección de luminancia. Esto se logra modificando los datos de la dirección de textura del registro de destino, utilizando los datos de la dirección Perturbation (du, DV), una matriz de entorno de rugosidad 2D y luminancia.
ms.assetid: 345a0b77-8d4e-4a0b-a31a-1153f8cb5961
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d97877c67970f43a995fcfbe21d9aead2d792e09
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995580"
---
# <a name="texbeml---ps"></a><span data-ttu-id="8c96d-104">texbeml-PS</span><span class="sxs-lookup"><span data-stu-id="8c96d-104">texbeml - ps</span></span>

<span data-ttu-id="8c96d-105">Aplicar una transformación de mapa de entorno de rugosidad falsa con corrección de luminancia.</span><span class="sxs-lookup"><span data-stu-id="8c96d-105">Apply a fake bump environment-map transform with luminance correction.</span></span> <span data-ttu-id="8c96d-106">Esto se logra modificando los datos de la dirección de textura del registro de destino, utilizando los datos de la dirección Perturbation (du, DV), una matriz de entorno de rugosidad 2D y luminancia.</span><span class="sxs-lookup"><span data-stu-id="8c96d-106">This is accomplished by modifying the texture address data of the destination register, using address perturbation data (du,dv), a 2D bump environment matrix, and luminance.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c96d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8c96d-107">Syntax</span></span>



| <span data-ttu-id="8c96d-108">texbeml DST, src</span><span class="sxs-lookup"><span data-stu-id="8c96d-108">texbeml dst, src</span></span> |
|------------------|



 

<span data-ttu-id="8c96d-109">, donde</span><span class="sxs-lookup"><span data-stu-id="8c96d-109">where</span></span>

-   <span data-ttu-id="8c96d-110">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="8c96d-110">dst is the destination register.</span></span>
-   <span data-ttu-id="8c96d-111">src es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="8c96d-111">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c96d-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8c96d-112">Remarks</span></span>



| <span data-ttu-id="8c96d-113">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="8c96d-113">Pixel shader versions</span></span> | <span data-ttu-id="8c96d-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="8c96d-114">1\_1</span></span> | <span data-ttu-id="8c96d-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="8c96d-115">1\_2</span></span> | <span data-ttu-id="8c96d-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="8c96d-116">1\_3</span></span> | <span data-ttu-id="8c96d-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="8c96d-117">1\_4</span></span> | <span data-ttu-id="8c96d-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8c96d-118">2\_0</span></span> | <span data-ttu-id="8c96d-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="8c96d-119">2\_x</span></span> | <span data-ttu-id="8c96d-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="8c96d-120">2\_sw</span></span> | <span data-ttu-id="8c96d-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8c96d-121">3\_0</span></span> | <span data-ttu-id="8c96d-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="8c96d-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="8c96d-123">texbeml</span><span class="sxs-lookup"><span data-stu-id="8c96d-123">texbeml</span></span>               | <span data-ttu-id="8c96d-124">x</span><span class="sxs-lookup"><span data-stu-id="8c96d-124">x</span></span>    | <span data-ttu-id="8c96d-125">x</span><span class="sxs-lookup"><span data-stu-id="8c96d-125">x</span></span>    | <span data-ttu-id="8c96d-126">x</span><span class="sxs-lookup"><span data-stu-id="8c96d-126">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="8c96d-127">Los datos de color rojo y verde del registro de src se interpretan como los datos de Perturbation (du, DV).</span><span class="sxs-lookup"><span data-stu-id="8c96d-127">The red and green color data in the src register is interpreted as the perturbation data (du,dv).</span></span> <span data-ttu-id="8c96d-128">Los datos de color azul del registro de src se interpretan como los datos de luminancia.</span><span class="sxs-lookup"><span data-stu-id="8c96d-128">The blue color data in the src register is interpreted as the luminance data.</span></span>

<span data-ttu-id="8c96d-129">Esta instrucción transforma los componentes rojo y verde del registro de origen mediante la matriz de asignación del entorno de rugosidad 2D.</span><span class="sxs-lookup"><span data-stu-id="8c96d-129">This instruction transforms the red and green components in the source register using the 2D bump environment mapping matrix.</span></span> <span data-ttu-id="8c96d-130">El resultado se agrega al conjunto de coordenadas de textura correspondiente al número de registro de destino.</span><span class="sxs-lookup"><span data-stu-id="8c96d-130">The result is added to the texture coordinate set corresponding to the destination register number.</span></span> <span data-ttu-id="8c96d-131">Una corrección de luminancia se aplica mediante el valor de luminancia y los valores de la fase de textura de sesgo.</span><span class="sxs-lookup"><span data-stu-id="8c96d-131">A luminance correction is applied using the luminance value and the bias texture stage values.</span></span> <span data-ttu-id="8c96d-132">El resultado se usa para muestrear la fase de textura actual.</span><span class="sxs-lookup"><span data-stu-id="8c96d-132">The result is used to sample the current texture stage.</span></span>

<span data-ttu-id="8c96d-133">Se puede usar para una variedad de técnicas basadas en la dirección Perturbation, como la asignación de entorno falsa por píxel.</span><span class="sxs-lookup"><span data-stu-id="8c96d-133">This can be used for a variety of techniques based on address perturbation such as fake per-pixel environment mapping.</span></span>

<span data-ttu-id="8c96d-134">Esta operación siempre interpreta du y DV como cantidades firmadas.</span><span class="sxs-lookup"><span data-stu-id="8c96d-134">This operation always interprets du and dv as signed quantities.</span></span> <span data-ttu-id="8c96d-135">En las versiones 1 \_ y 1 \_ 1, no se permite el modificador de entrada de [escala firmada del registro de origen](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) ( \_ BX2) en el argumento de entrada.</span><span class="sxs-lookup"><span data-stu-id="8c96d-135">For versions 1\_0 and 1\_1, the [Source Register Signed Scaling](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) input modifier (\_bx2) is not permitted on the input argument.</span></span>

<span data-ttu-id="8c96d-136">Esta instrucción genera resultados definidos cuando las texturas de entrada contienen datos de formato mixto.</span><span class="sxs-lookup"><span data-stu-id="8c96d-136">This instruction produces defined results when input textures contain mixed format data.</span></span> <span data-ttu-id="8c96d-137">Para obtener más información sobre los formatos de Surface, vea [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).</span><span class="sxs-lookup"><span data-stu-id="8c96d-137">For more information about surface formats, see [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).</span></span>


```
// When using this instruction, texture registers must follow 
//   the following sequence:
// The texture assigned to stage tn contains the (du,dv) data
// The texture assigned to stage t(m) is sampled
tex     t(n)                    
texbeml t(m),  t(n)      where m > n
```



<span data-ttu-id="8c96d-138">Este ejemplo muestra los cálculos realizados dentro de la instrucción.</span><span class="sxs-lookup"><span data-stu-id="8c96d-138">This example shows the calculations done within the instruction.</span></span>


```
// 1. New values for texture addresses (u',v') are calculated
// 2. Sample the texture using (u',v')
// 3. Luminance correction is applied
```



<span data-ttu-id="8c96d-139">u ' = TextureCoordinates (fase m)<sub>u</sub> +</span><span class="sxs-lookup"><span data-stu-id="8c96d-139">u' = TextureCoordinates(stage m)<sub>u</sub> +</span></span>

<span data-ttu-id="8c96d-140">D3DTSS \_ BUMPENVMAT00 (Stage m) \* t (n)<sub>R</sub> +</span><span class="sxs-lookup"><span data-stu-id="8c96d-140">D3DTSS\_BUMPENVMAT00(stage m)\*t(n)<sub>R</sub> +</span></span>

<span data-ttu-id="8c96d-141">D3DTSS \_ BUMPENVMAT10 (Stage m) \* t (n)<sub>G</sub></span><span class="sxs-lookup"><span data-stu-id="8c96d-141">D3DTSS\_BUMPENVMAT10(stage m)\*t(n)<sub>G</sub></span></span>

<span data-ttu-id="8c96d-142">v ' = TextureCoordinates (fase m)<sub>v</sub> +</span><span class="sxs-lookup"><span data-stu-id="8c96d-142">v' = TextureCoordinates(stage m)<sub>v</sub> +</span></span>

<span data-ttu-id="8c96d-143">D3DTSS \_ BUMPENVMAT01 (Stage m) \* t (n)<sub>R</sub> +</span><span class="sxs-lookup"><span data-stu-id="8c96d-143">D3DTSS\_BUMPENVMAT01(stage m)\*t(n)<sub>R</sub> +</span></span>

<span data-ttu-id="8c96d-144">D3DTSS \_ BUMPENVMAT11 (Stage m) \* t (n)<sub>G</sub></span><span class="sxs-lookup"><span data-stu-id="8c96d-144">D3DTSS\_BUMPENVMAT11(stage m)\*t(n)<sub>G</sub></span></span>

<span data-ttu-id="8c96d-145">t (m)<sub>RGBA</sub> = TextureSample (fase m) mediante (u ', v ') como coordenadas</span><span class="sxs-lookup"><span data-stu-id="8c96d-145">t(m)<sub>RGBA</sub> = TextureSample(stage m) using (u',v') as coordinates</span></span>

<span data-ttu-id="8c96d-146">t (m)<sub>RGBA</sub> = t (m)<sub>RGBA</sub>\*</span><span class="sxs-lookup"><span data-stu-id="8c96d-146">t(m)<sub>RGBA</sub> = t(m)<sub>RGBA</sub> \*</span></span>

<span data-ttu-id="8c96d-147">\[(t (n)<sub>B</sub> \* D3DTSS \_ BUMPENVLSCALE (fase m)) +</span><span class="sxs-lookup"><span data-stu-id="8c96d-147">\[(t(n)<sub>B</sub> \* D3DTSS\_BUMPENVLSCALE(stage m)) +</span></span>

<span data-ttu-id="8c96d-148">D3DTSS \_ BUMPENVLOFFSET (fase m)\]</span><span class="sxs-lookup"><span data-stu-id="8c96d-148">D3DTSS\_BUMPENVLOFFSET(stage m)\]</span></span>

<span data-ttu-id="8c96d-149">Los datos de registro que ha leído una instrucción [texbem](texbem---ps.md) o texbeml no se pueden leer más adelante, excepto por otro texbem o texbeml.</span><span class="sxs-lookup"><span data-stu-id="8c96d-149">Register data that has been read by a [texbem](texbem---ps.md) or texbeml instruction cannot be read later, except by another texbem or texbeml.</span></span>


```
// This example demonstrates the validation error caused by 
//   t0 being reread
ps_1_1
tex t0
texbem t1, t0
add r0, t1, t0

(Instruction Error) (Statement 4) Register data that has been read by 
texbem or texbeml instruction cannot be read by other instructions
```



## <a name="examples"></a><span data-ttu-id="8c96d-150">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8c96d-150">Examples</span></span>

<span data-ttu-id="8c96d-151">A continuación se muestra un sombreador de ejemplo con los mapas de textura identificados y las fases de textura identificadas.</span><span class="sxs-lookup"><span data-stu-id="8c96d-151">Here is an example shader with the texture maps identified and the texture stages identified.</span></span>


```
ps_1_1
tex t0              ; Define t0 to get a 2-tuple DuDv
texbeml t1, t0      ; Compute (u',v')
                    ; Apply luminance correction                    
                    ; Sample t1 using (u',v')
mov r0, t1          ; Output result
```



<span data-ttu-id="8c96d-152">Este ejemplo requiere las siguientes texturas en las siguientes fases de textura.</span><span class="sxs-lookup"><span data-stu-id="8c96d-152">This example requires the following textures in the following texture stages.</span></span>

-   <span data-ttu-id="8c96d-153">A la fase 0 se le asigna un mapa de rugosidad con datos Perturbation (du, DV).</span><span class="sxs-lookup"><span data-stu-id="8c96d-153">Stage 0 is assigned a bump map with (du, dv) perturbation data.</span></span>
-   <span data-ttu-id="8c96d-154">En la fase 1 se le asigna un mapa de textura con datos de color.</span><span class="sxs-lookup"><span data-stu-id="8c96d-154">Stage 1 is assigned a texture map with color data.</span></span>
-   <span data-ttu-id="8c96d-155">texbeml establece los datos de la matriz en la fase de textura que se muestrea.</span><span class="sxs-lookup"><span data-stu-id="8c96d-155">texbeml sets the matrix data on the texture stage that is sampled.</span></span> <span data-ttu-id="8c96d-156">Esto es diferente de la funcionalidad de la canalización de función fija en la que los datos de Perturbation y las matrices ocupan la misma fase de textura.</span><span class="sxs-lookup"><span data-stu-id="8c96d-156">This is different from the functionality of the fixed function pipeline where the perturbation data and the matrices occupy the same texture stage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8c96d-157">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8c96d-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c96d-158">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="8c96d-158">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 