---
title: setp_comp-vs
description: Establezca el registro del predicado. | setp_comp-vs
ms.assetid: bfead3f8-f7fe-4fc1-939f-8e5fbc3e0adf
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 77d9e5f46e9fb8bbcfb96e56d13cd6f7cebfecc2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104424247"
---
# <a name="setp_comp---vs"></a><span data-ttu-id="07e84-104">\_COMP SETP-vs</span><span class="sxs-lookup"><span data-stu-id="07e84-104">setp\_comp - vs</span></span>

<span data-ttu-id="07e84-105">Establezca el registro del predicado.</span><span class="sxs-lookup"><span data-stu-id="07e84-105">Set the predicate register.</span></span>

## <a name="syntax"></a><span data-ttu-id="07e84-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="07e84-106">Syntax</span></span>



| <span data-ttu-id="07e84-107">SETP \_ COMP DST, src0, SRC1</span><span class="sxs-lookup"><span data-stu-id="07e84-107">setp\_comp dst, src0, src1</span></span> |
|----------------------------|



 

<span data-ttu-id="07e84-108">Donde:</span><span class="sxs-lookup"><span data-stu-id="07e84-108">Where:</span></span>

-   <span data-ttu-id="07e84-109">\_Comp es una comparación por canal entre los dos registros de origen.</span><span class="sxs-lookup"><span data-stu-id="07e84-109">\_comp is a per-channel comparison between the two source registers.</span></span> <span data-ttu-id="07e84-110">Puede tener uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="07e84-110">It can be one of the following:</span></span> 

    | <span data-ttu-id="07e84-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="07e84-111">Syntax</span></span> | <span data-ttu-id="07e84-112">De comparación</span><span class="sxs-lookup"><span data-stu-id="07e84-112">Comparison</span></span>            |
    |--------|-----------------------|
    | <span data-ttu-id="07e84-113">\_bruto</span><span class="sxs-lookup"><span data-stu-id="07e84-113">\_gt</span></span>   | <span data-ttu-id="07e84-114">Mayor que</span><span class="sxs-lookup"><span data-stu-id="07e84-114">Greater than</span></span>          |
    | <span data-ttu-id="07e84-115">\_plazo</span><span class="sxs-lookup"><span data-stu-id="07e84-115">\_lt</span></span>   | <span data-ttu-id="07e84-116">Menor que</span><span class="sxs-lookup"><span data-stu-id="07e84-116">Less than</span></span>             |
    | <span data-ttu-id="07e84-117">\_GE</span><span class="sxs-lookup"><span data-stu-id="07e84-117">\_ge</span></span>   | <span data-ttu-id="07e84-118">Mayor o igual que</span><span class="sxs-lookup"><span data-stu-id="07e84-118">Greater than or equal</span></span> |
    | <span data-ttu-id="07e84-119">\_cuarto</span><span class="sxs-lookup"><span data-stu-id="07e84-119">\_le</span></span>   | <span data-ttu-id="07e84-120">Menor o igual que</span><span class="sxs-lookup"><span data-stu-id="07e84-120">Less than or equal</span></span>    |
    | <span data-ttu-id="07e84-121">\_ajustes</span><span class="sxs-lookup"><span data-stu-id="07e84-121">\_eq</span></span>   | <span data-ttu-id="07e84-122">Igual a</span><span class="sxs-lookup"><span data-stu-id="07e84-122">Equal to</span></span>              |
    | <span data-ttu-id="07e84-123">\_&</span><span class="sxs-lookup"><span data-stu-id="07e84-123">\_ne</span></span>   | <span data-ttu-id="07e84-124">No es igual a</span><span class="sxs-lookup"><span data-stu-id="07e84-124">Not equal to</span></span>          |

    

     

-   <span data-ttu-id="07e84-125">DST es el registro de [predicado](dx9-graphics-reference-asm-vs-registers-predicate.md) Register, P0.</span><span class="sxs-lookup"><span data-stu-id="07e84-125">dst is the [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md) register, p0.</span></span>
-   <span data-ttu-id="07e84-126">src0 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="07e84-126">src0 is a source register.</span></span>
-   <span data-ttu-id="07e84-127">SRC1 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="07e84-127">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="07e84-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="07e84-128">Remarks</span></span>



