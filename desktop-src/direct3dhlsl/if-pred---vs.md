---
title: Si Pred-vs
description: 'Inicio de una en caso de Pred-vs... Else-vs... endif: bloque de vs, con la condición tomada del contenido del registro de predicado.'
ms.assetid: 03f60ca3-cda0-4653-8582-74d1a75e0aee
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0a1a36bb0c6c68f5132757719bbc7e37fbc71501
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104358472"
---
# <a name="if-pred---vs"></a><span data-ttu-id="c820a-103">Si Pred-vs</span><span class="sxs-lookup"><span data-stu-id="c820a-103">if pred - vs</span></span>

<span data-ttu-id="c820a-104">Inicio de una en caso de Pred-vs... [else-vs](else---vs.md)... [endif:](endif---vs.md) bloque de vs, con la condición tomada del contenido del registro de predicado.</span><span class="sxs-lookup"><span data-stu-id="c820a-104">Start of an if pred - vs...[else - vs](else---vs.md)...[endif - vs](endif---vs.md) block, with the condition taken from the content of the predicate register.</span></span>

## <a name="syntax"></a><span data-ttu-id="c820a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c820a-105">Syntax</span></span>



| <span data-ttu-id="c820a-106">Si \[ ! \] Pred. replicateSwizzle</span><span class="sxs-lookup"><span data-stu-id="c820a-106">if \[!\]pred.replicateSwizzle</span></span> |
|-------------------------------|



 

<span data-ttu-id="c820a-107">Donde:</span><span class="sxs-lookup"><span data-stu-id="c820a-107">Where:</span></span>

-   <span data-ttu-id="c820a-108">\[!\] un modificador NOT opcional.</span><span class="sxs-lookup"><span data-stu-id="c820a-108">\[!\] an optional NOT modifier.</span></span> <span data-ttu-id="c820a-109">Esto modifica el valor en el registro del predicado.</span><span class="sxs-lookup"><span data-stu-id="c820a-109">This modifies the value in the predicate register.</span></span>
-   <span data-ttu-id="c820a-110">Pred es el registro de predicado, P0.</span><span class="sxs-lookup"><span data-stu-id="c820a-110">pred is the predicate register, p0.</span></span> <span data-ttu-id="c820a-111">Vea [registro de predicados](dx9-graphics-reference-asm-vs-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="c820a-111">See [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md).</span></span>
-   <span data-ttu-id="c820a-112">replicateSwizzle es un componente único que se copia (o se replica) en los cuatro componentes (swizzled).</span><span class="sxs-lookup"><span data-stu-id="c820a-112">replicateSwizzle is a single component that is copied (or replicated) to all four components (swizzled).</span></span> <span data-ttu-id="c820a-113">Los componentes válidos son: x, y, z, w o r, g, b, a.</span><span class="sxs-lookup"><span data-stu-id="c820a-113">Valid components are: x, y, z, w or r, g, b, a.</span></span>

## <a name="remarks"></a><span data-ttu-id="c820a-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c820a-114">Remarks</span></span>



| <span data-ttu-id="c820a-115">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="c820a-115">Vertex shader versions</span></span> | <span data-ttu-id="c820a-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="c820a-116">1\_1</span></span> | <span data-ttu-id="c820a-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c820a-117">2\_0</span></span> | <span data-ttu-id="c820a-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c820a-118">2\_x</span></span> | <span data-ttu-id="c820a-119">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c820a-119">2\_sw</span></span> | <span data-ttu-id="c820a-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c820a-120">3\_0</span></span> | <span data-ttu-id="c820a-121">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c820a-121">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="c820a-122">Si es Pred</span><span class="sxs-lookup"><span data-stu-id="c820a-122">if pred</span></span>                |      |      | <span data-ttu-id="c820a-123">x</span><span class="sxs-lookup"><span data-stu-id="c820a-123">x</span></span>    | <span data-ttu-id="c820a-124">x</span><span class="sxs-lookup"><span data-stu-id="c820a-124">x</span></span>     | <span data-ttu-id="c820a-125">x</span><span class="sxs-lookup"><span data-stu-id="c820a-125">x</span></span>    | <span data-ttu-id="c820a-126">x</span><span class="sxs-lookup"><span data-stu-id="c820a-126">x</span></span>     |



 

<span data-ttu-id="c820a-127">Esta instrucción se usa para omitir un bloque de código, basado en un canal del registro del predicado.</span><span class="sxs-lookup"><span data-stu-id="c820a-127">This instruction is used to skip a block of code, based on a channel of the predicate register.</span></span> <span data-ttu-id="c820a-128">Cada si el \_ bloque Pred debe terminar con una instrucción else o endif.</span><span class="sxs-lookup"><span data-stu-id="c820a-128">Each if\_pred block must end with an else or endif instruction.</span></span>

<span data-ttu-id="c820a-129">Entre las restricciones se incluyen:</span><span class="sxs-lookup"><span data-stu-id="c820a-129">Restrictions include:</span></span>

<span data-ttu-id="c820a-130">Si \_ se pueden anidar los bloques pred.</span><span class="sxs-lookup"><span data-stu-id="c820a-130">if\_pred blocks can be nested.</span></span> <span data-ttu-id="c820a-131">Cuenta con la profundidad de anidamiento dinámica total junto con los bloques de [ \_ COMP if](if-comp---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="c820a-131">This counts to the total dynamic nesting depth along with [if\_comp](if-comp---vs.md) blocks.</span></span>

<span data-ttu-id="c820a-132">Un \_ bloque if Pred no puede ocupar un bloque de bucle, debe estar completamente dentro de él o encerrarlo.</span><span class="sxs-lookup"><span data-stu-id="c820a-132">An if\_pred block cannot straddle a loop block, it should be either completely inside it or surround it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c820a-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c820a-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c820a-134">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="c820a-134">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




