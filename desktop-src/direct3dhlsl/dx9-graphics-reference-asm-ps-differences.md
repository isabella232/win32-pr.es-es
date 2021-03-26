---
title: Diferencias entre el sombreador de píxeles
description: Diferencias entre el sombreador de píxeles
ms.assetid: 11aefb26-eb82-486c-81ff-7c0cfbab1b7a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9a74b5cc7588220fdc5173c470f7852ee9ef763d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420901"
---
# <a name="pixel-shader-differences"></a><span data-ttu-id="791a1-103">Diferencias entre el sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="791a1-103">Pixel Shader Differences</span></span>

## <a name="instruction-slots"></a><span data-ttu-id="791a1-104">Ranuras de instrucciones</span><span class="sxs-lookup"><span data-stu-id="791a1-104">Instruction Slots</span></span>

<span data-ttu-id="791a1-105">Cada versión admite un número diferente de ranuras de instrucciones máximas.</span><span class="sxs-lookup"><span data-stu-id="791a1-105">Each version supports a different number of maximum instruction slots.</span></span>



| <span data-ttu-id="791a1-106">Versión</span><span class="sxs-lookup"><span data-stu-id="791a1-106">Version</span></span>  | <span data-ttu-id="791a1-107">Número máximo de ranuras de instrucciones</span><span class="sxs-lookup"><span data-stu-id="791a1-107">Maximum number of instruction slots</span></span>                                                                                   |
|----------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="791a1-108">PS \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="791a1-108">ps\_1\_1</span></span> | <span data-ttu-id="791a1-109">4 textura + 8 aritméticos</span><span class="sxs-lookup"><span data-stu-id="791a1-109">4 texture + 8 arithmetic</span></span>                                                                                              |
| <span data-ttu-id="791a1-110">PS \_ 1 \_ 2</span><span class="sxs-lookup"><span data-stu-id="791a1-110">ps\_1\_2</span></span> | <span data-ttu-id="791a1-111">4 textura + 8 aritméticos</span><span class="sxs-lookup"><span data-stu-id="791a1-111">4 texture + 8 arithmetic</span></span>                                                                                              |
| <span data-ttu-id="791a1-112">PS \_ 1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="791a1-112">ps\_1\_3</span></span> | <span data-ttu-id="791a1-113">4 textura + 8 aritméticos</span><span class="sxs-lookup"><span data-stu-id="791a1-113">4 texture + 8 arithmetic</span></span>                                                                                              |
| <span data-ttu-id="791a1-114">PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="791a1-114">ps\_1\_4</span></span> | <span data-ttu-id="791a1-115">6 textura + 8 aritmético por fase</span><span class="sxs-lookup"><span data-stu-id="791a1-115">6 texture + 8 arithmetic per phase</span></span>                                                                                    |
| <span data-ttu-id="791a1-116">PS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="791a1-116">ps\_2\_0</span></span> | <span data-ttu-id="791a1-117">32 textura + 64 aritmética</span><span class="sxs-lookup"><span data-stu-id="791a1-117">32 texture + 64 arithmetic</span></span>                                                                                            |
| <span data-ttu-id="791a1-118">PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="791a1-118">ps\_2\_x</span></span> | <span data-ttu-id="791a1-119">96 como mínimo y hasta el número de ranuras de D3DCAPS9. D3DPSHADERCAPS2 \_ 0. NumInstructionSlots.</span><span class="sxs-lookup"><span data-stu-id="791a1-119">96 minimum, and up to the number of slots in D3DCAPS9.D3DPSHADERCAPS2\_0.NumInstructionSlots.</span></span> <span data-ttu-id="791a1-120">Vea D3DPSHADERCAPS2 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="791a1-120">See D3DPSHADERCAPS2\_0.</span></span> |
| <span data-ttu-id="791a1-121">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="791a1-121">ps\_3\_0</span></span> | <span data-ttu-id="791a1-122">512 como mínimo y hasta el número de ranuras de D3DCAPS9. MaxPixelShader30InstructionSlots.</span><span class="sxs-lookup"><span data-stu-id="791a1-122">512 minimum, and up to the number of slots in D3DCAPS9.MaxPixelShader30InstructionSlots.</span></span> <span data-ttu-id="791a1-123">Vea D3DPSHADERCAPS2 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="791a1-123">See D3DPSHADERCAPS2\_0.</span></span>      |



 

