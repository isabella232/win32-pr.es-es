---
title: setp_comp-PS
description: Establezca el registro del predicado. | setp_comp-PS
ms.assetid: a9acb685-f9aa-41f1-8ef1-6d104cb76a09
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a68da290ecb04e9cb7ae49c5525997fbf4c112a3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104280128"
---
# <a name="setp_comp---ps"></a><span data-ttu-id="7ab64-104">SETP \_ COMP-PS</span><span class="sxs-lookup"><span data-stu-id="7ab64-104">setp\_comp - ps</span></span>

<span data-ttu-id="7ab64-105">Establezca el registro del predicado.</span><span class="sxs-lookup"><span data-stu-id="7ab64-105">Set the predicate register.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ab64-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7ab64-106">Syntax</span></span>



| <span data-ttu-id="7ab64-107">SETP \_ COMP DST, src0, SRC1</span><span class="sxs-lookup"><span data-stu-id="7ab64-107">setp\_comp dst, src0, src1</span></span> |
|----------------------------|



 

<span data-ttu-id="7ab64-108">Donde:</span><span class="sxs-lookup"><span data-stu-id="7ab64-108">Where:</span></span>

-   <span data-ttu-id="7ab64-109">\_Comp es una comparación por canal entre los dos registros de origen.</span><span class="sxs-lookup"><span data-stu-id="7ab64-109">\_comp is a per-channel comparison between the two source registers.</span></span> <span data-ttu-id="7ab64-110">Puede tener uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="7ab64-110">It can be one of the following:</span></span> 

    | <span data-ttu-id="7ab64-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7ab64-111">Syntax</span></span> | <span data-ttu-id="7ab64-112">De comparación</span><span class="sxs-lookup"><span data-stu-id="7ab64-112">Comparison</span></span>            |
    |--------|-----------------------|
    | <span data-ttu-id="7ab64-113">\_bruto</span><span class="sxs-lookup"><span data-stu-id="7ab64-113">\_gt</span></span>   | <span data-ttu-id="7ab64-114">Mayor que</span><span class="sxs-lookup"><span data-stu-id="7ab64-114">Greater than</span></span>          |
    | <span data-ttu-id="7ab64-115">\_plazo</span><span class="sxs-lookup"><span data-stu-id="7ab64-115">\_lt</span></span>   | <span data-ttu-id="7ab64-116">Menor que</span><span class="sxs-lookup"><span data-stu-id="7ab64-116">Less than</span></span>             |
    | <span data-ttu-id="7ab64-117">\_GE</span><span class="sxs-lookup"><span data-stu-id="7ab64-117">\_ge</span></span>   | <span data-ttu-id="7ab64-118">Mayor o igual que</span><span class="sxs-lookup"><span data-stu-id="7ab64-118">Greater than or equal</span></span> |
    | <span data-ttu-id="7ab64-119">\_cuarto</span><span class="sxs-lookup"><span data-stu-id="7ab64-119">\_le</span></span>   | <span data-ttu-id="7ab64-120">Menor o igual que</span><span class="sxs-lookup"><span data-stu-id="7ab64-120">Less than or equal</span></span>    |
    | <span data-ttu-id="7ab64-121">\_ajustes</span><span class="sxs-lookup"><span data-stu-id="7ab64-121">\_eq</span></span>   | <span data-ttu-id="7ab64-122">Igual a</span><span class="sxs-lookup"><span data-stu-id="7ab64-122">Equal to</span></span>              |
    | <span data-ttu-id="7ab64-123">\_&</span><span class="sxs-lookup"><span data-stu-id="7ab64-123">\_ne</span></span>   | <span data-ttu-id="7ab64-124">No es igual a</span><span class="sxs-lookup"><span data-stu-id="7ab64-124">Not equal to</span></span>          |

    

     

-   <span data-ttu-id="7ab64-125">DST es el registro de [predicado](dx9-graphics-reference-asm-ps-registers-predicate.md) Register, P0.</span><span class="sxs-lookup"><span data-stu-id="7ab64-125">dst is the [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md) register, p0.</span></span>
-   <span data-ttu-id="7ab64-126">src0 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="7ab64-126">src0 is a source register.</span></span>
-   <span data-ttu-id="7ab64-127">SRC1 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="7ab64-127">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ab64-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7ab64-128">Remarks</span></span>



