---
title: SGE-vs
description: Calcula el signo si el primer origen es mayor o igual que el segundo origen.
ms.assetid: 88e8eb68-8189-40c3-b20e-f395576f5f6a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7bad8816b87a32c5f10c73df27beb3cc2aef7716
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419937"
---
# <a name="sge---vs"></a><span data-ttu-id="5789e-103">SGE-vs</span><span class="sxs-lookup"><span data-stu-id="5789e-103">sge - vs</span></span>

<span data-ttu-id="5789e-104">Calcula el signo si el primer origen es mayor o igual que el segundo origen.</span><span class="sxs-lookup"><span data-stu-id="5789e-104">Computes the sign if the first source is greater than or equal to the second source.</span></span>

## <a name="syntax"></a><span data-ttu-id="5789e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5789e-105">Syntax</span></span>



| <span data-ttu-id="5789e-106">SGE DST, src0, SRC1</span><span class="sxs-lookup"><span data-stu-id="5789e-106">sge dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="5789e-107">, donde</span><span class="sxs-lookup"><span data-stu-id="5789e-107">where</span></span>

-   <span data-ttu-id="5789e-108">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="5789e-108">dst is the destination register.</span></span>
-   <span data-ttu-id="5789e-109">src0 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="5789e-109">src0 is a source register.</span></span>
-   <span data-ttu-id="5789e-110">SRC1 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="5789e-110">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="5789e-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5789e-111">Remarks</span></span>



| <span data-ttu-id="5789e-112">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="5789e-112">Vertex shader versions</span></span> | <span data-ttu-id="5789e-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="5789e-113">1\_1</span></span> | <span data-ttu-id="5789e-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5789e-114">2\_0</span></span> | <span data-ttu-id="5789e-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5789e-115">2\_x</span></span> | <span data-ttu-id="5789e-116">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5789e-116">2\_sw</span></span> | <span data-ttu-id="5789e-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5789e-117">3\_0</span></span> | <span data-ttu-id="5789e-118">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5789e-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="5789e-119">sge</span><span class="sxs-lookup"><span data-stu-id="5789e-119">sge</span></span>                    | <span data-ttu-id="5789e-120">x</span><span class="sxs-lookup"><span data-stu-id="5789e-120">x</span></span>    | <span data-ttu-id="5789e-121">x</span><span class="sxs-lookup"><span data-stu-id="5789e-121">x</span></span>    | <span data-ttu-id="5789e-122">x</span><span class="sxs-lookup"><span data-stu-id="5789e-122">x</span></span>    | <span data-ttu-id="5789e-123">x</span><span class="sxs-lookup"><span data-stu-id="5789e-123">x</span></span>     | <span data-ttu-id="5789e-124">x</span><span class="sxs-lookup"><span data-stu-id="5789e-124">x</span></span>    | <span data-ttu-id="5789e-125">x</span><span class="sxs-lookup"><span data-stu-id="5789e-125">x</span></span>     |



 

<span data-ttu-id="5789e-126">En el siguiente fragmento de código se muestran las operaciones realizadas.</span><span class="sxs-lookup"><span data-stu-id="5789e-126">The following code fragment shows the operations performed.</span></span>


```
 
dest.x = (src0.x >= src1.x) ? 1.0f : 0.0f;
dest.y = (src0.y >= src1.y) ? 1.0f : 0.0f;
dest.z = (src0.z >= src1.z) ? 1.0f : 0.0f;
dest.w = (src0.w >= src1.w) ? 1.0f : 0.0f;
```



## <a name="related-topics"></a><span data-ttu-id="5789e-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5789e-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5789e-128">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="5789e-128">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




