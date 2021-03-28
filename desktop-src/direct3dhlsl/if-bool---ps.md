---
title: Si es bool-PS
description: Inicio de un bloque if.
ms.assetid: cff53072-1c73-4cf8-9ecd-11032a9c4bbb
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 92c3158a09aeb871ef367133c07278b0f3b87390
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103784889"
---
# <a name="if-bool---ps"></a><span data-ttu-id="dde70-103">Si es bool-PS</span><span class="sxs-lookup"><span data-stu-id="dde70-103">if bool - ps</span></span>

<span data-ttu-id="dde70-104">Inicio de un bloque if.</span><span class="sxs-lookup"><span data-stu-id="dde70-104">Start of an if block.</span></span>

## <a name="syntax"></a><span data-ttu-id="dde70-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dde70-105">Syntax</span></span>



| <span data-ttu-id="dde70-106">Si es bool</span><span class="sxs-lookup"><span data-stu-id="dde70-106">if bool</span></span> |
|---------|



 

<span data-ttu-id="dde70-107">Donde:</span><span class="sxs-lookup"><span data-stu-id="dde70-107">Where:</span></span>

-   <span data-ttu-id="dde70-108">bool es un número de registro booleano (booleano).</span><span class="sxs-lookup"><span data-stu-id="dde70-108">bool is a bool (Boolean) register number.</span></span> <span data-ttu-id="dde70-109">Vea [registro booleano constante](dx9-graphics-reference-asm-ps-registers-constant-boolean.md).</span><span class="sxs-lookup"><span data-stu-id="dde70-109">See [Constant Boolean Register](dx9-graphics-reference-asm-ps-registers-constant-boolean.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="dde70-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dde70-110">Remarks</span></span>



| <span data-ttu-id="dde70-111">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="dde70-111">Pixel shader versions</span></span> | <span data-ttu-id="dde70-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="dde70-112">1\_1</span></span> | <span data-ttu-id="dde70-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="dde70-113">1\_2</span></span> | <span data-ttu-id="dde70-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="dde70-114">1\_3</span></span> | <span data-ttu-id="dde70-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="dde70-115">1\_4</span></span> | <span data-ttu-id="dde70-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="dde70-116">2\_0</span></span> | <span data-ttu-id="dde70-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="dde70-117">2\_x</span></span> | <span data-ttu-id="dde70-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="dde70-118">2\_sw</span></span> | <span data-ttu-id="dde70-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="dde70-119">3\_0</span></span> | <span data-ttu-id="dde70-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="dde70-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="dde70-121">Si es bool</span><span class="sxs-lookup"><span data-stu-id="dde70-121">if bool</span></span>               |      |      |      |      |      | <span data-ttu-id="dde70-122">x</span><span class="sxs-lookup"><span data-stu-id="dde70-122">x</span></span>    | <span data-ttu-id="dde70-123">x</span><span class="sxs-lookup"><span data-stu-id="dde70-123">x</span></span>     | <span data-ttu-id="dde70-124">x</span><span class="sxs-lookup"><span data-stu-id="dde70-124">x</span></span>    | <span data-ttu-id="dde70-125">x</span><span class="sxs-lookup"><span data-stu-id="dde70-125">x</span></span>     |



 

<span data-ttu-id="dde70-126">Si el registro de valor booleano de origen en la instrucción if es true, se ejecuta el código incluido entre la instrucción if y el [endif-PS](endif---ps.md) correspondiente, o bien el [PS](else---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="dde70-126">If the source Boolean register in the if statement is true, the code enclosed by the if statement and the matching [endif - ps](endif---ps.md) or [else - ps](else---ps.md) is executed.</span></span> <span data-ttu-id="dde70-127">De lo contrario, el código incluido en el bloque else-PS... se ejecutan las instrucciones endif-PS.</span><span class="sxs-lookup"><span data-stu-id="dde70-127">Otherwise, the code enclosed by the else - ps...endif - ps statements is executed.</span></span> <span data-ttu-id="dde70-128">Esta instrucción usa una ranura de instrucción.</span><span class="sxs-lookup"><span data-stu-id="dde70-128">This instruction consumes one instruction slot.</span></span>

<span data-ttu-id="dde70-129">Un bloque if se puede anidar.</span><span class="sxs-lookup"><span data-stu-id="dde70-129">An if block can be nested.</span></span>

<span data-ttu-id="dde70-130">Un bloque If no puede ocupar un bloque de bucle.</span><span class="sxs-lookup"><span data-stu-id="dde70-130">An if block cannot straddle a loop block.</span></span>

<span data-ttu-id="dde70-131">Un bloque if puede ir seguido de un bloque de instrucciones y/o una instrucción [else-PS](else---ps.md) , y/o una instrucción [endif-PS](endif---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="dde70-131">An if block can be followed by a statement block, and/or an [else - ps](else---ps.md) instruction, and/or an [endif - ps](endif---ps.md) instruction.</span></span>

## <a name="example"></a><span data-ttu-id="dde70-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dde70-132">Example</span></span>

<span data-ttu-id="dde70-133">Esta instrucción proporciona el control de flujo estático condicional.</span><span class="sxs-lookup"><span data-stu-id="dde70-133">This instruction provides conditional static flow control.</span></span>


```
defb b3, true

if b3
// Instructions to run if b3 is nonzero
else
// Instructions to run otherwise
endif
```



## <a name="related-topics"></a><span data-ttu-id="dde70-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dde70-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dde70-135">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="dde70-135">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[<span data-ttu-id="dde70-136">Else-PS</span><span class="sxs-lookup"><span data-stu-id="dde70-136">else - ps</span></span>](else---ps.md)
</dt> <dt>

[<span data-ttu-id="dde70-137">endif-PS</span><span class="sxs-lookup"><span data-stu-id="dde70-137">endif - ps</span></span>](endif---ps.md)
</dt> </dl>

 

 