| <span data-ttu-id="7ab64-129">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="7ab64-129">Pixel shader versions</span></span> | <span data-ttu-id="7ab64-130">1\_1</span><span class="sxs-lookup"><span data-stu-id="7ab64-130">1\_1</span></span> | <span data-ttu-id="7ab64-131">1\_2</span><span class="sxs-lookup"><span data-stu-id="7ab64-131">1\_2</span></span> | <span data-ttu-id="7ab64-132">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="7ab64-132">1\_3</span></span> | <span data-ttu-id="7ab64-133">1\_4</span><span class="sxs-lookup"><span data-stu-id="7ab64-133">1\_4</span></span> | <span data-ttu-id="7ab64-134">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7ab64-134">2\_0</span></span> | <span data-ttu-id="7ab64-135">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="7ab64-135">2\_x</span></span> | <span data-ttu-id="7ab64-136">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7ab64-136">2\_sw</span></span> | <span data-ttu-id="7ab64-137">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7ab64-137">3\_0</span></span> | <span data-ttu-id="7ab64-138">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7ab64-138">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="7ab64-139">comp. SETP \_</span><span class="sxs-lookup"><span data-stu-id="7ab64-139">setp\_comp</span></span>            |      |      |      |      |      | <span data-ttu-id="7ab64-140">x</span><span class="sxs-lookup"><span data-stu-id="7ab64-140">x</span></span>    | <span data-ttu-id="7ab64-141">x</span><span class="sxs-lookup"><span data-stu-id="7ab64-141">x</span></span>     | <span data-ttu-id="7ab64-142">x</span><span class="sxs-lookup"><span data-stu-id="7ab64-142">x</span></span>    | <span data-ttu-id="7ab64-143">x</span><span class="sxs-lookup"><span data-stu-id="7ab64-143">x</span></span>     |



 

<span data-ttu-id="7ab64-144">Esta instrucción funciona como:</span><span class="sxs-lookup"><span data-stu-id="7ab64-144">This instruction operates as:</span></span>


```
per channel in destination write mask
{
  dst.channel = src0.channel cmp src1.channel
}
```



<span data-ttu-id="7ab64-145">Para cada canal que se puede escribir en función de la máscara de escritura de destino, guarde el resultado booleano de la operación de comparación entre los canales correspondientes de src0 y SRC1 (después de que se haya resuelto el modificador de origen swizzles).</span><span class="sxs-lookup"><span data-stu-id="7ab64-145">For each channel that can be written according to the destination write mask, save the boolean result of the comparison operation between the corresponding channels of src0 and src1 (after the source modifier swizzles have been resolved).</span></span>

<span data-ttu-id="7ab64-146">Los registros de origen permiten especificar swizzles de componentes arbitrarios.</span><span class="sxs-lookup"><span data-stu-id="7ab64-146">Source registers allow arbitrary component swizzles to be specified.</span></span>

<span data-ttu-id="7ab64-147">El registro de destino permite máscaras de escritura arbitrarias.</span><span class="sxs-lookup"><span data-stu-id="7ab64-147">The destination register allows arbitrary write masks.</span></span>

<span data-ttu-id="7ab64-148">El registro de DST debe ser el registro del predicado.</span><span class="sxs-lookup"><span data-stu-id="7ab64-148">The dst register must be the predicate register.</span></span>

## <a name="applying-the-predicate-register"></a><span data-ttu-id="7ab64-149">Aplicar el registro de predicado</span><span class="sxs-lookup"><span data-stu-id="7ab64-149">Applying the Predicate Register</span></span>

<span data-ttu-id="7ab64-150">Una vez que se ha inicializado el registro de predicado con SETP \_ COMP, se puede usar para controlar una instrucción por componente.</span><span class="sxs-lookup"><span data-stu-id="7ab64-150">Once the predicate register has been initialized with setp\_comp, it can be used to control an instruction per component.</span></span> <span data-ttu-id="7ab64-151">Esta es la sintaxis:</span><span class="sxs-lookup"><span data-stu-id="7ab64-151">Here's the syntax:</span></span>


```
([!]p0[.swizzle]) instruction dest, src0, ...
```



<span data-ttu-id="7ab64-152">Donde:</span><span class="sxs-lookup"><span data-stu-id="7ab64-152">Where:</span></span>

