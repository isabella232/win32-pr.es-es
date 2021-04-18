---
title: REP-vs
description: Iniciar un representante... bloque endrep.
ms.assetid: vs|directx_sdk|~\rep___vs.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5441d5d134ee2d60e14db9f273ec374323f93902
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419917"
---
# <a name="rep---vs"></a><span data-ttu-id="f1286-103">REP-vs</span><span class="sxs-lookup"><span data-stu-id="f1286-103">rep - vs</span></span>

<span data-ttu-id="f1286-104">Iniciar un representante... bloque [endrep](endrep---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="f1286-104">Start a rep...[endrep](endrep---vs.md) block.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1286-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f1286-105">Syntax</span></span>



| <span data-ttu-id="f1286-106">REP i\#</span><span class="sxs-lookup"><span data-stu-id="f1286-106">rep i\#</span></span> |
|---------|



 

<span data-ttu-id="f1286-107">donde i \# es un registro entero que especifica el número de repeticiones en el componente. x.</span><span class="sxs-lookup"><span data-stu-id="f1286-107">where i\# is an integer register that specifies the repeat count in the .x component.</span></span> <span data-ttu-id="f1286-108">Vea [registro de entero constante](dx9-graphics-reference-asm-vs-registers-constant-integer.md).</span><span class="sxs-lookup"><span data-stu-id="f1286-108">See [Constant Integer Register](dx9-graphics-reference-asm-vs-registers-constant-integer.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f1286-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f1286-109">Remarks</span></span>



| <span data-ttu-id="f1286-110">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="f1286-110">Vertex shader versions</span></span> | <span data-ttu-id="f1286-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="f1286-111">1\_1</span></span> | <span data-ttu-id="f1286-112">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f1286-112">2\_0</span></span> | <span data-ttu-id="f1286-113">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="f1286-113">2\_x</span></span> | <span data-ttu-id="f1286-114">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f1286-114">2\_sw</span></span> | <span data-ttu-id="f1286-115">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f1286-115">3\_0</span></span> | <span data-ttu-id="f1286-116">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f1286-116">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="f1286-117">Selecc</span><span class="sxs-lookup"><span data-stu-id="f1286-117">rep</span></span>                    |      | <span data-ttu-id="f1286-118">x</span><span class="sxs-lookup"><span data-stu-id="f1286-118">x</span></span>    | <span data-ttu-id="f1286-119">x</span><span class="sxs-lookup"><span data-stu-id="f1286-119">x</span></span>    | <span data-ttu-id="f1286-120">x</span><span class="sxs-lookup"><span data-stu-id="f1286-120">x</span></span>     | <span data-ttu-id="f1286-121">x</span><span class="sxs-lookup"><span data-stu-id="f1286-121">x</span></span>    | <span data-ttu-id="f1286-122">x</span><span class="sxs-lookup"><span data-stu-id="f1286-122">x</span></span>     |



 

-   <span data-ttu-id="f1286-123">i \# . x especifica el número de iteraciones.</span><span class="sxs-lookup"><span data-stu-id="f1286-123">i\#.x specifies the iteration count.</span></span> <span data-ttu-id="f1286-124">El intervalo legal es \[ 0, 255 \] .</span><span class="sxs-lookup"><span data-stu-id="f1286-124">The legal range is \[0, 255\].</span></span> <span data-ttu-id="f1286-125">Tenga en cuenta que esta instrucción no incrementa ni reduce el valor de i \# . x.</span><span class="sxs-lookup"><span data-stu-id="f1286-125">Note that this instruction does not increment or decrement the value of i\#.x.</span></span>
-   <span data-ttu-id="f1286-126">i \# . YZW no se usa en el bloque REPEAT.</span><span class="sxs-lookup"><span data-stu-id="f1286-126">i\#.yzw are not used by the repeat block.</span></span>
-   <span data-ttu-id="f1286-127">Los bloques de repetición pueden estar anidados.</span><span class="sxs-lookup"><span data-stu-id="f1286-127">Repeat blocks may be nested.</span></span> <span data-ttu-id="f1286-128">Consulte [límites de anidamiento de control de flujo](dx9-graphics-reference-asm-vs-instructions-flow-control.md).</span><span class="sxs-lookup"><span data-stu-id="f1286-128">See [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md).</span></span>
-   <span data-ttu-id="f1286-129">Los bloques de repetición pueden estar completamente dentro \* de un bloque if o por completo.</span><span class="sxs-lookup"><span data-stu-id="f1286-129">Repeat blocks are allowed to be either completely inside an if\* block or completely surrounding it.</span></span> <span data-ttu-id="f1286-130">No se permite la necesidad de estar en el mismo.</span><span class="sxs-lookup"><span data-stu-id="f1286-130">No straddling is allowed.</span></span>
-   <span data-ttu-id="f1286-131">El uso de la misma \# instrucción i para instrucciones de representación diferentes o anidadas es correcto: cada bucle se iterará en función del recuento especificado.</span><span class="sxs-lookup"><span data-stu-id="f1286-131">Using the same i\# for different or nested rep instructions is fine - each loop will iterate based on the specified count.</span></span>

## <a name="example"></a><span data-ttu-id="f1286-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f1286-132">Example</span></span>


```
rep i2
    add r0, r0, c0
endrep  
```



## <a name="related-topics"></a><span data-ttu-id="f1286-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f1286-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1286-134">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="f1286-134">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




