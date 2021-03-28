---
title: breakp-vs
description: Divida condicionalmente el bucle actual en el ENDLOOP-vs o endrep-vs más cercano. Use uno de los componentes del registro de predicado como condición para determinar si se debe realizar o no la instrucción.
ms.assetid: 940252a0-6f6a-45d8-9d2f-315cc97686ca
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dbd0d5e20040bc2d353287eb4243c9e9d6d21dc8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104077094"
---
# <a name="breakp---vs"></a><span data-ttu-id="37ac0-103">breakp-vs</span><span class="sxs-lookup"><span data-stu-id="37ac0-103">breakp - vs</span></span>

<span data-ttu-id="37ac0-104">Divida condicionalmente el bucle actual en el [ENDLOOP-vs](endloop---vs.md) o [endrep-vs](endrep---vs.md)más cercano. Use uno de los componentes del registro de predicado como condición para determinar si se debe realizar o no la instrucción.</span><span class="sxs-lookup"><span data-stu-id="37ac0-104">Conditionally break out of the current loop at the nearest [endloop - vs](endloop---vs.md) or [endrep - vs](endrep---vs.md). Use one of the components of the predicate register as a condition to determine whether or not to perform the instruction.</span></span>

## <a name="syntax"></a><span data-ttu-id="37ac0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="37ac0-105">Syntax</span></span>



| <span data-ttu-id="37ac0-106">breakp \[ ! \] P0. x1</span><span class="sxs-lookup"><span data-stu-id="37ac0-106">breakp \[!\]p0.{x\</span></span>|<span data-ttu-id="37ac0-107">sí</span><span class="sxs-lookup"><span data-stu-id="37ac0-107">y\</span></span>|<span data-ttu-id="37ac0-108">z</span><span class="sxs-lookup"><span data-stu-id="37ac0-108">z\</span></span>|<span data-ttu-id="37ac0-109">con</span><span class="sxs-lookup"><span data-stu-id="37ac0-109">w}</span></span> |
|-----------------------------|



 

<span data-ttu-id="37ac0-110">Donde:</span><span class="sxs-lookup"><span data-stu-id="37ac0-110">Where:</span></span>

-   <span data-ttu-id="37ac0-111">\[!\] booleano opcional no.</span><span class="sxs-lookup"><span data-stu-id="37ac0-111">\[!\] optional boolean NOT.</span></span>
-   <span data-ttu-id="37ac0-112">P0 es el registro del predicado.</span><span class="sxs-lookup"><span data-stu-id="37ac0-112">p0 is the predicate register.</span></span> <span data-ttu-id="37ac0-113">Vea [registro de predicados](dx9-graphics-reference-asm-vs-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="37ac0-113">See [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md).</span></span>
-   <span data-ttu-id="37ac0-114">{x \| y \| z \| w} es el swizzle de replicación necesario en P0.</span><span class="sxs-lookup"><span data-stu-id="37ac0-114">{x\|y\|z\|w} is the required replicate swizzle on p0.</span></span>

## <a name="remarks"></a><span data-ttu-id="37ac0-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="37ac0-115">Remarks</span></span>



| <span data-ttu-id="37ac0-116">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="37ac0-116">Vertex shader versions</span></span> | <span data-ttu-id="37ac0-117">1\_1</span><span class="sxs-lookup"><span data-stu-id="37ac0-117">1\_1</span></span> | <span data-ttu-id="37ac0-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="37ac0-118">2\_0</span></span> | <span data-ttu-id="37ac0-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="37ac0-119">2\_x</span></span> | <span data-ttu-id="37ac0-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="37ac0-120">2\_sw</span></span> | <span data-ttu-id="37ac0-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="37ac0-121">3\_0</span></span> | <span data-ttu-id="37ac0-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="37ac0-122">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="37ac0-123">breakp</span><span class="sxs-lookup"><span data-stu-id="37ac0-123">breakp</span></span>                 |      |      | <span data-ttu-id="37ac0-124">x</span><span class="sxs-lookup"><span data-stu-id="37ac0-124">x</span></span>    | <span data-ttu-id="37ac0-125">x</span><span class="sxs-lookup"><span data-stu-id="37ac0-125">x</span></span>     | <span data-ttu-id="37ac0-126">x</span><span class="sxs-lookup"><span data-stu-id="37ac0-126">x</span></span>    | <span data-ttu-id="37ac0-127">x</span><span class="sxs-lookup"><span data-stu-id="37ac0-127">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="37ac0-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="37ac0-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37ac0-129">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="37ac0-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