-   <span data-ttu-id="7ab64-153">\[!\] es un booleano opcional que no es</span><span class="sxs-lookup"><span data-stu-id="7ab64-153">\[!\] is an optional boolean NOT</span></span>
-   <span data-ttu-id="7ab64-154">P0 es el registro del predicado</span><span class="sxs-lookup"><span data-stu-id="7ab64-154">p0 is the predicate register</span></span>
-   <span data-ttu-id="7ab64-155">\[. swizzle \] es un swizzle opcional que se aplica al contenido del predicado Register antes de usarlo para enmascarar la instrucción.</span><span class="sxs-lookup"><span data-stu-id="7ab64-155">\[.swizzle\] is an optional swizzle to apply to the contents of the predicate register before using it to mask the instruction.</span></span> <span data-ttu-id="7ab64-156">Los swizzles disponibles son:. xyzw (valor predeterminado cuando no se especifica ninguno) o cualquier swizzle de replicación:. x/. r,. y/. g,. z/. b o. a/. w.</span><span class="sxs-lookup"><span data-stu-id="7ab64-156">The available swizzles are: .xyzw (default when none specified), or any replicate swizzle: .x/.r, .y/.g, .z/.b or .a/.w.</span></span>
-   <span data-ttu-id="7ab64-157">Instruction es cualquier Aritmetic o instrucción de textura.</span><span class="sxs-lookup"><span data-stu-id="7ab64-157">instruction is any aritmetic, or texture instruction.</span></span> <span data-ttu-id="7ab64-158">No puede ser una instrucción de control de flujo estático o dinámico.</span><span class="sxs-lookup"><span data-stu-id="7ab64-158">This cannot be a static or dynamic flow control instruction.</span></span>
-   <span data-ttu-id="7ab64-159">Dest, src0,... son los registros requeridos por la instrucción</span><span class="sxs-lookup"><span data-stu-id="7ab64-159">dest, src0, ... are the registers required by the instruction</span></span>

<span data-ttu-id="7ab64-160">Suponiendo que el registro de predicado se ha configurado con valores de componente (true, true, false, false), se puede aplicar a esta instrucción:</span><span class="sxs-lookup"><span data-stu-id="7ab64-160">Assuming the predicate register has been set up with (true, true, false, false) component values, it can be applied to this instruction:</span></span>


```
(p0) add r1, r2, r3
```



<span data-ttu-id="7ab64-161">para realizar una adición de dos componentes.</span><span class="sxs-lookup"><span data-stu-id="7ab64-161">to perform a 2 component add.</span></span>


```
r1.x = r2.x + r3.x
r1.y = r2.y + r3.y
```



<span data-ttu-id="7ab64-162">Los componentes z y w de R1 no se escribirán, ya que el registro de predicado contenía false en los componentes z y w.</span><span class="sxs-lookup"><span data-stu-id="7ab64-162">The z and w components of r1 will not be written since the predicate register contained false in components z and w.</span></span>

<span data-ttu-id="7ab64-163">La aplicación del registro de predicado a una instrucción aritmética o de textura aumenta el número de ranuras de la instrucción en 1.</span><span class="sxs-lookup"><span data-stu-id="7ab64-163">Applying the predicate register to an arithmetic or texture instruction increases its instruction slot count by 1.</span></span>

<span data-ttu-id="7ab64-164">También se puede aplicar el registro de predicado a las instrucciones de [callnz Pred](callnz-pred---ps.md) - [PS](if-pred---ps.md)y [breakp-](break-p---ps.md) PS.</span><span class="sxs-lookup"><span data-stu-id="7ab64-164">The predicate register can also be applied to [if pred - ps](if-pred---ps.md), [callnz pred - ps](callnz-pred---ps.md) and [breakp - ps](break-p---ps.md) instructions.</span></span> <span data-ttu-id="7ab64-165">Estas instrucciones de control de flujo no tienen ningún aumento en el recuento de ranuras de instrucciones cuando se usa el registro de predicado.</span><span class="sxs-lookup"><span data-stu-id="7ab64-165">These flow control instructions do not have any increase in the instruction slot count when using the predicate register.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7ab64-166">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7ab64-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ab64-167">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="7ab64-167">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




