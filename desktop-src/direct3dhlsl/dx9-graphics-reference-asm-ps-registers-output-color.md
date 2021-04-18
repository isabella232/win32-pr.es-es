---
title: Registro de color de salida
description: Los registros de salida de color del sombreador de píxeles (oC \) son registros de solo escritura que generan resultados en varios destinos de representación.
ms.assetid: 88e69189-3956-47de-a336-921f1e62c025
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 316160e39ce172d56e4ecac17dfbd1d53077005b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421209"
---
# <a name="output-color-register"></a><span data-ttu-id="653c8-103">Registro de color de salida</span><span class="sxs-lookup"><span data-stu-id="653c8-103">Output Color Register</span></span>

<span data-ttu-id="653c8-104">Los registros de salida de color del sombreador de píxeles (oC #) son registros de solo escritura que generan resultados en varios destinos de representación.</span><span class="sxs-lookup"><span data-stu-id="653c8-104">The pixel shader color output registers (oC#) are write-only registers that output results to multiple render targets.</span></span>

<span data-ttu-id="653c8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="653c8-105">Syntax</span></span>



| <span data-ttu-id="653c8-106">Opcional #</span><span class="sxs-lookup"><span data-stu-id="653c8-106">oC#</span></span> |
|------|



 

<span data-ttu-id="653c8-107">Donde:</span><span class="sxs-lookup"><span data-stu-id="653c8-107">Where:</span></span>



| <span data-ttu-id="653c8-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="653c8-108">Name</span></span> | <span data-ttu-id="653c8-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="653c8-109">Description</span></span>       |
|------|-------------------|
| <span data-ttu-id="653c8-110">oC0</span><span class="sxs-lookup"><span data-stu-id="653c8-110">oC0</span></span>  | <span data-ttu-id="653c8-111">destino de representación \# 0</span><span class="sxs-lookup"><span data-stu-id="653c8-111">render target \#0</span></span> |
| <span data-ttu-id="653c8-112">oC1</span><span class="sxs-lookup"><span data-stu-id="653c8-112">oC1</span></span>  | <span data-ttu-id="653c8-113">destino de representación \# 1</span><span class="sxs-lookup"><span data-stu-id="653c8-113">render target \#1</span></span> |
| <span data-ttu-id="653c8-114">oC2</span><span class="sxs-lookup"><span data-stu-id="653c8-114">oC2</span></span>  | <span data-ttu-id="653c8-115">destino de representación \# 2</span><span class="sxs-lookup"><span data-stu-id="653c8-115">render target \#2</span></span> |
| <span data-ttu-id="653c8-116">oC3</span><span class="sxs-lookup"><span data-stu-id="653c8-116">oC3</span></span>  | <span data-ttu-id="653c8-117">destino de representación \# 3</span><span class="sxs-lookup"><span data-stu-id="653c8-117">render target \#3</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="653c8-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="653c8-118">Remarks</span></span>

-   <span data-ttu-id="653c8-119">Si oCn se escribe pero no hay ningún destino de representación correspondiente, se omite esta escritura en oCn.</span><span class="sxs-lookup"><span data-stu-id="653c8-119">If oCn is written but there is no corresponding render target, then this write to oCn is ignored.</span></span>
-   <span data-ttu-id="653c8-120">Los Estados de representación D3DRS \_ COLORWRITEENABLE, D3DRS \_ COLORWRITEENABLE1, D3DRS \_ COLORWRITEENABLE2 y D3DRS \_ COLORWRITEENABLE3 determinan qué componentes de oCn se escriben en última instancia en el destino de representación (después de Blend, si procede).</span><span class="sxs-lookup"><span data-stu-id="653c8-120">The render states D3DRS\_COLORWRITEENABLE, D3DRS\_COLORWRITEENABLE1, D3DRS\_COLORWRITEENABLE2 and D3DRS\_COLORWRITEENABLE3 determine which components of oCn ultimately get written to the render target (after blend, if applicable).</span></span> <span data-ttu-id="653c8-121">Si el sombreador escribe algunos, pero no todos los componentes definidos por los Estados de representación de D3DRS \_ COLORWRITEENABLE \* para un registro de oCn determinado, los canales sin escribir generan valores no definidos en el destino de representación correspondiente.</span><span class="sxs-lookup"><span data-stu-id="653c8-121">If the shader writes some but not all of the components defined by the D3DRS\_COLORWRITEENABLE\* render states for a given oCn register, then the unwritten channels produce undefined values in the corresponding render target.</span></span> <span data-ttu-id="653c8-122">Si no se escribe ninguno de los componentes de un oCn, el destino de representación correspondiente no debe actualizarse en absoluto (como se indicó anteriormente), por lo que \_ no se aplican los Estados de representación COLORWRITEENABLE de D3DRS \* .</span><span class="sxs-lookup"><span data-stu-id="653c8-122">If none of the components of an oCn are written, the corresponding render target must not be updated at all (as stated above), so the D3DRS\_COLORWRITEENABLE\* render states do not apply.</span></span>

### <a name="shader-model-2-restrictions"></a><span data-ttu-id="653c8-123">Restricciones del modelo 2 del sombreador</span><span class="sxs-lookup"><span data-stu-id="653c8-123">Shader Model 2 Restrictions</span></span>

-   <span data-ttu-id="653c8-124">oCn solo se puede escribir con la instrucción [MOV-PS](mov---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="653c8-124">oCn can only be written with the [mov - ps](mov---ps.md) instruction.</span></span>
-   <span data-ttu-id="653c8-125">oC0 debe estar siempre escrito en el sombreador.</span><span class="sxs-lookup"><span data-stu-id="653c8-125">oC0 must be always written in the shader.</span></span>
-   <span data-ttu-id="653c8-126">No se permite ningún swizzle de origen (excepto. xyzw = default swizzle) o el modificador de origen al escribir en cualquier oCn.</span><span class="sxs-lookup"><span data-stu-id="653c8-126">No source swizzle (except .xyzw = default swizzle) or source modifier is allowed when writing to any oCn.</span></span>
-   <span data-ttu-id="653c8-127">No se permite ninguna máscara de escritura de destino (excepto. xyzw = máscara predeterminada) o el modificador de instrucciones cuando se escribe en cualquier oCn.</span><span class="sxs-lookup"><span data-stu-id="653c8-127">No destination write mask (except .xyzw = default mask) or instruction modifier is allowed when writing to any oCn.</span></span>
-   <span data-ttu-id="653c8-128">Si se escribe oCn, también se debe escribir oC0-oCn-1.</span><span class="sxs-lookup"><span data-stu-id="653c8-128">If oCn is written, then oC0 - oCn-1 must also be written.</span></span> <span data-ttu-id="653c8-129">Por ejemplo, para escribir en oC2, también debe escribir en oC0 y oC1.</span><span class="sxs-lookup"><span data-stu-id="653c8-129">For example, to write to oC2, you must also write to oC0 and oC1.</span></span>
-   <span data-ttu-id="653c8-130">Como máximo, se permite una escritura en cualquier número de oC por sombreador.</span><span class="sxs-lookup"><span data-stu-id="653c8-130">At most one write to any oC# per shader is allowed.</span></span>
-   <span data-ttu-id="653c8-131">En el caso de PS \_ 2 \_ x y PS \_ 3 \_ 0, no se pueden escribir en los registros de OC # y OD \# en el control de flujo dinámico o en predication (el control de flujo estático de escrituras en OC es fino).</span><span class="sxs-lookup"><span data-stu-id="653c8-131">For ps\_2\_x and ps\_3\_0, you cannot write to oC# and oD\# registers within dynamic flow control or predication (writes to oC# inside static flow control is fine).</span></span>

### <a name="shader-model-3-restrictions"></a><span data-ttu-id="653c8-132">Restricciones del modelo de sombreador 3</span><span class="sxs-lookup"><span data-stu-id="653c8-132">Shader Model 3 Restrictions</span></span>

-   <span data-ttu-id="653c8-133">En el caso de PS \_ 3 \_ 0, los registros de salida \# se pueden escribir en cualquier número de veces.</span><span class="sxs-lookup"><span data-stu-id="653c8-133">For ps\_3\_0, output registers oC# and oD\# can be written any number of times.</span></span> <span data-ttu-id="653c8-134">La salida del sombreador de píxeles procede del contenido de los registros de salida al final de la ejecución del sombreador.</span><span class="sxs-lookup"><span data-stu-id="653c8-134">The output of the pixel shader comes from the contents of the output registers at the end of shader execution.</span></span> <span data-ttu-id="653c8-135">Si no se produce una escritura en un registro de salida, quizás debido al control de flujo o si el sombreador no lo escribió, tampoco se actualiza el rendertarget correspondiente.</span><span class="sxs-lookup"><span data-stu-id="653c8-135">If a write to an output register does not happen, perhaps due to flow control or if the shader just did not write it, the corresponding rendertarget is also not updated.</span></span> <span data-ttu-id="653c8-136">Si se escribe un subconjunto de los canales en un registro de salida, los valores no definidos se escribirán en los canales restantes.</span><span class="sxs-lookup"><span data-stu-id="653c8-136">If a subset of the channels in an output register are written, then undefined values will be written to the remaining channels.</span></span>
-   <span data-ttu-id="653c8-137">Para PS \_ 3 \_ 0, los registros de OC # se pueden escribir con cualquier writemasks.</span><span class="sxs-lookup"><span data-stu-id="653c8-137">For ps\_3\_0, the oC# registers can be written with any writemasks.</span></span>
-   <span data-ttu-id="653c8-138">En el caso de PS \_ 2 \_ x y PS \_ 3 \_ 0, no se pueden escribir en los registros de OC # y OD \# en el control de flujo dinámico o en predication (el control de flujo estático de escrituras en OC es fino).</span><span class="sxs-lookup"><span data-stu-id="653c8-138">For ps\_2\_x and ps\_3\_0, you cannot write to oC# and oD\# registers within dynamic flow control or predication (writes to oC# inside static flow control is fine).</span></span>
-   <span data-ttu-id="653c8-139">No puede realizar ningún cálculo de degradado (u operaciones que invoquen implícitamente los cálculos de degradado como [texld-PS \_ 2 \_ 0 y up](texld---ps-2-0.md), [texldb-PS](texldb---ps.md), [texldp-PS](texldp---ps.md)) dentro de las instrucciones de control de flujo cuyas condiciones de bifurcación varían en función de la primitiva (por ejemplo: instrucciones de control de flujo dinámico).</span><span class="sxs-lookup"><span data-stu-id="653c8-139">You may not perform any gradient calculations (or operations that implicitly invoke gradient calculations such as [texld - ps\_2\_0 and up](texld---ps-2-0.md), [texldb - ps](texldb---ps.md), [texldp - ps](texldp---ps.md)) inside of flow control statements whose branching conditions vary on a per-primitive basis (ie: dynamic flow control instructions).</span></span> <span data-ttu-id="653c8-140">La instrucción predication no se considera el control de flujo dinámico.</span><span class="sxs-lookup"><span data-stu-id="653c8-140">Instruction predication is not considered dynamic flow control.</span></span>

## <a name="related-topics"></a><span data-ttu-id="653c8-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="653c8-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="653c8-142">Registra</span><span class="sxs-lookup"><span data-stu-id="653c8-142">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> <dt>

[<span data-ttu-id="653c8-143">Varios destinos de representación (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="653c8-143">Multiple Render Targets (Direct3D 9)</span></span>](/windows/desktop/direct3d9/multiple-render-targets)
</dt> </dl>

 

 