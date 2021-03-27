---
title: Si Pred-PS
description: Inicio de una expresión if bool-PS... Else-PS... bloque endif-PS, con la condición tomada del contenido del registro de predicado.
ms.assetid: 7b43bf71-a2e9-468f-805f-620de065db08
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ead7c5936550715d48ee1ef6a3938b6219558823
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103784912"
---
# <a name="if-pred---ps"></a><span data-ttu-id="e9b9f-103">Si Pred-PS</span><span class="sxs-lookup"><span data-stu-id="e9b9f-103">if pred - ps</span></span>

<span data-ttu-id="e9b9f-104">Inicio de una expresión [If bool-PS](if-bool---ps.md)... [else-PS](else---ps.md)... bloque [endif-PS](endif---ps.md) , con la condición tomada del contenido del registro de predicado.</span><span class="sxs-lookup"><span data-stu-id="e9b9f-104">Start of an [if bool - ps](if-bool---ps.md)...[else - ps](else---ps.md)...[endif - ps](endif---ps.md) block, with the condition taken from the content of the predicate register.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9b9f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e9b9f-105">Syntax</span></span>



| <span data-ttu-id="e9b9f-106">Si \[ ! \] Pred. replicateSwizzle</span><span class="sxs-lookup"><span data-stu-id="e9b9f-106">if \[!\]pred.replicateSwizzle</span></span> |
|-------------------------------|



 

<span data-ttu-id="e9b9f-107">Donde:</span><span class="sxs-lookup"><span data-stu-id="e9b9f-107">Where:</span></span>

-   <span data-ttu-id="e9b9f-108">\[!\] es un modificador NOT opcional.</span><span class="sxs-lookup"><span data-stu-id="e9b9f-108">\[!\] is an optional NOT modifier.</span></span> <span data-ttu-id="e9b9f-109">Esto modifica el valor en el registro del predicado.</span><span class="sxs-lookup"><span data-stu-id="e9b9f-109">This modifies the value in the predicate register.</span></span>
-   <span data-ttu-id="e9b9f-110">Pred es el [registro del predicado](dx9-graphics-reference-asm-ps-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="e9b9f-110">pred is the [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md).</span></span>
-   <span data-ttu-id="e9b9f-111">replicateSwizzle es un componente único que se copia (o se replica) en los cuatro componentes (swizzled).</span><span class="sxs-lookup"><span data-stu-id="e9b9f-111">replicateSwizzle is a single component that is copied (or replicated) to all four components (swizzled).</span></span> <span data-ttu-id="e9b9f-112">Los componentes válidos son: \[ x, y, z, w \] o \[ r, g, b, a \] .</span><span class="sxs-lookup"><span data-stu-id="e9b9f-112">Valid components are: \[x, y, z, w\] or \[r, g, b, a\].</span></span>

## <a name="remarks"></a><span data-ttu-id="e9b9f-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e9b9f-113">Remarks</span></span>



| <span data-ttu-id="e9b9f-114">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="e9b9f-114">Pixel shader versions</span></span> | <span data-ttu-id="e9b9f-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="e9b9f-115">1\_1</span></span> | <span data-ttu-id="e9b9f-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="e9b9f-116">1\_2</span></span> | <span data-ttu-id="e9b9f-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="e9b9f-117">1\_3</span></span> | <span data-ttu-id="e9b9f-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="e9b9f-118">1\_4</span></span> | <span data-ttu-id="e9b9f-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e9b9f-119">2\_0</span></span> | <span data-ttu-id="e9b9f-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="e9b9f-120">2\_x</span></span> | <span data-ttu-id="e9b9f-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e9b9f-121">2\_sw</span></span> | <span data-ttu-id="e9b9f-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e9b9f-122">3\_0</span></span> | <span data-ttu-id="e9b9f-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e9b9f-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="e9b9f-124">Si es \_ Pred</span><span class="sxs-lookup"><span data-stu-id="e9b9f-124">if\_pred</span></span>              |      |      |      |      |      | <span data-ttu-id="e9b9f-125">x</span><span class="sxs-lookup"><span data-stu-id="e9b9f-125">x</span></span>    | <span data-ttu-id="e9b9f-126">x</span><span class="sxs-lookup"><span data-stu-id="e9b9f-126">x</span></span>     | <span data-ttu-id="e9b9f-127">x</span><span class="sxs-lookup"><span data-stu-id="e9b9f-127">x</span></span>    | <span data-ttu-id="e9b9f-128">x</span><span class="sxs-lookup"><span data-stu-id="e9b9f-128">x</span></span>     |



 

<span data-ttu-id="e9b9f-129">Esta instrucción se usa para omitir un bloque de código, basado en un canal del registro del predicado.</span><span class="sxs-lookup"><span data-stu-id="e9b9f-129">This instruction is used to skip a block of code, based on a channel of the predicate register.</span></span> <span data-ttu-id="e9b9f-130">Cada si el \_ bloque Pred debe terminar con una instrucción [else-PS](else---ps.md) o [endif-PS](endif---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="e9b9f-130">Each if\_pred block must end with an [else - ps](else---ps.md) or [endif - ps](endif---ps.md) instruction.</span></span>

<span data-ttu-id="e9b9f-131">Entre las restricciones se incluyen:</span><span class="sxs-lookup"><span data-stu-id="e9b9f-131">Restrictions include:</span></span>

<span data-ttu-id="e9b9f-132">Si \_ se pueden anidar los bloques pred.</span><span class="sxs-lookup"><span data-stu-id="e9b9f-132">if\_pred blocks can be nested.</span></span> <span data-ttu-id="e9b9f-133">Cuenta con la profundidad de anidamiento dinámica total junto con los bloques de [ \_ COMP if](if-comp---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="e9b9f-133">This counts to the total dynamic nesting depth along with [if\_comp](if-comp---ps.md) blocks.</span></span>

<span data-ttu-id="e9b9f-134">Un \_ bloque if Pred no puede ocupar un bloque de bucle; debe estar completamente dentro o delimitarlo.</span><span class="sxs-lookup"><span data-stu-id="e9b9f-134">An if\_pred block cannot straddle a loop block; it should either be completely inside it or surround it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e9b9f-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e9b9f-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9b9f-136">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="e9b9f-136">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




