---
title: Diferencias del sombreador de vértices
description: Diferencias del sombreador de vértices
ms.assetid: 94fe4033-94c0-4561-b0fd-1fb85d8f796b
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1c74603f9eab4ea91e9220bbaa172c0262aeda99
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077883"
---
# <a name="vertex-shader-differences"></a><span data-ttu-id="60fad-103">Diferencias del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="60fad-103">Vertex Shader Differences</span></span>

## <a name="instruction-slots"></a><span data-ttu-id="60fad-104">Ranuras de instrucciones</span><span class="sxs-lookup"><span data-stu-id="60fad-104">Instruction Slots</span></span>

<span data-ttu-id="60fad-105">Cada versión admite un número distinto de ranuras de instrucciones máximas.</span><span class="sxs-lookup"><span data-stu-id="60fad-105">Each version supports a differing number of maximum instruction slots.</span></span>



| <span data-ttu-id="60fad-106">Versión</span><span class="sxs-lookup"><span data-stu-id="60fad-106">Version</span></span>  | <span data-ttu-id="60fad-107">Número máximo de ranuras de instrucciones</span><span class="sxs-lookup"><span data-stu-id="60fad-107">Maximum number of instruction slots</span></span>                                                                                               |
|----------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60fad-108">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="60fad-108">vs\_1\_1</span></span> | <span data-ttu-id="60fad-109">128</span><span class="sxs-lookup"><span data-stu-id="60fad-109">128</span></span>                                                                                                                               |
| <span data-ttu-id="60fad-110">vs \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="60fad-110">vs\_2\_0</span></span> | <span data-ttu-id="60fad-111">256</span><span class="sxs-lookup"><span data-stu-id="60fad-111">256</span></span>                                                                                                                               |
| <span data-ttu-id="60fad-112">vs \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="60fad-112">vs\_2\_x</span></span> | <span data-ttu-id="60fad-113">256</span><span class="sxs-lookup"><span data-stu-id="60fad-113">256</span></span>                                                                                                                               |
| <span data-ttu-id="60fad-114">vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="60fad-114">vs\_3\_0</span></span> | <span data-ttu-id="60fad-115">512 como mínimo y hasta el número de ranuras de D3DCAPS9. MaxVertexShader30InstructionSlots.</span><span class="sxs-lookup"><span data-stu-id="60fad-115">512 minimum, and up to the number of slots in D3DCAPS9.MaxVertexShader30InstructionSlots.</span></span> <span data-ttu-id="60fad-116">Vea [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="60fad-116">See [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9).</span></span> |



 

<span data-ttu-id="60fad-117">Para obtener información sobre las limitaciones de los sombreadores de software, consulte [sombreadores de software](dx9-graphics-reference-asm-software-shaders.md).</span><span class="sxs-lookup"><span data-stu-id="60fad-117">For information about the limitations of software shaders, see [Software Shaders](dx9-graphics-reference-asm-software-shaders.md).</span></span>

## <a name="flow-control-nesting-limits"></a><span data-ttu-id="60fad-118">Límites de anidamiento de control de flujo</span><span class="sxs-lookup"><span data-stu-id="60fad-118">Flow Control Nesting Limits</span></span>

-   <span data-ttu-id="60fad-119">Consulte [límites de anidamiento de control de flujo](dx9-graphics-reference-asm-vs-instructions-flow-control.md).</span><span class="sxs-lookup"><span data-stu-id="60fad-119">See [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md).</span></span>

## <a name="vs_1_1-features"></a><span data-ttu-id="60fad-120">vs \_ 1 \_ 1 características</span><span class="sxs-lookup"><span data-stu-id="60fad-120">vs\_1\_1 Features</span></span>

<span data-ttu-id="60fad-121">Nuevas instrucciones:</span><span class="sxs-lookup"><span data-stu-id="60fad-121">New instructions:</span></span>

<span data-ttu-id="60fad-122">Consulte las [instrucciones-vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-instructions-vs-1-1.md).</span><span class="sxs-lookup"><span data-stu-id="60fad-122">See [Instructions - vs\_1\_1](dx9-graphics-reference-asm-vs-instructions-vs-1-1.md).</span></span>

<span data-ttu-id="60fad-123">Nuevos registros:</span><span class="sxs-lookup"><span data-stu-id="60fad-123">New registers:</span></span>

<span data-ttu-id="60fad-124">Consulte [registros-vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md).</span><span class="sxs-lookup"><span data-stu-id="60fad-124">See [Registers - vs\_1\_1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md).</span></span>

## <a name="vs_2_0-features"></a><span data-ttu-id="60fad-125">vs \_ 2 \_ 0 características</span><span class="sxs-lookup"><span data-stu-id="60fad-125">vs\_2\_0 Features</span></span>

<span data-ttu-id="60fad-126">Características nuevas:</span><span class="sxs-lookup"><span data-stu-id="60fad-126">New features:</span></span>

-   <span data-ttu-id="60fad-127">Control de flujo estático</span><span class="sxs-lookup"><span data-stu-id="60fad-127">Static flow control</span></span>
-   <span data-ttu-id="60fad-128">Los cuatro componentes del [registro de direcciones](dx9-graphics-reference-asm-vs-registers-address.md) (a0) están disponibles.</span><span class="sxs-lookup"><span data-stu-id="60fad-128">All four components of the [Address Register](dx9-graphics-reference-asm-vs-registers-address.md) (a0) are available.</span></span>

<span data-ttu-id="60fad-129">Nuevas instrucciones:</span><span class="sxs-lookup"><span data-stu-id="60fad-129">New instructions:</span></span>

-   <span data-ttu-id="60fad-130">Instrucciones de instalación- [defb-vs](defb---vs.md), [defi-vs](defi---vs.md)</span><span class="sxs-lookup"><span data-stu-id="60fad-130">Setup instructions - [defb - vs](defb---vs.md), [defi - vs](defi---vs.md)</span></span>
-   <span data-ttu-id="60fad-131">Instrucciones aritméticas- [ABS-vs](abs---vs.md), [CRS-vs](crs---vs.md), [LRP-vs](lrp---vs.md), [mova-vs](mova---vs.md), [NRM-vs](nrm---vs.md), [Pow-vs](pow---vs.md), [SGN-vs](sgn---vs.md), [sincos (-vs](sincos---vs.md)</span><span class="sxs-lookup"><span data-stu-id="60fad-131">Arithmetic instructions - [abs - vs](abs---vs.md), [crs - vs](crs---vs.md), [lrp - vs](lrp---vs.md), [mova - vs](mova---vs.md), [nrm - vs](nrm---vs.md), [pow - vs](pow---vs.md), [sgn - vs](sgn---vs.md), [sincos - vs](sincos---vs.md)</span></span>
-   <span data-ttu-id="60fad-132">Instrucciones de control de flujo estático: [Call-vs](call---vs.md), [callnz bool-vs](callnz-bool---vs.md), [else-vs](else---vs.md), [endif-vs](endif---vs.md), [ENDLOOP-vs](endloop---vs.md), [endrep-vs](endrep---vs.md), [If bool-vs](if-bool---vs.md), [etiqueta-vs](label---vs.md), [Loop-vs](loop---vs.md), [REP-vs](rep---vs.md), [RET-vs](ret---vs.md)</span><span class="sxs-lookup"><span data-stu-id="60fad-132">Static flow control instructions - [call - vs](call---vs.md), [callnz bool - vs](callnz-bool---vs.md), [else - vs](else---vs.md), [endif - vs](endif---vs.md), [endloop - vs](endloop---vs.md), [endrep - vs](endrep---vs.md), [if bool - vs](if-bool---vs.md), [label - vs](label---vs.md), [loop - vs](loop---vs.md), [rep - vs](rep---vs.md), [ret - vs](ret---vs.md)</span></span>

<span data-ttu-id="60fad-133">Nuevos registros:</span><span class="sxs-lookup"><span data-stu-id="60fad-133">New registers:</span></span>

-   <span data-ttu-id="60fad-134">[Registro booleano constante](dx9-graphics-reference-asm-vs-registers-constant-boolean.md) (b \# )</span><span class="sxs-lookup"><span data-stu-id="60fad-134">[Constant Boolean Register](dx9-graphics-reference-asm-vs-registers-constant-boolean.md) (b\#)</span></span>
-   <span data-ttu-id="60fad-135">[Registro de entero constante](dx9-graphics-reference-asm-vs-registers-constant-integer.md) (i \# )</span><span class="sxs-lookup"><span data-stu-id="60fad-135">[Constant Integer Register](dx9-graphics-reference-asm-vs-registers-constant-integer.md) (i\#)</span></span>
-   <span data-ttu-id="60fad-136">[Registro de contador de bucle](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (al)</span><span class="sxs-lookup"><span data-stu-id="60fad-136">[Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL)</span></span>

## <a name="vs_2_x-features"></a><span data-ttu-id="60fad-137">Características de vs \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="60fad-137">vs\_2\_x Features</span></span>

<span data-ttu-id="60fad-138">Nuevas características (D3DCAPS9. VS20Caps):</span><span class="sxs-lookup"><span data-stu-id="60fad-138">New features (D3DCAPS9.VS20Caps):</span></span>

-   <span data-ttu-id="60fad-139">Control de flujo dinámico</span><span class="sxs-lookup"><span data-stu-id="60fad-139">Dynamic flow control</span></span>
-   <span data-ttu-id="60fad-140">Anidar instrucciones de control de flujo dinámico y estático</span><span class="sxs-lookup"><span data-stu-id="60fad-140">Nesting for dynamic and static flow control instructions</span></span>
-   <span data-ttu-id="60fad-141">Número de [registros temporales](dx9-graphics-reference-asm-vs-registers-temporary.md) \# incrementados (r)</span><span class="sxs-lookup"><span data-stu-id="60fad-141">Number of [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md)s (r\#) increased</span></span>
-   <span data-ttu-id="60fad-142">Predicación</span><span class="sxs-lookup"><span data-stu-id="60fad-142">Predication</span></span>

<span data-ttu-id="60fad-143">Nuevas instrucciones:</span><span class="sxs-lookup"><span data-stu-id="60fad-143">New Instructions:</span></span>

-   <span data-ttu-id="60fad-144">Instrucciones de control de flujo dinámico: [break-vs](break---vs.md), [break \_ COMP-vs](break-comp---vs.md), [breakp-vs](breakp---vs.md), [callnz Pred-vs](callnz-pred---vs.md), [If \_ COMP-vs](if-comp---vs.md), [si Pred-vs](if-pred---vs.md), [SETP \_ COMP-vs](setp-comp---vs.md)</span><span class="sxs-lookup"><span data-stu-id="60fad-144">Dynamic flow control instructions - [break - vs](break---vs.md), [break\_comp - vs](break-comp---vs.md), [breakp - vs](breakp---vs.md), [callnz pred - vs](callnz-pred---vs.md), [if\_comp - vs](if-comp---vs.md), [if pred - vs](if-pred---vs.md), [setp\_comp - vs](setp-comp---vs.md)</span></span>

<span data-ttu-id="60fad-145">Nuevos registros:</span><span class="sxs-lookup"><span data-stu-id="60fad-145">New registers:</span></span>

-   <span data-ttu-id="60fad-146">[Registro de predicado](dx9-graphics-reference-asm-vs-registers-predicate.md) (P0)</span><span class="sxs-lookup"><span data-stu-id="60fad-146">[Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md) (p0)</span></span>

## <a name="vs_3_0-features"></a><span data-ttu-id="60fad-147">vs \_ 3 \_ 0 características</span><span class="sxs-lookup"><span data-stu-id="60fad-147">vs\_3\_0 Features</span></span>

<span data-ttu-id="60fad-148">Nuevas características:</span><span class="sxs-lookup"><span data-stu-id="60fad-148">New features :</span></span>

-   <span data-ttu-id="60fad-149">Búsqueda de texturas</span><span class="sxs-lookup"><span data-stu-id="60fad-149">Texture lookup</span></span>
-   <span data-ttu-id="60fad-150">Registros de [salida](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) indexables (o \# )</span><span class="sxs-lookup"><span data-stu-id="60fad-150">Indexable [Output Registers](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) (o\#)</span></span>
-   <span data-ttu-id="60fad-151">Número de [registros temporales](dx9-graphics-reference-asm-vs-registers-temporary.md)(r \# ) incrementados en 32</span><span class="sxs-lookup"><span data-stu-id="60fad-151">Number of [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md)s (r\#) increased to 32</span></span>

<span data-ttu-id="60fad-152">Nuevas instrucciones:</span><span class="sxs-lookup"><span data-stu-id="60fad-152">New instructions:</span></span>

-   <span data-ttu-id="60fad-153">Instrucción de instalación- [DCL \_ samplerType (SM3-vs ASM)](dcl-samplertype---vs.md)</span><span class="sxs-lookup"><span data-stu-id="60fad-153">Setup instruction - [dcl\_samplerType (sm3 - vs asm)](dcl-samplertype---vs.md)</span></span>
-   <span data-ttu-id="60fad-154">Instrucción de textura- [texldl-vs](texldl---vs.md)</span><span class="sxs-lookup"><span data-stu-id="60fad-154">Texture instruction - [texldl - vs](texldl---vs.md)</span></span>

<span data-ttu-id="60fad-155">Nuevos registros:</span><span class="sxs-lookup"><span data-stu-id="60fad-155">New registers:</span></span>

-   <span data-ttu-id="60fad-156">[Muestra (Direct3D 9 ASM-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md) (s \# )</span><span class="sxs-lookup"><span data-stu-id="60fad-156">[Sampler (Direct3D 9 asm-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md) (s\#)</span></span>

## <a name="related-topics"></a><span data-ttu-id="60fad-157">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="60fad-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60fad-158">Sombreadores de vértices</span><span class="sxs-lookup"><span data-stu-id="60fad-158">Vertex Shaders</span></span>](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 