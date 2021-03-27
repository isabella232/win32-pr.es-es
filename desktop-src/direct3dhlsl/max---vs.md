---
title: Max-vs
description: Calcula el máximo de los orígenes. | Max-vs
ms.assetid: 93fb8fb2-c722-43e5-bfe4-a2e9d3cd2049
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 923da795210fe2be62a6dd84a53f0127fef21077
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986534"
---
# <a name="max---vs"></a><span data-ttu-id="3c197-104">Max-vs</span><span class="sxs-lookup"><span data-stu-id="3c197-104">max - vs</span></span>

<span data-ttu-id="3c197-105">Calcula el máximo de los orígenes.</span><span class="sxs-lookup"><span data-stu-id="3c197-105">Calculates the maximum of the sources.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c197-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3c197-106">Syntax</span></span>



| <span data-ttu-id="3c197-107">Max DST, src0, SRC1</span><span class="sxs-lookup"><span data-stu-id="3c197-107">max dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="3c197-108">, donde</span><span class="sxs-lookup"><span data-stu-id="3c197-108">where</span></span>

-   <span data-ttu-id="3c197-109">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="3c197-109">dst is the destination register.</span></span>
-   <span data-ttu-id="3c197-110">src0 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="3c197-110">src0 is a source register.</span></span>
-   <span data-ttu-id="3c197-111">SRC1 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="3c197-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c197-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3c197-112">Remarks</span></span>



| <span data-ttu-id="3c197-113">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="3c197-113">Vertex shader versions</span></span> | <span data-ttu-id="3c197-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="3c197-114">1\_1</span></span> | <span data-ttu-id="3c197-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3c197-115">2\_0</span></span> | <span data-ttu-id="3c197-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="3c197-116">2\_x</span></span> | <span data-ttu-id="3c197-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3c197-117">2\_sw</span></span> | <span data-ttu-id="3c197-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3c197-118">3\_0</span></span> | <span data-ttu-id="3c197-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3c197-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="3c197-120">max</span><span class="sxs-lookup"><span data-stu-id="3c197-120">max</span></span>                    | <span data-ttu-id="3c197-121">x</span><span class="sxs-lookup"><span data-stu-id="3c197-121">x</span></span>    | <span data-ttu-id="3c197-122">x</span><span class="sxs-lookup"><span data-stu-id="3c197-122">x</span></span>    | <span data-ttu-id="3c197-123">x</span><span class="sxs-lookup"><span data-stu-id="3c197-123">x</span></span>    | <span data-ttu-id="3c197-124">x</span><span class="sxs-lookup"><span data-stu-id="3c197-124">x</span></span>     | <span data-ttu-id="3c197-125">x</span><span class="sxs-lookup"><span data-stu-id="3c197-125">x</span></span>    | <span data-ttu-id="3c197-126">x</span><span class="sxs-lookup"><span data-stu-id="3c197-126">x</span></span>     |



 

<span data-ttu-id="3c197-127">En el siguiente fragmento de código se muestran las operaciones realizadas.</span><span class="sxs-lookup"><span data-stu-id="3c197-127">The following code fragment shows the operations performed.</span></span>


```
dest.x=(src0.x >= src1.x) ? src0.x : src1.x;
dest.y=(src0.y >= src1.y) ? src0.y : src1.y;
dest.z=(src0.z >= src1.z) ? src0.z : src1.z;
dest.w=(src0.w >= src1.w) ? src0.w : src1.w;
```



## <a name="related-topics"></a><span data-ttu-id="3c197-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3c197-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c197-129">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="3c197-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




