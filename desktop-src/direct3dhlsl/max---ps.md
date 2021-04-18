---
title: Max-PS
description: Calcula el máximo de los orígenes. | Max-PS
ms.assetid: 3d3bef5b-0ff7-441b-8681-a3f4cde0ae4f
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c6186f0bd57acd4862a62a4c0a30ae92118b75ce
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986743"
---
# <a name="max---ps"></a><span data-ttu-id="8f8cc-104">Max-PS</span><span class="sxs-lookup"><span data-stu-id="8f8cc-104">max - ps</span></span>

<span data-ttu-id="8f8cc-105">Calcula el máximo de los orígenes.</span><span class="sxs-lookup"><span data-stu-id="8f8cc-105">Calculates the maximum of the sources.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f8cc-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8f8cc-106">Syntax</span></span>



| <span data-ttu-id="8f8cc-107">Max DST, src0, SRC1</span><span class="sxs-lookup"><span data-stu-id="8f8cc-107">max dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="8f8cc-108">, donde</span><span class="sxs-lookup"><span data-stu-id="8f8cc-108">where</span></span>

-   <span data-ttu-id="8f8cc-109">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="8f8cc-109">dst is the destination register.</span></span>
-   <span data-ttu-id="8f8cc-110">src0 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="8f8cc-110">src0 is a source register.</span></span>
-   <span data-ttu-id="8f8cc-111">SRC1 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="8f8cc-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f8cc-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8f8cc-112">Remarks</span></span>



| <span data-ttu-id="8f8cc-113">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="8f8cc-113">Pixel shader versions</span></span> | <span data-ttu-id="8f8cc-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="8f8cc-114">1\_1</span></span> | <span data-ttu-id="8f8cc-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="8f8cc-115">1\_2</span></span> | <span data-ttu-id="8f8cc-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="8f8cc-116">1\_3</span></span> | <span data-ttu-id="8f8cc-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="8f8cc-117">1\_4</span></span> | <span data-ttu-id="8f8cc-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8f8cc-118">2\_0</span></span> | <span data-ttu-id="8f8cc-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="8f8cc-119">2\_x</span></span> | <span data-ttu-id="8f8cc-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="8f8cc-120">2\_sw</span></span> | <span data-ttu-id="8f8cc-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8f8cc-121">3\_0</span></span> | <span data-ttu-id="8f8cc-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="8f8cc-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="8f8cc-123">max</span><span class="sxs-lookup"><span data-stu-id="8f8cc-123">max</span></span>                   |      |      |      |      | <span data-ttu-id="8f8cc-124">x</span><span class="sxs-lookup"><span data-stu-id="8f8cc-124">x</span></span>    | <span data-ttu-id="8f8cc-125">x</span><span class="sxs-lookup"><span data-stu-id="8f8cc-125">x</span></span>    | <span data-ttu-id="8f8cc-126">x</span><span class="sxs-lookup"><span data-stu-id="8f8cc-126">x</span></span>     | <span data-ttu-id="8f8cc-127">x</span><span class="sxs-lookup"><span data-stu-id="8f8cc-127">x</span></span>    | <span data-ttu-id="8f8cc-128">x</span><span class="sxs-lookup"><span data-stu-id="8f8cc-128">x</span></span>     |



 

<span data-ttu-id="8f8cc-129">En el fragmento de código siguiente se muestran las operaciones realizadas.</span><span class="sxs-lookup"><span data-stu-id="8f8cc-129">The following code snippet shows the operations performed.</span></span>


```
dest.x=(src0.x >= src1.x) ? src0.x : src1.x;
dest.y=(src0.y >= src1.y) ? src0.y : src1.y;
dest.z=(src0.z >= src1.z) ? src0.z : src1.z;
dest.w=(src0.w >= src1.w) ? src0.w : src1.w;
```



## <a name="related-topics"></a><span data-ttu-id="8f8cc-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8f8cc-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f8cc-131">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="8f8cc-131">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




