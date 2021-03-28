---
title: texbem-PS
description: Aplicar una transformación de mapa de entorno de rugosidad falsa. Para ello, se modifican los datos de la dirección de textura del registro de destino, utilizando los datos de dirección Perturbation (du, DV) y una matriz de entorno de rugosidad 2D.
ms.assetid: 8e773f4a-c7a2-4caf-973f-8f50dccc9c04
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f026819b268836fd7d4c1d550033ceefdf0bbbf9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104984007"
---
# <a name="texbem---ps"></a><span data-ttu-id="948e5-104">texbem-PS</span><span class="sxs-lookup"><span data-stu-id="948e5-104">texbem - ps</span></span>

<span data-ttu-id="948e5-105">Aplicar una transformación de mapa de entorno de rugosidad falsa.</span><span class="sxs-lookup"><span data-stu-id="948e5-105">Apply a fake bump environment-map transform.</span></span> <span data-ttu-id="948e5-106">Para ello, se modifican los datos de la dirección de textura del registro de destino, utilizando los datos de dirección Perturbation (du, DV) y una matriz de entorno de rugosidad 2D.</span><span class="sxs-lookup"><span data-stu-id="948e5-106">This is accomplished by modifying the texture address data of the destination register, using address perturbation data (du,dv), and a 2D bump environment matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="948e5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="948e5-107">Syntax</span></span>



| <span data-ttu-id="948e5-108">texbem DST, src</span><span class="sxs-lookup"><span data-stu-id="948e5-108">texbem dst, src</span></span> |
|-----------------|



 

<span data-ttu-id="948e5-109">, donde</span><span class="sxs-lookup"><span data-stu-id="948e5-109">where</span></span>

-   <span data-ttu-id="948e5-110">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="948e5-110">dst is the destination register.</span></span>
-   <span data-ttu-id="948e5-111">src es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="948e5-111">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="948e5-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="948e5-112">Remarks</span></span>



| <span data-ttu-id="948e5-113">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="948e5-113">Pixel shader versions</span></span> | <span data-ttu-id="948e5-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="948e5-114">1\_1</span></span> | <span data-ttu-id="948e5-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="948e5-115">1\_2</span></span> | <span data-ttu-id="948e5-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="948e5-116">1\_3</span></span> | <span data-ttu-id="948e5-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="948e5-117">1\_4</span></span> | <span data-ttu-id="948e5-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="948e5-118">2\_0</span></span> | <span data-ttu-id="948e5-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="948e5-119">2\_x</span></span> | <span data-ttu-id="948e5-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="948e5-120">2\_sw</span></span> | <span data-ttu-id="948e5-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="948e5-121">3\_0</span></span> | <span data-ttu-id="948e5-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="948e5-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="948e5-123">texbem</span><span class="sxs-lookup"><span data-stu-id="948e5-123">texbem</span></span>                | <span data-ttu-id="948e5-124">x</span><span class="sxs-lookup"><span data-stu-id="948e5-124">x</span></span>    | <span data-ttu-id="948e5-125">x</span><span class="sxs-lookup"><span data-stu-id="948e5-125">x</span></span>    | <span data-ttu-id="948e5-126">x</span><span class="sxs-lookup"><span data-stu-id="948e5-126">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="948e5-127">Los datos de color rojo y verde del registro de src se interpretan como los datos de Perturbation (du, DV).</span><span class="sxs-lookup"><span data-stu-id="948e5-127">The red and green color data in the src register is interpreted as the perturbation data (du,dv).</span></span>

<span data-ttu-id="948e5-128">Esta instrucción transforma los componentes rojo y verde en el registro de origen mediante la matriz de asignación del entorno de rugosidad 2D.</span><span class="sxs-lookup"><span data-stu-id="948e5-128">This instruction transforms red and green components in the source register using the 2D bump environment-mapping matrix.</span></span> <span data-ttu-id="948e5-129">El resultado se agrega al conjunto de coordenadas de textura correspondiente al número de registro de destino y se usa para muestrear la fase de textura actual.</span><span class="sxs-lookup"><span data-stu-id="948e5-129">The result is added to the texture coordinate set corresponding to the destination register number, and is used to sample the current texture stage.</span></span>

<span data-ttu-id="948e5-130">Esta operación siempre interpreta du y DV como cantidades firmadas.</span><span class="sxs-lookup"><span data-stu-id="948e5-130">This operation always interprets du and dv as signed quantities.</span></span> <span data-ttu-id="948e5-131">En las versiones 1 \_ y 1 \_ 1, no se permite el modificador de entrada de [escala firmada del registro de origen](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) ( \_ BX2) en el argumento de entrada.</span><span class="sxs-lookup"><span data-stu-id="948e5-131">For versions 1\_0 and 1\_1, the [Source Register Signed Scaling](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) input modifier (\_bx2) is not permitted on the input argument.</span></span>

<span data-ttu-id="948e5-132">Esta instrucción genera resultados definidos cuando las texturas de entrada contienen datos de formato firmados.</span><span class="sxs-lookup"><span data-stu-id="948e5-132">This instruction produces defined results when input textures contain signed format data.</span></span> <span data-ttu-id="948e5-133">Los datos con formato mixto solo funcionan si los dos primeros canales contienen datos firmados.</span><span class="sxs-lookup"><span data-stu-id="948e5-133">Mixed format data works only if the first two channels contain signed data.</span></span> <span data-ttu-id="948e5-134">Para obtener más información sobre los formatos de Surface, vea [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).</span><span class="sxs-lookup"><span data-stu-id="948e5-134">For more information about surface formats, see [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).</span></span>

