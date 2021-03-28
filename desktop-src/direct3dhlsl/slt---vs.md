---
title: SLT-vs
description: Calcula el signo si el primer origen es menor que el segundo origen.
ms.assetid: 7573bcee-8f31-49ea-b515-5be59a7a508d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f6476ec24f82295d56b04682dfa4320547672b43
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104077078"
---
# <a name="slt---vs"></a><span data-ttu-id="26447-103">SLT-vs</span><span class="sxs-lookup"><span data-stu-id="26447-103">slt - vs</span></span>

<span data-ttu-id="26447-104">Calcula el signo si el primer origen es menor que el segundo origen.</span><span class="sxs-lookup"><span data-stu-id="26447-104">Computes the sign if the first source is less than the second source.</span></span>

## <a name="syntax"></a><span data-ttu-id="26447-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="26447-105">Syntax</span></span>



| <span data-ttu-id="26447-106">SLT DST, src0, SRC1</span><span class="sxs-lookup"><span data-stu-id="26447-106">slt dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="26447-107">, donde</span><span class="sxs-lookup"><span data-stu-id="26447-107">where</span></span>

-   <span data-ttu-id="26447-108">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="26447-108">dst is the destination register.</span></span>
-   <span data-ttu-id="26447-109">src0 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="26447-109">src0 is a source register.</span></span>
-   <span data-ttu-id="26447-110">SRC1 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="26447-110">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="26447-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="26447-111">Remarks</span></span>



| <span data-ttu-id="26447-112">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="26447-112">Vertex shader versions</span></span> | <span data-ttu-id="26447-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="26447-113">1\_1</span></span> | <span data-ttu-id="26447-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="26447-114">2\_0</span></span> | <span data-ttu-id="26447-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="26447-115">2\_x</span></span> | <span data-ttu-id="26447-116">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="26447-116">2\_sw</span></span> | <span data-ttu-id="26447-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="26447-117">3\_0</span></span> | <span data-ttu-id="26447-118">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="26447-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="26447-119">SLT</span><span class="sxs-lookup"><span data-stu-id="26447-119">slt</span></span>                    | <span data-ttu-id="26447-120">x</span><span class="sxs-lookup"><span data-stu-id="26447-120">x</span></span>    | <span data-ttu-id="26447-121">x</span><span class="sxs-lookup"><span data-stu-id="26447-121">x</span></span>    | <span data-ttu-id="26447-122">x</span><span class="sxs-lookup"><span data-stu-id="26447-122">x</span></span>    | <span data-ttu-id="26447-123">x</span><span class="sxs-lookup"><span data-stu-id="26447-123">x</span></span>     | <span data-ttu-id="26447-124">x</span><span class="sxs-lookup"><span data-stu-id="26447-124">x</span></span>    | <span data-ttu-id="26447-125">x</span><span class="sxs-lookup"><span data-stu-id="26447-125">x</span></span>     |



 

<span data-ttu-id="26447-126">En el siguiente fragmento de código se muestran las operaciones realizadas.</span><span class="sxs-lookup"><span data-stu-id="26447-126">The following code fragment shows the operations performed.</span></span>


```
dest.x = (src0.x < src1.x) ? 1.0f : 0.0f;
dest.y = (src0.y < src1.y) ? 1.0f : 0.0f;
dest.z = (src0.z < src1.z) ? 1.0f : 0.0f;
dest.w = (src0.w < src1.w) ? 1.0f : 0.0f;
```



## <a name="related-topics"></a><span data-ttu-id="26447-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="26447-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26447-128">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="26447-128">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




