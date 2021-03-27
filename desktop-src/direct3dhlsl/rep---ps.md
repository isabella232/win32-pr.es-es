---
title: REP-PS
description: 'Iniciar un representante... endrep: bloque PS.'
ms.assetid: vs|directx_sdk|~\rep___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a6873a6aee9e31b1f28ba2755b1869cddb177306
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103784924"
---
# <a name="rep---ps"></a><span data-ttu-id="3946a-103">REP-PS</span><span class="sxs-lookup"><span data-stu-id="3946a-103">rep - ps</span></span>

<span data-ttu-id="3946a-104">Iniciar un representante... [endrep: bloque PS](endrep---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="3946a-104">Start a rep...[endrep - ps](endrep---ps.md) block.</span></span>

## <a name="syntax"></a><span data-ttu-id="3946a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3946a-105">Syntax</span></span>



| <span data-ttu-id="3946a-106">REP i\#</span><span class="sxs-lookup"><span data-stu-id="3946a-106">rep i\#</span></span> |
|---------|



 

<span data-ttu-id="3946a-107">donde i \# es un registro entero que especifica el número de repeticiones en el componente. x.</span><span class="sxs-lookup"><span data-stu-id="3946a-107">where i\# is an integer register that specifies the repeat count in the .x component.</span></span> <span data-ttu-id="3946a-108">Vea [registro de entero constante](dx9-graphics-reference-asm-ps-registers-constant-integer.md).</span><span class="sxs-lookup"><span data-stu-id="3946a-108">See [Constant Integer Register](dx9-graphics-reference-asm-ps-registers-constant-integer.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3946a-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3946a-109">Remarks</span></span>



| <span data-ttu-id="3946a-110">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="3946a-110">Pixel shader versions</span></span> | <span data-ttu-id="3946a-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="3946a-111">1\_1</span></span> | <span data-ttu-id="3946a-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="3946a-112">1\_2</span></span> | <span data-ttu-id="3946a-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="3946a-113">1\_3</span></span> | <span data-ttu-id="3946a-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="3946a-114">1\_4</span></span> | <span data-ttu-id="3946a-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3946a-115">2\_0</span></span> | <span data-ttu-id="3946a-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="3946a-116">2\_x</span></span> | <span data-ttu-id="3946a-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3946a-117">2\_sw</span></span> | <span data-ttu-id="3946a-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3946a-118">3\_0</span></span> | <span data-ttu-id="3946a-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3946a-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="3946a-120">Selecc</span><span class="sxs-lookup"><span data-stu-id="3946a-120">rep</span></span>                   |      |      |      |      |      | <span data-ttu-id="3946a-121">x</span><span class="sxs-lookup"><span data-stu-id="3946a-121">x</span></span>    | <span data-ttu-id="3946a-122">x</span><span class="sxs-lookup"><span data-stu-id="3946a-122">x</span></span>     | <span data-ttu-id="3946a-123">x</span><span class="sxs-lookup"><span data-stu-id="3946a-123">x</span></span>    | <span data-ttu-id="3946a-124">x</span><span class="sxs-lookup"><span data-stu-id="3946a-124">x</span></span>     |



 

-   <span data-ttu-id="3946a-125">i \# . x especifica el número de iteraciones.</span><span class="sxs-lookup"><span data-stu-id="3946a-125">i\#.x specifies the iteration count.</span></span> <span data-ttu-id="3946a-126">El intervalo legal es \[ 0, 255 \] .</span><span class="sxs-lookup"><span data-stu-id="3946a-126">The legal range is \[0, 255\].</span></span> <span data-ttu-id="3946a-127">Tenga en cuenta que esta instrucción no incrementa ni reduce el valor de i \# . x.</span><span class="sxs-lookup"><span data-stu-id="3946a-127">Note that this instruction does not increment or decrement the value of i\#.x.</span></span>
-   <span data-ttu-id="3946a-128">i \# . YZW no se usa en el bloque REPEAT.</span><span class="sxs-lookup"><span data-stu-id="3946a-128">i\#.yzw are not used by the repeat block.</span></span>
-   <span data-ttu-id="3946a-129">Los bloques de repetición pueden estar anidados.</span><span class="sxs-lookup"><span data-stu-id="3946a-129">Repeat blocks may be nested.</span></span> <span data-ttu-id="3946a-130">Vea [limitaciones del control de flujo](dx9-graphics-reference-asm-ps-instructions-flow-control.md).</span><span class="sxs-lookup"><span data-stu-id="3946a-130">See [Flow Control Limitations](dx9-graphics-reference-asm-ps-instructions-flow-control.md).</span></span>
-   <span data-ttu-id="3946a-131">Los bloques de repetición pueden estar completamente dentro \* de un bloque if o por completo.</span><span class="sxs-lookup"><span data-stu-id="3946a-131">Repeat blocks are allowed to be either completely inside an if\* block or completely surrounding it.</span></span> <span data-ttu-id="3946a-132">No se permite la necesidad de estar en el mismo.</span><span class="sxs-lookup"><span data-stu-id="3946a-132">No straddling is allowed.</span></span>
-   <span data-ttu-id="3946a-133">El uso de la misma \# instrucción i para instrucciones de representación diferentes o anidadas es correcto: cada bucle se iterará en función del recuento especificado.</span><span class="sxs-lookup"><span data-stu-id="3946a-133">Using the same i\# for different or nested rep instructions is fine - each loop will iterate based on the specified count.</span></span>

## <a name="example"></a><span data-ttu-id="3946a-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3946a-134">Example</span></span>


```
rep i2
    add r0, r0, c0
endrep  
```



## <a name="related-topics"></a><span data-ttu-id="3946a-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3946a-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3946a-136">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="3946a-136">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




