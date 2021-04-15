---
title: min-PS
description: Calcula el mínimo de los orígenes. | min-PS
ms.assetid: 2ee6208d-a353-4747-8037-c21dd1a05016
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3a735b38769a30e9dccf544785d931641469f5dc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986443"
---
# <a name="min---ps"></a><span data-ttu-id="5d7bf-104">min-PS</span><span class="sxs-lookup"><span data-stu-id="5d7bf-104">min - ps</span></span>

<span data-ttu-id="5d7bf-105">Calcula el mínimo de los orígenes.</span><span class="sxs-lookup"><span data-stu-id="5d7bf-105">Calculates the minimum of the sources.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d7bf-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5d7bf-106">Syntax</span></span>



| <span data-ttu-id="5d7bf-107">min DST, src0, SRC1</span><span class="sxs-lookup"><span data-stu-id="5d7bf-107">min dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="5d7bf-108">, donde</span><span class="sxs-lookup"><span data-stu-id="5d7bf-108">where</span></span>

-   <span data-ttu-id="5d7bf-109">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="5d7bf-109">dst is the destination register.</span></span>
-   <span data-ttu-id="5d7bf-110">src0 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="5d7bf-110">src0 is a source register.</span></span>
-   <span data-ttu-id="5d7bf-111">SRC1 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="5d7bf-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d7bf-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5d7bf-112">Remarks</span></span>



| <span data-ttu-id="5d7bf-113">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="5d7bf-113">Pixel shader versions</span></span> | <span data-ttu-id="5d7bf-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="5d7bf-114">1\_1</span></span> | <span data-ttu-id="5d7bf-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="5d7bf-115">1\_2</span></span> | <span data-ttu-id="5d7bf-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="5d7bf-116">1\_3</span></span> | <span data-ttu-id="5d7bf-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="5d7bf-117">1\_4</span></span> | <span data-ttu-id="5d7bf-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5d7bf-118">2\_0</span></span> | <span data-ttu-id="5d7bf-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5d7bf-119">2\_x</span></span> | <span data-ttu-id="5d7bf-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5d7bf-120">2\_sw</span></span> | <span data-ttu-id="5d7bf-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5d7bf-121">3\_0</span></span> | <span data-ttu-id="5d7bf-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5d7bf-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="5d7bf-123">min.</span><span class="sxs-lookup"><span data-stu-id="5d7bf-123">min</span></span>                   |      |      |      |      | <span data-ttu-id="5d7bf-124">x</span><span class="sxs-lookup"><span data-stu-id="5d7bf-124">x</span></span>    | <span data-ttu-id="5d7bf-125">x</span><span class="sxs-lookup"><span data-stu-id="5d7bf-125">x</span></span>    | <span data-ttu-id="5d7bf-126">x</span><span class="sxs-lookup"><span data-stu-id="5d7bf-126">x</span></span>     | <span data-ttu-id="5d7bf-127">x</span><span class="sxs-lookup"><span data-stu-id="5d7bf-127">x</span></span>    | <span data-ttu-id="5d7bf-128">x</span><span class="sxs-lookup"><span data-stu-id="5d7bf-128">x</span></span>     |



 

<span data-ttu-id="5d7bf-129">En el fragmento de código siguiente se muestran las operaciones realizadas.</span><span class="sxs-lookup"><span data-stu-id="5d7bf-129">The following code snippet shows the operations performed.</span></span>


```
dest.x=(src0.x < src1.x) ? src0.x : src1.x;
dest.y=(src0.y < src1.y) ? src0.y : src1.y;
dest.z=(src0.z < src1.z) ? src0.z : src1.z;
dest.w=(src0.w < src1.w) ? src0.w : src1.w;
```



## <a name="related-topics"></a><span data-ttu-id="5d7bf-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5d7bf-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d7bf-131">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="5d7bf-131">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