<span data-ttu-id="791a1-124">Para obtener información sobre las limitaciones de los sombreadores de software, consulte [sombreadores de software](dx9-graphics-reference-asm-software-shaders.md).</span><span class="sxs-lookup"><span data-stu-id="791a1-124">For information about the limitations of software shaders, see [Software Shaders](dx9-graphics-reference-asm-software-shaders.md).</span></span>

## <a name="flow-control-nesting-limits"></a><span data-ttu-id="791a1-125">Límites de anidamiento de control de flujo</span><span class="sxs-lookup"><span data-stu-id="791a1-125">Flow Control Nesting Limits</span></span>

-   <span data-ttu-id="791a1-126">Vea [limitaciones del control de flujo](dx9-graphics-reference-asm-ps-instructions-flow-control.md).</span><span class="sxs-lookup"><span data-stu-id="791a1-126">See [Flow Control Limitations](dx9-graphics-reference-asm-ps-instructions-flow-control.md).</span></span>

## <a name="ps_1_x-features"></a><span data-ttu-id="791a1-127">Características de PS \_ 1 \_ x</span><span class="sxs-lookup"><span data-stu-id="791a1-127">ps\_1\_x Features</span></span>

<span data-ttu-id="791a1-128">Nuevas instrucciones:</span><span class="sxs-lookup"><span data-stu-id="791a1-128">New instructions:</span></span>

<span data-ttu-id="791a1-129">Consulte las instrucciones PS 1, PS 1 [ \_ \_ \_ \_ 2, PS 1 \_ \_ 3, PS \_ 1 \_ 4](dx9-graphics-reference-asm-ps-instructions-ps-1-x.md).</span><span class="sxs-lookup"><span data-stu-id="791a1-129">See [ps\_1\_1, ps\_1\_2, ps\_1\_3, ps\_1\_4 Instructions](dx9-graphics-reference-asm-ps-instructions-ps-1-x.md).</span></span>

<span data-ttu-id="791a1-130">Nuevos registros:</span><span class="sxs-lookup"><span data-stu-id="791a1-130">New registers:</span></span>

