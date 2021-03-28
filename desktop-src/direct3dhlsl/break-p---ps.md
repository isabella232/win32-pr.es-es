---
title: breakp-PS
description: Divida condicionalmente el bucle actual en el ENDLOOP-PS o endrep-PS más cercano. Use uno de los componentes del registro de predicado como condición para determinar si se debe realizar o no la instrucción.
ms.assetid: be219239-fccb-4561-8b71-083c47ba915b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6e358debb2377f08574997acd96c11f83d32e66c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419944"
---
# <a name="breakp---ps"></a><span data-ttu-id="e6b4a-104">breakp-PS</span><span class="sxs-lookup"><span data-stu-id="e6b4a-104">breakp - ps</span></span>

<span data-ttu-id="e6b4a-105">Divida condicionalmente el bucle actual en el [ENDLOOP-PS](endloop---ps.md) o [endrep-PS](endrep---ps.md)más cercano.</span><span class="sxs-lookup"><span data-stu-id="e6b4a-105">Conditionally break out of the current loop at the nearest [endloop - ps](endloop---ps.md) or [endrep - ps](endrep---ps.md).</span></span> <span data-ttu-id="e6b4a-106">Use uno de los componentes del registro de predicado como condición para determinar si se debe realizar o no la instrucción.</span><span class="sxs-lookup"><span data-stu-id="e6b4a-106">Use one of the components of the predicate register as a condition to determine whether or not to perform the instruction.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6b4a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e6b4a-107">Syntax</span></span>



| <span data-ttu-id="e6b4a-108">breakp \[ ! \] P0. x1</span><span class="sxs-lookup"><span data-stu-id="e6b4a-108">breakp \[!\]p0.{x\</span></span>|<span data-ttu-id="e6b4a-109">sí</span><span class="sxs-lookup"><span data-stu-id="e6b4a-109">y\</span></span>|<span data-ttu-id="e6b4a-110">z</span><span class="sxs-lookup"><span data-stu-id="e6b4a-110">z\</span></span>|<span data-ttu-id="e6b4a-111">con</span><span class="sxs-lookup"><span data-stu-id="e6b4a-111">w}</span></span> |
|-----------------------------|



 

<span data-ttu-id="e6b4a-112">Donde:</span><span class="sxs-lookup"><span data-stu-id="e6b4a-112">Where:</span></span>

-   <span data-ttu-id="e6b4a-113">\[!\] es un modificador opcional Negate.</span><span class="sxs-lookup"><span data-stu-id="e6b4a-113">\[!\] is an optional negate modifier.</span></span>
-   <span data-ttu-id="e6b4a-114">P0 es el [registro del predicado](dx9-graphics-reference-asm-ps-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="e6b4a-114">p0 is the [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md).</span></span>
-   <span data-ttu-id="e6b4a-115">{x \| y \| z \| w} es el swizzle de replicación necesario en P0.</span><span class="sxs-lookup"><span data-stu-id="e6b4a-115">{x\|y\|z\|w} is the required replicate swizzle on p0.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6b4a-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e6b4a-116">Remarks</span></span>



| <span data-ttu-id="e6b4a-117">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="e6b4a-117">Pixel shader versions</span></span> | <span data-ttu-id="e6b4a-118">1\_1</span><span class="sxs-lookup"><span data-stu-id="e6b4a-118">1\_1</span></span> | <span data-ttu-id="e6b4a-119">1\_2</span><span class="sxs-lookup"><span data-stu-id="e6b4a-119">1\_2</span></span> | <span data-ttu-id="e6b4a-120">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="e6b4a-120">1\_3</span></span> | <span data-ttu-id="e6b4a-121">1\_4</span><span class="sxs-lookup"><span data-stu-id="e6b4a-121">1\_4</span></span> | <span data-ttu-id="e6b4a-122">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e6b4a-122">2\_0</span></span> | <span data-ttu-id="e6b4a-123">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="e6b4a-123">2\_x</span></span> | <span data-ttu-id="e6b4a-124">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e6b4a-124">2\_sw</span></span> | <span data-ttu-id="e6b4a-125">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e6b4a-125">3\_0</span></span> | <span data-ttu-id="e6b4a-126">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e6b4a-126">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="e6b4a-127">breakp</span><span class="sxs-lookup"><span data-stu-id="e6b4a-127">breakp</span></span>                |      |      |      |      |      | <span data-ttu-id="e6b4a-128">x</span><span class="sxs-lookup"><span data-stu-id="e6b4a-128">x</span></span>    | <span data-ttu-id="e6b4a-129">x</span><span class="sxs-lookup"><span data-stu-id="e6b4a-129">x</span></span>     | <span data-ttu-id="e6b4a-130">x</span><span class="sxs-lookup"><span data-stu-id="e6b4a-130">x</span></span>    | <span data-ttu-id="e6b4a-131">x</span><span class="sxs-lookup"><span data-stu-id="e6b4a-131">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="e6b4a-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e6b4a-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6b4a-133">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="e6b4a-133">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




