---
title: ENDLOOP-vs
description: Fin de un bucle... bloque ENDLOOP.
ms.assetid: fd7df120-a927-4a66-b152-6ce5247446e4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8a9aec4d1b2c5237a87fae2c0beab4e8d995db97
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419879"
---
# <a name="endloop---vs"></a><span data-ttu-id="5037e-103">ENDLOOP-vs</span><span class="sxs-lookup"><span data-stu-id="5037e-103">endloop - vs</span></span>

<span data-ttu-id="5037e-104">Fin de un [bucle](loop---vs.md)... bloque ENDLOOP.</span><span class="sxs-lookup"><span data-stu-id="5037e-104">End of a [loop](loop---vs.md)...endloop block.</span></span>

## <a name="syntax"></a><span data-ttu-id="5037e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5037e-105">Syntax</span></span>



| <span data-ttu-id="5037e-106">ENDLOOP</span><span class="sxs-lookup"><span data-stu-id="5037e-106">endloop</span></span> |
|---------|



 

## <a name="remarks"></a><span data-ttu-id="5037e-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5037e-107">Remarks</span></span>



| <span data-ttu-id="5037e-108">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="5037e-108">Vertex shader versions</span></span> | <span data-ttu-id="5037e-109">1\_1</span><span class="sxs-lookup"><span data-stu-id="5037e-109">1\_1</span></span> | <span data-ttu-id="5037e-110">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5037e-110">2\_0</span></span> | <span data-ttu-id="5037e-111">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5037e-111">2\_x</span></span> | <span data-ttu-id="5037e-112">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5037e-112">2\_sw</span></span> | <span data-ttu-id="5037e-113">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5037e-113">3\_0</span></span> | <span data-ttu-id="5037e-114">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5037e-114">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="5037e-115">ENDLOOP</span><span class="sxs-lookup"><span data-stu-id="5037e-115">endloop</span></span>                |      | <span data-ttu-id="5037e-116">x</span><span class="sxs-lookup"><span data-stu-id="5037e-116">x</span></span>    | <span data-ttu-id="5037e-117">x</span><span class="sxs-lookup"><span data-stu-id="5037e-117">x</span></span>    | <span data-ttu-id="5037e-118">x</span><span class="sxs-lookup"><span data-stu-id="5037e-118">x</span></span>     | <span data-ttu-id="5037e-119">x</span><span class="sxs-lookup"><span data-stu-id="5037e-119">x</span></span>    | <span data-ttu-id="5037e-120">x</span><span class="sxs-lookup"><span data-stu-id="5037e-120">x</span></span>     |



 

<span data-ttu-id="5037e-121">Esta instrucción funciona como se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="5037e-121">This instruction works as shown here.</span></span>


```
LoopCounter += LoopStep;
LoopInterationCount = LoopIterationCount - 1;
if (LoopIterationCount > 0)
    Continue execution at the StartLoopOffset
```



<span data-ttu-id="5037e-122">ENDLOOP debe seguir la última instrucción de un bloque [Loop-vs](loop---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="5037e-122">endloop must follow the last instruction of a [loop - vs](loop---vs.md) block.</span></span>

## <a name="example"></a><span data-ttu-id="5037e-123">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5037e-123">Example</span></span>


```
loop aL, i3
    add r1, r0, c2[ aL ]
endloop
```



## <a name="related-topics"></a><span data-ttu-id="5037e-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5037e-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5037e-125">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="5037e-125">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




