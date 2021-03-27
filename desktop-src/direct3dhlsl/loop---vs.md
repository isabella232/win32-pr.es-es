---
title: bucle-vs
description: Iniciar un bucle... bloque ENDLOOP.
ms.assetid: vs|directx_sdk|~\loop___vs.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6a96a1ce53b850ec8feeba282055e8111b275bfd
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996921"
---
# <a name="loop---vs"></a><span data-ttu-id="c593e-103">bucle-vs</span><span class="sxs-lookup"><span data-stu-id="c593e-103">loop - vs</span></span>

<span data-ttu-id="c593e-104">Iniciar un bucle... bloque [ENDLOOP](endloop---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="c593e-104">Start a loop...[endloop](endloop---vs.md) block.</span></span>

## <a name="syntax"></a><span data-ttu-id="c593e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c593e-105">Syntax</span></span>



| <span data-ttu-id="c593e-106">bucle aL, i\#</span><span class="sxs-lookup"><span data-stu-id="c593e-106">loop aL, i\#</span></span> |
|--------------|



 

<span data-ttu-id="c593e-107">Donde:</span><span class="sxs-lookup"><span data-stu-id="c593e-107">Where:</span></span>

-   <span data-ttu-id="c593e-108">aL es el [registro del contador de bucles](dx9-graphics-reference-asm-vs-registers-loop-counter.md) que contiene el número de bucles actual.</span><span class="sxs-lookup"><span data-stu-id="c593e-108">aL is the [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) holding the current loop count.</span></span>
-   <span data-ttu-id="c593e-109">i \# es un [registro entero constante](dx9-graphics-reference-asm-vs-registers-constant-integer.md).</span><span class="sxs-lookup"><span data-stu-id="c593e-109">i\# is a [Constant Integer Register](dx9-graphics-reference-asm-vs-registers-constant-integer.md).</span></span> <span data-ttu-id="c593e-110">Vea Notas.</span><span class="sxs-lookup"><span data-stu-id="c593e-110">See remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="c593e-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c593e-111">Remarks</span></span>



| <span data-ttu-id="c593e-112">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="c593e-112">Vertex shader versions</span></span> | <span data-ttu-id="c593e-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="c593e-113">1\_1</span></span> | <span data-ttu-id="c593e-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c593e-114">2\_0</span></span> | <span data-ttu-id="c593e-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c593e-115">2\_x</span></span> | <span data-ttu-id="c593e-116">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c593e-116">2\_sw</span></span> | <span data-ttu-id="c593e-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c593e-117">3\_0</span></span> | <span data-ttu-id="c593e-118">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c593e-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="c593e-119">bucle</span><span class="sxs-lookup"><span data-stu-id="c593e-119">loop</span></span>                   |      | <span data-ttu-id="c593e-120">x</span><span class="sxs-lookup"><span data-stu-id="c593e-120">x</span></span>    | <span data-ttu-id="c593e-121">x</span><span class="sxs-lookup"><span data-stu-id="c593e-121">x</span></span>    | <span data-ttu-id="c593e-122">x</span><span class="sxs-lookup"><span data-stu-id="c593e-122">x</span></span>     | <span data-ttu-id="c593e-123">x</span><span class="sxs-lookup"><span data-stu-id="c593e-123">x</span></span>    | <span data-ttu-id="c593e-124">x</span><span class="sxs-lookup"><span data-stu-id="c593e-124">x</span></span>     |



 

-   <span data-ttu-id="c593e-125">El [registro de contador de bucle](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (al) contiene el recuento de bucles actual y se puede usar para el direccionamiento relativo en el [registro de enteros constante](dx9-graphics-reference-asm-vs-registers-constant-integer.md) (c \# ) o los [registros de salida](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) (o \# ) dentro del bloque de bucle.</span><span class="sxs-lookup"><span data-stu-id="c593e-125">The [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL) holds the current loop count, and can be used for relative addressing into [Constant Integer Register](dx9-graphics-reference-asm-vs-registers-constant-integer.md) (c\#) or [Output Registers](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) (o\#) inside the loop block.</span></span>
-   <span data-ttu-id="c593e-126">i \# . x especifica el número de iteraciones.</span><span class="sxs-lookup"><span data-stu-id="c593e-126">i\#.x specifies the iteration count.</span></span> <span data-ttu-id="c593e-127">El intervalo legal es \[ 0, 255 \] .</span><span class="sxs-lookup"><span data-stu-id="c593e-127">The legal range is \[0, 255\].</span></span> <span data-ttu-id="c593e-128">Tenga en cuenta que esta instrucción no incrementa ni reduce el valor de i \# . x.</span><span class="sxs-lookup"><span data-stu-id="c593e-128">Note that this instruction does not increment or decrement the value of i\#.x.</span></span>
-   <span data-ttu-id="c593e-129">i \# . y especifica el valor inicial del registro de [contadores del bucle](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (al).</span><span class="sxs-lookup"><span data-stu-id="c593e-129">i\#.y specifies the initial value of the [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL) register.</span></span> <span data-ttu-id="c593e-130">El intervalo legal es \[ 0, 255 \] .</span><span class="sxs-lookup"><span data-stu-id="c593e-130">The legal range is \[0, 255\].</span></span> <span data-ttu-id="c593e-131">Tenga en cuenta que esta instrucción no incrementa ni disminuye el valor de i \# . y.</span><span class="sxs-lookup"><span data-stu-id="c593e-131">Note that this instruction does not increment or decrement the value of i\#.y.</span></span>
-   <span data-ttu-id="c593e-132">i \# . z especifica el tamaño de paso/STRIDE.</span><span class="sxs-lookup"><span data-stu-id="c593e-132">i\#.z specifies the step/stride size.</span></span> <span data-ttu-id="c593e-133">El intervalo válido es \[ -128, 127 \] .</span><span class="sxs-lookup"><span data-stu-id="c593e-133">The legal range is \[-128, 127\].</span></span>
-   <span data-ttu-id="c593e-134">i \# . w no se utiliza y debe establecerse en 0.</span><span class="sxs-lookup"><span data-stu-id="c593e-134">i\#.w is not used and must be set to 0.</span></span>
-   <span data-ttu-id="c593e-135">Los bloques de bucle pueden estar anidados.</span><span class="sxs-lookup"><span data-stu-id="c593e-135">Loop blocks may be nested.</span></span> <span data-ttu-id="c593e-136">Consulte [límites de anidamiento de control de flujo](dx9-graphics-reference-asm-vs-instructions-flow-control.md).</span><span class="sxs-lookup"><span data-stu-id="c593e-136">See [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md).</span></span>
-   <span data-ttu-id="c593e-137">Cuando está anidado, el valor del [registro de contador de bucle](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (al) hace referencia al bloque de bucle de inclusión inmediato.</span><span class="sxs-lookup"><span data-stu-id="c593e-137">When nested, the value of the [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL) refers to the immediate enclosing loop block.</span></span>
-   <span data-ttu-id="c593e-138">Los bloques de bucle pueden estar completamente dentro \* de un bloque if o por completo.</span><span class="sxs-lookup"><span data-stu-id="c593e-138">Loop blocks are allowed to be either completely inside an if\* block or completely surrounding it.</span></span> <span data-ttu-id="c593e-139">No se permite la necesidad de estar en el mismo.</span><span class="sxs-lookup"><span data-stu-id="c593e-139">No straddling is allowed.</span></span>

## <a name="example"></a><span data-ttu-id="c593e-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c593e-140">Example</span></span>


```
loop aL, i3
    add r1, r0, c2[aL]
endloop
```



## <a name="related-topics"></a><span data-ttu-id="c593e-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c593e-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c593e-142">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="c593e-142">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




