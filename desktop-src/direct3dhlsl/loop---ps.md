---
title: bucle-PS
description: 'Inicia un bucle... ENDLOOP: bloque PS.'
ms.assetid: vs|directx_sdk|~\loop___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cf4c71641003d460e9752dcf33f983c70a82e4f6
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104077100"
---
# <a name="loop---ps"></a><span data-ttu-id="f4bce-103">bucle-PS</span><span class="sxs-lookup"><span data-stu-id="f4bce-103">loop - ps</span></span>

<span data-ttu-id="f4bce-104">Inicia un bucle... [ENDLOOP: bloque PS](endloop---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="f4bce-104">Starts a loop...[endloop - ps](endloop---ps.md) block.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4bce-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f4bce-105">Syntax</span></span>



| <span data-ttu-id="f4bce-106">bucle aL, i\#</span><span class="sxs-lookup"><span data-stu-id="f4bce-106">loop aL, i\#</span></span> |
|--------------|



 

<span data-ttu-id="f4bce-107">Donde:</span><span class="sxs-lookup"><span data-stu-id="f4bce-107">Where:</span></span>

-   <span data-ttu-id="f4bce-108">aL es el [registro del contador de bucles](dx9-graphics-reference-asm-ps-registers-loop-counter.md) que contiene el número de bucles actual.</span><span class="sxs-lookup"><span data-stu-id="f4bce-108">aL is the [Loop Counter Register](dx9-graphics-reference-asm-ps-registers-loop-counter.md) holding the current loop count.</span></span>
-   <span data-ttu-id="f4bce-109">i \# es un [registro entero constante](dx9-graphics-reference-asm-ps-registers-constant-integer.md).</span><span class="sxs-lookup"><span data-stu-id="f4bce-109">i\# is a [Constant Integer Register](dx9-graphics-reference-asm-ps-registers-constant-integer.md).</span></span> <span data-ttu-id="f4bce-110">Vea Notas.</span><span class="sxs-lookup"><span data-stu-id="f4bce-110">See remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4bce-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f4bce-111">Remarks</span></span>



| <span data-ttu-id="f4bce-112">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="f4bce-112">Pixel shader versions</span></span> | <span data-ttu-id="f4bce-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="f4bce-113">1\_1</span></span> | <span data-ttu-id="f4bce-114">1\_2</span><span class="sxs-lookup"><span data-stu-id="f4bce-114">1\_2</span></span> | <span data-ttu-id="f4bce-115">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="f4bce-115">1\_3</span></span> | <span data-ttu-id="f4bce-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="f4bce-116">1\_4</span></span> | <span data-ttu-id="f4bce-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f4bce-117">2\_0</span></span> | <span data-ttu-id="f4bce-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="f4bce-118">2\_x</span></span> | <span data-ttu-id="f4bce-119">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f4bce-119">2\_sw</span></span> | <span data-ttu-id="f4bce-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f4bce-120">3\_0</span></span> | <span data-ttu-id="f4bce-121">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f4bce-121">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="f4bce-122">bucle</span><span class="sxs-lookup"><span data-stu-id="f4bce-122">loop</span></span>                  |      |      |      |      |      |      |       | <span data-ttu-id="f4bce-123">x</span><span class="sxs-lookup"><span data-stu-id="f4bce-123">x</span></span>    | <span data-ttu-id="f4bce-124">x</span><span class="sxs-lookup"><span data-stu-id="f4bce-124">x</span></span>     |



 

-   <span data-ttu-id="f4bce-125">El [registro de contador de bucle](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (al) contiene el número de bucles actual y se puede usar para el direccionamiento relativo en el [registro de color de entrada](dx9-graphics-reference-asm-ps-registers-input-color.md) (v \# ) dentro del bloque de bucle.</span><span class="sxs-lookup"><span data-stu-id="f4bce-125">The [Loop Counter Register](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (aL) holds the current loop count and can be used for relative addressing into [Input Color Register](dx9-graphics-reference-asm-ps-registers-input-color.md) (v\#) inside the loop block.</span></span>
-   <span data-ttu-id="f4bce-126">i \# . x especifica el número de iteraciones.</span><span class="sxs-lookup"><span data-stu-id="f4bce-126">i\#.x specifies the iteration count.</span></span> <span data-ttu-id="f4bce-127">El intervalo legal es \[ 0, 255 \] .</span><span class="sxs-lookup"><span data-stu-id="f4bce-127">The legal range is \[0, 255\].</span></span> <span data-ttu-id="f4bce-128">Tenga en cuenta que esta instrucción no incrementa ni reduce el valor de i \# . x.</span><span class="sxs-lookup"><span data-stu-id="f4bce-128">Note that this instruction does not increment or decrement the value of i\#.x.</span></span>
-   <span data-ttu-id="f4bce-129">i \# . y especifica el valor inicial del registro de [contadores del bucle](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (al).</span><span class="sxs-lookup"><span data-stu-id="f4bce-129">i\#.y specifies the initial value of the [Loop Counter Register](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (aL) register.</span></span> <span data-ttu-id="f4bce-130">El intervalo legal es \[ 0, 255 \] .</span><span class="sxs-lookup"><span data-stu-id="f4bce-130">The legal range is \[0, 255\].</span></span> <span data-ttu-id="f4bce-131">Tenga en cuenta que esta instrucción no incrementa ni disminuye el valor de i \# . y.</span><span class="sxs-lookup"><span data-stu-id="f4bce-131">Note that this instruction does not increment or decrement the value of i\#.y.</span></span>
-   <span data-ttu-id="f4bce-132">i \# . z especifica el tamaño de paso/STRIDE.</span><span class="sxs-lookup"><span data-stu-id="f4bce-132">i\#.z specifies the step/stride size.</span></span> <span data-ttu-id="f4bce-133">El intervalo válido es \[ -128, 127 \] .</span><span class="sxs-lookup"><span data-stu-id="f4bce-133">The legal range is \[-128, 127\].</span></span>
-   <span data-ttu-id="f4bce-134">i \# . w no se usa en el bloque de bucle y debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="f4bce-134">i\#.w is not used by the loop block and has to be 0.</span></span>
-   <span data-ttu-id="f4bce-135">Los bloques de bucle pueden estar anidados.</span><span class="sxs-lookup"><span data-stu-id="f4bce-135">Loop blocks may be nested.</span></span> <span data-ttu-id="f4bce-136">Vea [limitaciones del control de flujo](dx9-graphics-reference-asm-ps-instructions-flow-control.md).</span><span class="sxs-lookup"><span data-stu-id="f4bce-136">See [Flow Control Limitations](dx9-graphics-reference-asm-ps-instructions-flow-control.md).</span></span>
-   <span data-ttu-id="f4bce-137">Cuando está anidado, el valor del [registro de contador de bucle](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (al) hace referencia al bloque de bucle de inclusión inmediato.</span><span class="sxs-lookup"><span data-stu-id="f4bce-137">When nested, the value of the [Loop Counter Register](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (aL) refers to the immediate enclosing loop block.</span></span>
-   <span data-ttu-id="f4bce-138">Los bloques de bucle pueden estar completamente dentro \* de un bloque if o por completo.</span><span class="sxs-lookup"><span data-stu-id="f4bce-138">Loop blocks are allowed to be either completely inside an if\* block or completely surrounding it.</span></span> <span data-ttu-id="f4bce-139">No se permite la necesidad de estar en el mismo.</span><span class="sxs-lookup"><span data-stu-id="f4bce-139">No straddling is allowed.</span></span>

## <a name="example"></a><span data-ttu-id="f4bce-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f4bce-140">Example</span></span>


```
loop aL, i3
    add r1, r0, v2[ aL ]
endloop
```



## <a name="related-topics"></a><span data-ttu-id="f4bce-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f4bce-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4bce-142">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="f4bce-142">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




