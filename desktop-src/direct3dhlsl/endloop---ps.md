---
title: ENDLOOP-PS
description: Final de un bucle-PS... bloque ENDLOOP.
ms.assetid: 8d05d0b3-88d2-44e3-a22d-54d8a8ceb5f4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee1a7eb10146e40a39c05bcecb99d3a7667dee2c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103994825"
---
# <a name="endloop---ps"></a><span data-ttu-id="3d7b1-103">ENDLOOP-PS</span><span class="sxs-lookup"><span data-stu-id="3d7b1-103">endloop - ps</span></span>

<span data-ttu-id="3d7b1-104">Final de un [bucle-PS](loop---ps.md)... bloque ENDLOOP.</span><span class="sxs-lookup"><span data-stu-id="3d7b1-104">End of a [loop - ps](loop---ps.md)...endloop block.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d7b1-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3d7b1-105">Remarks</span></span>



| <span data-ttu-id="3d7b1-106">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="3d7b1-106">Pixel shader versions</span></span> | <span data-ttu-id="3d7b1-107">1\_1</span><span class="sxs-lookup"><span data-stu-id="3d7b1-107">1\_1</span></span> | <span data-ttu-id="3d7b1-108">1\_2</span><span class="sxs-lookup"><span data-stu-id="3d7b1-108">1\_2</span></span> | <span data-ttu-id="3d7b1-109">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="3d7b1-109">1\_3</span></span> | <span data-ttu-id="3d7b1-110">1\_4</span><span class="sxs-lookup"><span data-stu-id="3d7b1-110">1\_4</span></span> | <span data-ttu-id="3d7b1-111">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3d7b1-111">2\_0</span></span> | <span data-ttu-id="3d7b1-112">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="3d7b1-112">2\_x</span></span> | <span data-ttu-id="3d7b1-113">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3d7b1-113">2\_sw</span></span> | <span data-ttu-id="3d7b1-114">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3d7b1-114">3\_0</span></span> | <span data-ttu-id="3d7b1-115">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3d7b1-115">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="3d7b1-116">ENDLOOP</span><span class="sxs-lookup"><span data-stu-id="3d7b1-116">endloop</span></span>               |      |      |      |      |      |      |       | <span data-ttu-id="3d7b1-117">x</span><span class="sxs-lookup"><span data-stu-id="3d7b1-117">x</span></span>    | <span data-ttu-id="3d7b1-118">x</span><span class="sxs-lookup"><span data-stu-id="3d7b1-118">x</span></span>     |



 

<span data-ttu-id="3d7b1-119">ENDLOOP debe seguir la última instrucción de un bloque [de bucle-PS](loop---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="3d7b1-119">endloop must follow the last instruction of a [loop - ps](loop---ps.md) block.</span></span>

## <a name="example"></a><span data-ttu-id="3d7b1-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3d7b1-120">Example</span></span>


```
loop aL, i3
    add r1, r0, c2[ aL ]
endloop
```



## <a name="related-topics"></a><span data-ttu-id="3d7b1-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3d7b1-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d7b1-122">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="3d7b1-122">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