<span data-ttu-id="791a1-131">Vea [PS \_ 1 \_ 1 \_ \_ PS \_ 1 \_ 2 \_ \_ PS \_ 1 \_ 3 \_ \_ PS \_ 1 \_ 4 registros](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span><span class="sxs-lookup"><span data-stu-id="791a1-131">See [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="ps_2_0-features"></a><span data-ttu-id="791a1-132">Características de PS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="791a1-132">ps\_2\_0 Features</span></span>

<span data-ttu-id="791a1-133">Características nuevas:</span><span class="sxs-lookup"><span data-stu-id="791a1-133">New features:</span></span>

-   <span data-ttu-id="791a1-134">Tres nuevos swizzles-. yzxw,. zxyw,. wzyx</span><span class="sxs-lookup"><span data-stu-id="791a1-134">Three new swizzles - .yzxw, .zxyw, .wzyx</span></span>
-   <span data-ttu-id="791a1-135">El número de [registro temporal](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) aumentó a 12</span><span class="sxs-lookup"><span data-stu-id="791a1-135">Number of [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#) increased to 12</span></span>
-   <span data-ttu-id="791a1-136">El número de registros de [registro Float constantes](dx9-graphics-reference-asm-ps-registers-constant-float.md) (c \# ) aumentó a 32</span><span class="sxs-lookup"><span data-stu-id="791a1-136">Number of [Constant Float Register](dx9-graphics-reference-asm-ps-registers-constant-float.md) registers (c\#) increased to 32</span></span>
-   <span data-ttu-id="791a1-137">El número de [registros de coordenadas de textura](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md)(t \# ) aumentó a 8</span><span class="sxs-lookup"><span data-stu-id="791a1-137">Number of [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md)s (t\#) increased to 8</span></span>

<span data-ttu-id="791a1-138">Nuevas instrucciones:</span><span class="sxs-lookup"><span data-stu-id="791a1-138">New instructions:</span></span>

-   <span data-ttu-id="791a1-139">Instrucciones de instalación- [DCL-(SM2, SM3-PS ASM)](dcl---ps.md), [DCL \_ samplerType (SM2, SM3-PS ASM)](dcl-samplertype---ps.md)</span><span class="sxs-lookup"><span data-stu-id="791a1-139">Setup instructions - [dcl - (sm2, sm3 - ps asm)](dcl---ps.md), [dcl\_samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md)</span></span>
-   <span data-ttu-id="791a1-140">Instrucciones aritméticas- [ABS-PS](abs---ps.md), [CRS-PS](crs---ps.md), [dp2add-PS](dp2add---ps.md), [exp-PS](exp---ps.md), [FRC-PS](frc---ps.md), [log-PS](log---ps.md), [m3x2-PS](m3x2---ps.md), [M3x3-PS](m3x3---ps.md), [M3x4-](m3x4---ps.md)PS [, m4x3-PS,](m4x3---ps.md) [M4x4-PS](m4x4---ps.md), [Max-PS](max---ps.md), [min-PS](min---ps.md), [NRM-PS](nrm---ps.md), [Pow-PS](pow---ps.md), [RCP-PS](rcp---ps.md), [RSQ-PS](rsq---ps.md), [sincos (-PS](sincos---ps.md)</span><span class="sxs-lookup"><span data-stu-id="791a1-140">Arithmetic instructions - [abs - ps](abs---ps.md), [crs - ps](crs---ps.md), [dp2add - ps](dp2add---ps.md), [exp - ps](exp---ps.md), [frc - ps](frc---ps.md), [log - ps](log---ps.md), [m3x2 - ps](m3x2---ps.md), [m3x3 - ps](m3x3---ps.md), [m3x4 - ps](m3x4---ps.md), [m4x3 - ps](m4x3---ps.md), [m4x4 - ps](m4x4---ps.md), [max - ps](max---ps.md), [min - ps](min---ps.md), [nrm - ps](nrm---ps.md), [pow - ps](pow---ps.md), [rcp - ps](rcp---ps.md), [rsq - ps](rsq---ps.md), [sincos - ps](sincos---ps.md)</span></span>
-   <span data-ttu-id="791a1-141">Instrucciones de textura: [texld-PS \_ 2 \_ 0 y up](texld---ps-2-0.md) (sintaxis diferente), [texldb-PS](texldb---ps.md), [texldp-PS](texldp---ps.md)</span><span class="sxs-lookup"><span data-stu-id="791a1-141">Texture instructions - [texld - ps\_2\_0 and up](texld---ps-2-0.md) (different syntax), [texldb - ps](texldb---ps.md), [texldp - ps](texldp---ps.md)</span></span>

<span data-ttu-id="791a1-142">Nuevos registros:</span><span class="sxs-lookup"><span data-stu-id="791a1-142">New registers:</span></span>

-   <span data-ttu-id="791a1-143">[Muestra (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s \# )</span><span class="sxs-lookup"><span data-stu-id="791a1-143">[Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#)</span></span>

## <a name="ps_2_x-features"></a><span data-ttu-id="791a1-144">Características de PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="791a1-144">ps\_2\_x Features</span></span>

<span data-ttu-id="791a1-145">Nuevas características (consulte [**D3DPSHADERCAPS2 \_ 0**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0)):</span><span class="sxs-lookup"><span data-stu-id="791a1-145">New features (See [**D3DPSHADERCAPS2\_0**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0).):</span></span>

-   <span data-ttu-id="791a1-146">Control de flujo dinámico</span><span class="sxs-lookup"><span data-stu-id="791a1-146">Dynamic flow control</span></span>
-   <span data-ttu-id="791a1-147">Control de flujo estático</span><span class="sxs-lookup"><span data-stu-id="791a1-147">Static flow control</span></span>
-   <span data-ttu-id="791a1-148">Anidar instrucciones de control de flujo dinámico y estático</span><span class="sxs-lookup"><span data-stu-id="791a1-148">Nesting for dynamic and static flow control instructions</span></span>
-   <span data-ttu-id="791a1-149">Número de [registros temporales](dx9-graphics-reference-asm-ps-registers-temporary.md) \# incrementados (r)</span><span class="sxs-lookup"><span data-stu-id="791a1-149">Number of [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md)s (r\#) increased</span></span>
-   <span data-ttu-id="791a1-150">Swizzle de origen arbitrario</span><span class="sxs-lookup"><span data-stu-id="791a1-150">Arbitrary source swizzle</span></span>
-   <span data-ttu-id="791a1-151">Instrucciones de degradado</span><span class="sxs-lookup"><span data-stu-id="791a1-151">Gradient instructions</span></span>
-   <span data-ttu-id="791a1-152">Predicación</span><span class="sxs-lookup"><span data-stu-id="791a1-152">Predication</span></span>
-   <span data-ttu-id="791a1-153">Límite de lectura de textura dependiente</span><span class="sxs-lookup"><span data-stu-id="791a1-153">No dependent texture read limit</span></span>
-   <span data-ttu-id="791a1-154">No hay límite de instrucciones de textura</span><span class="sxs-lookup"><span data-stu-id="791a1-154">No texture instruction limit</span></span>

<span data-ttu-id="791a1-155">Nuevas instrucciones:</span><span class="sxs-lookup"><span data-stu-id="791a1-155">New instructions:</span></span>

-   <span data-ttu-id="791a1-156">Instrucciones de control de flujo estático: [si es bool-PS](if-bool---ps.md), [Call-PS](call---ps.md), [callnz bool-PS](callnz-bool---ps.md), [else-PS](else---ps.md), [endif-PS](endif---ps.md), [REP-PS](rep---ps.md), [endrep-PS](endrep---ps.md), [Label-PS](label---ps.md), [RET-PS](ret---ps.md)</span><span class="sxs-lookup"><span data-stu-id="791a1-156">Static flow control instructions - [if bool - ps](if-bool---ps.md), [call - ps](call---ps.md), [callnz bool - ps](callnz-bool---ps.md), [else - ps](else---ps.md), [endif - ps](endif---ps.md), [rep - ps](rep---ps.md), [endrep - ps](endrep---ps.md), [label - ps](label---ps.md), [ret - ps](ret---ps.md)</span></span>
-   <span data-ttu-id="791a1-157">Instrucciones de control de flujo dinámico- [break-PS](break---ps.md), [break \_ COMP-PS](break-comp---ps.md), [breakp-PS](break-p---ps.md), [callnz Pred-PS](callnz-pred---ps.md), [If \_ COMP-PS](if-comp---ps.md), si se PREA [-PS](if-pred---ps.md), [SETP \_ COMP-PS](setp-comp---ps.md)</span><span class="sxs-lookup"><span data-stu-id="791a1-157">Dynamic flow control instructions - [break - ps](break---ps.md), [break\_comp - ps](break-comp---ps.md), [breakp - ps](break-p---ps.md), [callnz pred - ps](callnz-pred---ps.md), [if\_comp - ps](if-comp---ps.md), [if pred - ps](if-pred---ps.md), [setp\_comp - ps](setp-comp---ps.md)</span></span>
-   <span data-ttu-id="791a1-158">Instrucciones aritméticas- [DSX-PS](dsx---ps.md), [DSY-PS](dsy---ps.md)</span><span class="sxs-lookup"><span data-stu-id="791a1-158">Arithmetic instructions - [dsx - ps](dsx---ps.md), [dsy - ps](dsy---ps.md)</span></span>
-   <span data-ttu-id="791a1-159">Instrucción de textura: [texldd-PS](texldd---ps.md)</span><span class="sxs-lookup"><span data-stu-id="791a1-159">Texture instruction - [texldd - ps](texldd---ps.md)</span></span>

<span data-ttu-id="791a1-160">Nuevos registros:</span><span class="sxs-lookup"><span data-stu-id="791a1-160">New registers:</span></span>

-   <span data-ttu-id="791a1-161">[Registro de predicado](dx9-graphics-reference-asm-ps-registers-predicate.md) (P0)</span><span class="sxs-lookup"><span data-stu-id="791a1-161">[Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md) (p0)</span></span>

## <a name="ps_3_0-features"></a><span data-ttu-id="791a1-162">Características de PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="791a1-162">ps\_3\_0 Features</span></span>

<span data-ttu-id="791a1-163">Características nuevas:</span><span class="sxs-lookup"><span data-stu-id="791a1-163">New features:</span></span>

-   <span data-ttu-id="791a1-164">10 [registros de entrada](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)consolidados (v \# )</span><span class="sxs-lookup"><span data-stu-id="791a1-164">Consolidated 10 [Input Register](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)s (v\#)</span></span>
-   <span data-ttu-id="791a1-165">Registro del [color de entrada](dx9-graphics-reference-asm-ps-registers-input-color.md) indexable (v \# ) con el [contador de bucle Register](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (al)</span><span class="sxs-lookup"><span data-stu-id="791a1-165">Indexable [Input Color Register](dx9-graphics-reference-asm-ps-registers-input-color.md) (v\#) with the [Loop Counter Register](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (aL)</span></span>
-   <span data-ttu-id="791a1-166">Número de [registros temporales](dx9-graphics-reference-asm-ps-registers-temporary.md)(r \# ) incrementados en 32</span><span class="sxs-lookup"><span data-stu-id="791a1-166">Number of [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md)s (r\#) increased to 32</span></span>
-   <span data-ttu-id="791a1-167">Número de [registros Float constantes](dx9-graphics-reference-asm-ps-registers-constant-float.md)(c \# ) aumentado a 224</span><span class="sxs-lookup"><span data-stu-id="791a1-167">Number of [Constant Float Register](dx9-graphics-reference-asm-ps-registers-constant-float.md)s (c\#) increased to 224</span></span>

<span data-ttu-id="791a1-168">Nuevas instrucciones:</span><span class="sxs-lookup"><span data-stu-id="791a1-168">New instructions:</span></span>

-   <span data-ttu-id="791a1-169">Instrucción de configuración [: \_ semántica de DCL (SM3-PS ASM)](dcl-usage---ps.md)</span><span class="sxs-lookup"><span data-stu-id="791a1-169">Setup instruction - [dcl\_semantics (sm3 - ps asm)](dcl-usage---ps.md)</span></span>
-   <span data-ttu-id="791a1-170">Instrucciones de flujo estático: [Loop-PS](loop---ps.md), [ENDLOOP-PS](endloop---ps.md)</span><span class="sxs-lookup"><span data-stu-id="791a1-170">Static flow instructions - [loop - ps](loop---ps.md), [endloop - ps](endloop---ps.md)</span></span>
-   <span data-ttu-id="791a1-171">Instrucción aritmética- [sincos (-PS](sincos---ps.md) (nueva sintaxis)</span><span class="sxs-lookup"><span data-stu-id="791a1-171">Arithmetic instruction - [sincos - ps](sincos---ps.md) (new syntax)</span></span>
-   <span data-ttu-id="791a1-172">Instrucción de textura: [texldl-PS](texldl---ps.md)</span><span class="sxs-lookup"><span data-stu-id="791a1-172">Texture instruction - [texldl - ps](texldl---ps.md)</span></span>

<span data-ttu-id="791a1-173">Nuevos registros:</span><span class="sxs-lookup"><span data-stu-id="791a1-173">New registers:</span></span>

-   <span data-ttu-id="791a1-174">[Registro de entrada](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (v \# )</span><span class="sxs-lookup"><span data-stu-id="791a1-174">[Input Register](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (v\#)</span></span>
-   <span data-ttu-id="791a1-175">[Registro de posición](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (vPos)</span><span class="sxs-lookup"><span data-stu-id="791a1-175">[Position Register](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (vPos)</span></span>
-   <span data-ttu-id="791a1-176">[Registro facial](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (vFace)</span><span class="sxs-lookup"><span data-stu-id="791a1-176">[Face Register](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (vFace)</span></span>

## <a name="related-topics"></a><span data-ttu-id="791a1-177">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="791a1-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="791a1-178">Sombreadores de píxeles</span><span class="sxs-lookup"><span data-stu-id="791a1-178">Pixel Shaders</span></span>](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 