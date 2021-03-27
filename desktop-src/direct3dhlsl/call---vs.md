---
title: llamada-vs
description: Realiza una llamada de función a la instrucción marcada con la etiqueta proporcionada. | llamada-vs
ms.assetid: 3c1ec529-1ee4-40d9-8ce5-f8e7a61fde9c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c797e7ef6745f5710752fe059d2a2ff1f94a8aa3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104003742"
---
# <a name="call---vs"></a><span data-ttu-id="937c2-104">llamada-vs</span><span class="sxs-lookup"><span data-stu-id="937c2-104">call - vs</span></span>

<span data-ttu-id="937c2-105">Realiza una llamada de función a la instrucción marcada con la etiqueta proporcionada.</span><span class="sxs-lookup"><span data-stu-id="937c2-105">Performs a function call to the instruction marked with the provided label.</span></span>

## <a name="syntax"></a><span data-ttu-id="937c2-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="937c2-106">Syntax</span></span>



| <span data-ttu-id="937c2-107">llamar a l\#</span><span class="sxs-lookup"><span data-stu-id="937c2-107">call l\#</span></span> |
|----------|



 

<span data-ttu-id="937c2-108">donde l \# es una [etiqueta,](label---vs.md) que marca el principio de la subrutina a la que se va a llamar.</span><span class="sxs-lookup"><span data-stu-id="937c2-108">where l\# is a [label - vs](label---vs.md) marking the beginning of the subroutine to be called.</span></span>

## <a name="remarks"></a><span data-ttu-id="937c2-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="937c2-109">Remarks</span></span>



| <span data-ttu-id="937c2-110">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="937c2-110">Vertex shader versions</span></span> | <span data-ttu-id="937c2-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="937c2-111">1\_1</span></span> | <span data-ttu-id="937c2-112">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="937c2-112">2\_0</span></span> | <span data-ttu-id="937c2-113">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="937c2-113">2\_x</span></span> | <span data-ttu-id="937c2-114">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="937c2-114">2\_sw</span></span> | <span data-ttu-id="937c2-115">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="937c2-115">3\_0</span></span> | <span data-ttu-id="937c2-116">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="937c2-116">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="937c2-117">llamada</span><span class="sxs-lookup"><span data-stu-id="937c2-117">call</span></span>                   |      | <span data-ttu-id="937c2-118">x</span><span class="sxs-lookup"><span data-stu-id="937c2-118">x</span></span>    | <span data-ttu-id="937c2-119">x</span><span class="sxs-lookup"><span data-stu-id="937c2-119">x</span></span>    | <span data-ttu-id="937c2-120">x</span><span class="sxs-lookup"><span data-stu-id="937c2-120">x</span></span>     | <span data-ttu-id="937c2-121">x</span><span class="sxs-lookup"><span data-stu-id="937c2-121">x</span></span>    | <span data-ttu-id="937c2-122">x</span><span class="sxs-lookup"><span data-stu-id="937c2-122">x</span></span>     |



 

<span data-ttu-id="937c2-123">Esta instrucción hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="937c2-123">This instruction does the following:</span></span>

1.  <span data-ttu-id="937c2-124">Dirección de extracción de la instrucción siguiente a la pila de direcciones devuelta.</span><span class="sxs-lookup"><span data-stu-id="937c2-124">Push address of the next instruction to the return address stack.</span></span>
2.  <span data-ttu-id="937c2-125">Continúe con la ejecución de la instrucción marcada por la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="937c2-125">Continue execution from the instruction marked by the label.</span></span>

<span data-ttu-id="937c2-126">En el sombreador de vértices 2 \_ 0, no se permiten las llamadas anidadas.</span><span class="sxs-lookup"><span data-stu-id="937c2-126">In vertex shader 2\_0, nesting calls are not allowed.</span></span>

<span data-ttu-id="937c2-127">En el sombreador de vértices 2 \_ x, la profundidad de anidamiento está limitada por el elemento StaticFlowControlDepth de la estructura [**D3DVSHADERCAPS2 \_ 0**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dvshadercaps2_0) .</span><span class="sxs-lookup"><span data-stu-id="937c2-127">In vertex shader 2\_x, the nesting depth is limited by the StaticFlowControlDepth element of the [**D3DVSHADERCAPS2\_0**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dvshadercaps2_0) structure.</span></span> <span data-ttu-id="937c2-128">Para obtener más información, vea [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps).</span><span class="sxs-lookup"><span data-stu-id="937c2-128">For more information, see [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps).</span></span>

<span data-ttu-id="937c2-129">En el sombreador de vértices 3 \_ 0, se permiten cuatro niveles de anidamiento de llamadas.</span><span class="sxs-lookup"><span data-stu-id="937c2-129">In vertex shader 3\_0, four levels of call nesting are allowed.</span></span>

<span data-ttu-id="937c2-130">Solo se permiten llamadas hacia delante.</span><span class="sxs-lookup"><span data-stu-id="937c2-130">Only forward calls are allowed.</span></span> <span data-ttu-id="937c2-131">Esto significa que la ubicación de la etiqueta dentro del sombreador de vértices debe ser después de la instrucción de llamada que hace referencia a ella.</span><span class="sxs-lookup"><span data-stu-id="937c2-131">This means that the location of the label inside the vertex shader should be after the call instruction referencing it.</span></span>

<span data-ttu-id="937c2-132">Si una instrucción de llamada se invoca dentro del [bucle](loop---vs.md)... bloque [ENDLOOP](endloop---vs.md) , el valor del [registro de contador de bucle](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (al) es accesible dentro de la subrutina.</span><span class="sxs-lookup"><span data-stu-id="937c2-132">If a call instruction is invoked inside [loop](loop---vs.md)...[endloop](endloop---vs.md) block, the value of the [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL) is accessible inside the subroutine.</span></span>

<span data-ttu-id="937c2-133">Si una subrutina hace referencia al [registro de contador de bucle](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (al) ubicado fuera de la subrutina, cada instancia de la llamada a esta subrutina debe estar rodeada por un [bucle](loop---vs.md)... bloque [ENDLOOP](endloop---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="937c2-133">If a subroutine is referencing the [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL) located outside of the subroutine, every instance of the call to this subroutine should be surrounded by a [loop](loop---vs.md)...[endloop](endloop---vs.md) block.</span></span>

## <a name="related-topics"></a><span data-ttu-id="937c2-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="937c2-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="937c2-135">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="937c2-135">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