| <span data-ttu-id="07e84-129">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="07e84-129">Vertex shader versions</span></span> | <span data-ttu-id="07e84-130">1\_1</span><span class="sxs-lookup"><span data-stu-id="07e84-130">1\_1</span></span> | <span data-ttu-id="07e84-131">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="07e84-131">2\_0</span></span> | <span data-ttu-id="07e84-132">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="07e84-132">2\_x</span></span> | <span data-ttu-id="07e84-133">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="07e84-133">2\_sw</span></span> | <span data-ttu-id="07e84-134">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="07e84-134">3\_0</span></span> | <span data-ttu-id="07e84-135">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="07e84-135">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="07e84-136">comp. SETP \_</span><span class="sxs-lookup"><span data-stu-id="07e84-136">setp\_comp</span></span>             |      |      | <span data-ttu-id="07e84-137">x</span><span class="sxs-lookup"><span data-stu-id="07e84-137">x</span></span>    | <span data-ttu-id="07e84-138">x</span><span class="sxs-lookup"><span data-stu-id="07e84-138">x</span></span>     | <span data-ttu-id="07e84-139">x</span><span class="sxs-lookup"><span data-stu-id="07e84-139">x</span></span>    | <span data-ttu-id="07e84-140">x</span><span class="sxs-lookup"><span data-stu-id="07e84-140">x</span></span>     |



 

<span data-ttu-id="07e84-141">Esta instrucción funciona como:</span><span class="sxs-lookup"><span data-stu-id="07e84-141">This instruction operates as:</span></span>


```
per channel in destination write mask
{
  dst.channel = src0.channel cmp src1.channel
}
```



<span data-ttu-id="07e84-142">Para cada canal que se puede escribir en función de la máscara de escritura de destino, guarde el resultado booleano de la operación de comparación entre los canales correspondientes de src0 y SRC1 (después de que se haya resuelto el modificador de origen swizzles).</span><span class="sxs-lookup"><span data-stu-id="07e84-142">For each channel that can be written according to the destination write mask, save the boolean result of the comparison operation between the corresponding channels of src0 and src1 (after the source modifier swizzles have been resolved).</span></span>

<span data-ttu-id="07e84-143">Los registros de origen permiten especificar swizzles de componentes arbitrarios.</span><span class="sxs-lookup"><span data-stu-id="07e84-143">Source registers allow arbitrary component swizzles to be specified.</span></span>

<span data-ttu-id="07e84-144">El registro de destino permite máscaras de escritura arbitrarias.</span><span class="sxs-lookup"><span data-stu-id="07e84-144">The destination register allows arbitrary write masks.</span></span>

<span data-ttu-id="07e84-145">El registro de destino debe ser el registro de predicado.</span><span class="sxs-lookup"><span data-stu-id="07e84-145">The dest register must be the predicate register.</span></span>

## <a name="applying-the-predicate-register"></a><span data-ttu-id="07e84-146">Aplicar el registro de predicado</span><span class="sxs-lookup"><span data-stu-id="07e84-146">Applying the Predicate Register</span></span>

<span data-ttu-id="07e84-147">Una vez que se ha inicializado el registro de predicado con SETP, se puede usar para controlar una instrucción por componente.</span><span class="sxs-lookup"><span data-stu-id="07e84-147">Once the predicate register has been initialized with setp, it can be used to control an instruction per component.</span></span> <span data-ttu-id="07e84-148">Esta es la sintaxis:</span><span class="sxs-lookup"><span data-stu-id="07e84-148">Here's the syntax:</span></span>


```
([!]p0[.swizzle]) instruction dest, srcReg, ...
```



<span data-ttu-id="07e84-149">Donde:</span><span class="sxs-lookup"><span data-stu-id="07e84-149">Where:</span></span>

