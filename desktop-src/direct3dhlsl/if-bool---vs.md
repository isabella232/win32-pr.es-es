---
title: Si es bool-vs
description: Inicia una... otra cosa... bloque endif-vs.
ms.assetid: d77e2f81-400c-4997-9c34-426b6e6f47be
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 261ff572cbaf519cc0099f3ab68d1a0becca706f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104077066"
---
# <a name="if-bool---vs"></a><span data-ttu-id="aa251-103">Si es bool-vs</span><span class="sxs-lookup"><span data-stu-id="aa251-103">if bool - vs</span></span>

<span data-ttu-id="aa251-104">Inicia una... [otra cosa](else---vs.md)... bloque [endif-vs](endif---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="aa251-104">Starts an if...[else](else---vs.md)...[endif - vs](endif---vs.md) block.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa251-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aa251-105">Syntax</span></span>



| <span data-ttu-id="aa251-106">Si es bool</span><span class="sxs-lookup"><span data-stu-id="aa251-106">if bool</span></span> |
|---------|



 

<span data-ttu-id="aa251-107">donde bool es un número de registro bool.</span><span class="sxs-lookup"><span data-stu-id="aa251-107">where bool is a bool register number.</span></span> <span data-ttu-id="aa251-108">Vea [registro booleano constante](dx9-graphics-reference-asm-vs-registers-constant-boolean.md).</span><span class="sxs-lookup"><span data-stu-id="aa251-108">See [Constant Boolean Register](dx9-graphics-reference-asm-vs-registers-constant-boolean.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="aa251-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aa251-109">Remarks</span></span>



| <span data-ttu-id="aa251-110">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="aa251-110">Vertex shader versions</span></span> | <span data-ttu-id="aa251-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="aa251-111">1\_1</span></span> | <span data-ttu-id="aa251-112">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="aa251-112">2\_0</span></span> | <span data-ttu-id="aa251-113">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="aa251-113">2\_x</span></span> | <span data-ttu-id="aa251-114">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="aa251-114">2\_sw</span></span> | <span data-ttu-id="aa251-115">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="aa251-115">3\_0</span></span> | <span data-ttu-id="aa251-116">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="aa251-116">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="aa251-117">Si es bool</span><span class="sxs-lookup"><span data-stu-id="aa251-117">if bool</span></span>                |      | <span data-ttu-id="aa251-118">x</span><span class="sxs-lookup"><span data-stu-id="aa251-118">x</span></span>    | <span data-ttu-id="aa251-119">x</span><span class="sxs-lookup"><span data-stu-id="aa251-119">x</span></span>    | <span data-ttu-id="aa251-120">x</span><span class="sxs-lookup"><span data-stu-id="aa251-120">x</span></span>     | <span data-ttu-id="aa251-121">x</span><span class="sxs-lookup"><span data-stu-id="aa251-121">x</span></span>    | <span data-ttu-id="aa251-122">x</span><span class="sxs-lookup"><span data-stu-id="aa251-122">x</span></span>     |



 

<span data-ttu-id="aa251-123">Si el registro booleano de origen en la instrucción if es true, se ejecuta el código incluido entre la instrucción if y la otra que coincide.</span><span class="sxs-lookup"><span data-stu-id="aa251-123">If the source Boolean register in the if statement is true, the code enclosed by the if statement and the matching else is run.</span></span> <span data-ttu-id="aa251-124">De lo contrario, el código delimitado por el bloque [else](else---vs.md)... se ejecutan las instrucciones [endif-vs](endif---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="aa251-124">Otherwise, the code enclosed by the [else](else---vs.md)...[endif - vs](endif---vs.md) statements is run.</span></span> <span data-ttu-id="aa251-125">Esta instrucción usa una ranura de instrucción.</span><span class="sxs-lookup"><span data-stu-id="aa251-125">This instruction consumes one instruction slot.</span></span>

<span data-ttu-id="aa251-126">Si los bloques se pueden anidar.</span><span class="sxs-lookup"><span data-stu-id="aa251-126">if blocks can be nested.</span></span>

<span data-ttu-id="aa251-127">Un bloque If no puede ocupar un bloque de bucle.</span><span class="sxs-lookup"><span data-stu-id="aa251-127">An if block cannot straddle a loop block.</span></span>

## <a name="example"></a><span data-ttu-id="aa251-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="aa251-128">Example</span></span>

<span data-ttu-id="aa251-129">Esta instrucción proporciona el control de flujo estático condicional.</span><span class="sxs-lookup"><span data-stu-id="aa251-129">This instruction provides conditional static flow control.</span></span>


```
defb b2, TRUE

...

if b2
// Instructions to run if b2 is nonzero

else
// Instructions to run otherwise

endif
```



## <a name="related-topics"></a><span data-ttu-id="aa251-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="aa251-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa251-131">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="aa251-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[<span data-ttu-id="aa251-132">Else-vs</span><span class="sxs-lookup"><span data-stu-id="aa251-132">else - vs</span></span>](else---vs.md)
</dt> <dt>

[<span data-ttu-id="aa251-133">endif-vs</span><span class="sxs-lookup"><span data-stu-id="aa251-133">endif - vs</span></span>](endif---vs.md)
</dt> </dl>

 

 