<span data-ttu-id="948e5-135">Se puede usar para una variedad de técnicas basadas en la dirección Perturbation, incluida la asignación de entorno falsa por píxel y la iluminación difusa (asignación de rugosidad).</span><span class="sxs-lookup"><span data-stu-id="948e5-135">This can be used for a variety of techniques based on address perturbation, including fake per-pixel environment mapping and diffuse lighting (bump mapping).</span></span>

<span data-ttu-id="948e5-136">Al utilizar esta instrucción, los registros de textura deben seguir la secuencia siguiente.</span><span class="sxs-lookup"><span data-stu-id="948e5-136">When using this instruction, texture registers must follow the following sequence.</span></span>


```
// The texture assigned to stage t(n) contains the (du,dv) data
// The texture assigned to stage t(m) is sampled
tex     t(n)                    
texbem  t(m),  t(n)      where m > n
```



<span data-ttu-id="948e5-137">Los cálculos realizados dentro de la instrucción se muestran a continuación.</span><span class="sxs-lookup"><span data-stu-id="948e5-137">The calculations done within the instruction are shown below.</span></span>


```
// 1. New values for texture addresses (u',v') are calculated
// 2. Sample the texture using (u',v')
```



<span data-ttu-id="948e5-138">u ' = TextureCoordinates (Stage m)<sub>u</sub> + D3DTSS \_ BUMPENVMAT00 (Stage m) \* t (n)<sub>R</sub> + D3DTSS \_ BUMPENVMAT10 (Stage m) \* t (n)<sub>G</sub> v ' = TextureCoordinates (Stage m)<sub>v</sub> + D3DTSS \_ BUMPENVMAT01 (Stage m) \* t (n)<sub>R</sub> + D3DTSS \_ BUMPENVMAT11 (Stage m) \* t (n)<sub>G</sub> t (m)<sub>RGBA</sub> = TextureSample (fase m)</span><span class="sxs-lookup"><span data-stu-id="948e5-138">u' = TextureCoordinates(stage m)<sub>u</sub> + D3DTSS\_BUMPENVMAT00(stage m)\*t(n)<sub>R</sub> + D3DTSS\_BUMPENVMAT10(stage m)\*t(n)<sub>G</sub> v' = TextureCoordinates(stage m)<sub>v</sub> + D3DTSS\_BUMPENVMAT01(stage m)\*t(n)<sub>R</sub> + D3DTSS\_BUMPENVMAT11(stage m)\*t(n)<sub>G</sub> t(m)<sub>RGBA</sub> = TextureSample(stage m)</span></span>

<span data-ttu-id="948e5-139">usar (u ', v ') como coordenadas</span><span class="sxs-lookup"><span data-stu-id="948e5-139">// using (u',v') as coordinates</span></span>

<span data-ttu-id="948e5-140">Los datos de registro que ha leído una instrucción texbem-PS o [texbeml-PS](texbeml---ps.md) no se pueden leer más adelante, excepto en otro texbem-PS o texbeml-PS.</span><span class="sxs-lookup"><span data-stu-id="948e5-140">Register data that has been read by a texbem - ps or [texbeml - ps](texbeml---ps.md) instruction cannot be read later, except by another texbem - ps or texbeml - ps.</span></span>


```
// This example demonstrates the validation error caused by t0 being reread:
ps_1_1
tex t0
texbem t1, t0
add r0, t1, t0

(Instruction Error) (Statement 4) Register data that has been read by 
texbem or texbeml instruction cannot be read by other instructions
```



## <a name="examples"></a><span data-ttu-id="948e5-141">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="948e5-141">Examples</span></span>

<span data-ttu-id="948e5-142">A continuación se muestra un sombreador de ejemplo con los mapas de textura identificados y las fases de textura identificadas.</span><span class="sxs-lookup"><span data-stu-id="948e5-142">Here is an example shader with the texture maps identified and the texture stages identified.</span></span>


```
ps_1_1
tex t0              ; Define t0 to get a 2-tuple DuDv
texbem t1, t0       ; Compute (u',v')
                    ; Sample t1 using (u',v')
mov r0, t1          ; Output result
```



<span data-ttu-id="948e5-143">texbem requiere las siguientes texturas en las siguientes fases de textura.</span><span class="sxs-lookup"><span data-stu-id="948e5-143">texbem requires the following textures in the following texture stages.</span></span>

-   <span data-ttu-id="948e5-144">A la fase 0 se le asigna un mapa de rugosidad con datos Perturbation (du, DV).</span><span class="sxs-lookup"><span data-stu-id="948e5-144">Stage 0 is assigned a bump map with (du, dv) perturbation data.</span></span>
-   <span data-ttu-id="948e5-145">En la fase 1 se usa un mapa de textura con datos de color.</span><span class="sxs-lookup"><span data-stu-id="948e5-145">Stage 1 uses a texture map with color data.</span></span>
-   <span data-ttu-id="948e5-146">Esta instrucción establece los datos de la matriz en la fase de textura que se muestrea.</span><span class="sxs-lookup"><span data-stu-id="948e5-146">This instruction sets the matrix data on the texture stage that is sampled.</span></span>
-   <span data-ttu-id="948e5-147">Esto es diferente de la funcionalidad de la canalización de función fija en la que los datos de Perturbation y las matrices ocupan la misma fase de textura.</span><span class="sxs-lookup"><span data-stu-id="948e5-147">This is different from the functionality of the fixed function pipeline where the perturbation data and the matrices occupy the same texture stage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="948e5-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="948e5-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="948e5-149">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="948e5-149">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 