-   <span data-ttu-id="07e84-150">\[!\] es un booleano opcional que no es</span><span class="sxs-lookup"><span data-stu-id="07e84-150">\[!\] is an optional boolean NOT</span></span>
-   <span data-ttu-id="07e84-151">P0 es el registro del predicado</span><span class="sxs-lookup"><span data-stu-id="07e84-151">p0 is the predicate register</span></span>
-   <span data-ttu-id="07e84-152">\[. swizzle \] es un swizzle opcional que se aplica al contenido del predicado Register antes de usarlo para enmascarar la instrucción.</span><span class="sxs-lookup"><span data-stu-id="07e84-152">\[.swizzle\] is an optional swizzle to apply to the contents of the predicate register before using it to mask the instruction.</span></span> <span data-ttu-id="07e84-153">Los swizzles disponibles son:. xyzw (valor predeterminado cuando no se especifica ninguno) o cualquier swizzle de replicación:. x/. r,. y/. g,. z/. b o. a/. w.</span><span class="sxs-lookup"><span data-stu-id="07e84-153">The available swizzles are: .xyzw (default when none specified), or any replicate swizzle: .x/.r, .y/.g, .z/.b or .a/.w.</span></span>
-   <span data-ttu-id="07e84-154">Instruction es cualquier Aritmetic o instrucción de textura.</span><span class="sxs-lookup"><span data-stu-id="07e84-154">instruction is any aritmetic, or texture instruction.</span></span> <span data-ttu-id="07e84-155">No puede ser una instrucción de control de flujo estático o dinámico.</span><span class="sxs-lookup"><span data-stu-id="07e84-155">This cannot be a static or dynamic flow control instruction.</span></span>
-   <span data-ttu-id="07e84-156">Dest, srcReg,... son los registros requeridos por la instrucción</span><span class="sxs-lookup"><span data-stu-id="07e84-156">dest, srcReg, ... are the registers required by the instruction</span></span>

<span data-ttu-id="07e84-157">Suponiendo que el registro de predicado se ha configurado con valores de componente (true, true, false, false), se puede aplicar a esta instrucción:</span><span class="sxs-lookup"><span data-stu-id="07e84-157">Assuming the predicate register has been set up with (true, true, false, false) component values, it can be applied to this instruction:</span></span>


```
// given r0 = 0,0,1,1
// given r1 = 1,1,0,0
setp_le p0, r0, r1
(p0) add r2, r3, r4
```



<span data-ttu-id="07e84-158">para realizar una adición de dos componentes.</span><span class="sxs-lookup"><span data-stu-id="07e84-158">to perform a 2 component add.</span></span>


```
r2.x = r3.x + r4.x
r2.y = r3.y + r4.y
```



<span data-ttu-id="07e84-159">Los componentes x e y de R2 no se escribirán, ya que el registro de predicado contenía false en los componentes z y w.</span><span class="sxs-lookup"><span data-stu-id="07e84-159">The x and y components of r2 will not be written since the predicate register contained false in components z and w.</span></span>

<span data-ttu-id="07e84-160">La aplicación del registro de predicado a una instrucción aritmética o de textura aumenta el número de ranuras de la instrucción en 1.</span><span class="sxs-lookup"><span data-stu-id="07e84-160">Applying the predicate register to an arithmetic or texture instruction increases its instruction slot count by 1.</span></span>

<span data-ttu-id="07e84-161">El registro de predicado también se puede aplicar a si se preparan las instrucciones [Pred-vs](if-pred---vs.md), [callnz Pred-vs](callnz-pred---vs.md) y [breakp-vs](breakp---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="07e84-161">The predicate register can also be applied to [if pred - vs](if-pred---vs.md), [callnz pred - vs](callnz-pred---vs.md) and [breakp - vs](breakp---vs.md) instructions.</span></span> <span data-ttu-id="07e84-162">Estas instrucciones de control de flujo no tienen ningún aumento en el recuento de ranuras de instrucciones cuando se usa el registro de predicado.</span><span class="sxs-lookup"><span data-stu-id="07e84-162">These flow control instructions do not have any increase in the instruction slot count when using the predicate register.</span></span>

## <a name="related-topics"></a><span data-ttu-id="07e84-163">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="07e84-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07e84-164">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="07e84-164">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




