---
title: LRP-PS
description: Interpola linealmente entre el segundo y tercer registro de origen mediante una proporción especificada en el primer registro de origen. | LRP-PS
ms.assetid: b360f28e-cb2a-4403-a020-180524df6549
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: aec1ac23cc6c86f768d435e4c8169117c1bbe899
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104083686"
---
# <a name="lrp---ps"></a><span data-ttu-id="7a927-104">LRP-PS</span><span class="sxs-lookup"><span data-stu-id="7a927-104">lrp - ps</span></span>

<span data-ttu-id="7a927-105">Interpola linealmente entre el segundo y tercer registro de origen mediante una proporción especificada en el primer registro de origen.</span><span class="sxs-lookup"><span data-stu-id="7a927-105">Interpolates linearly between the second and third source registers by a proportion specified in the first source register.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a927-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7a927-106">Syntax</span></span>



| <span data-ttu-id="7a927-107">LRP DST, src0, SRC1, src2</span><span class="sxs-lookup"><span data-stu-id="7a927-107">lrp dst, src0, src1, src2</span></span> |
|---------------------------|



 

<span data-ttu-id="7a927-108">, donde</span><span class="sxs-lookup"><span data-stu-id="7a927-108">where</span></span>

-   <span data-ttu-id="7a927-109">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="7a927-109">dst is the destination register.</span></span>
-   <span data-ttu-id="7a927-110">src0 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="7a927-110">src0 is a source register.</span></span>
-   <span data-ttu-id="7a927-111">SRC1 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="7a927-111">src1 is a source register.</span></span>
-   <span data-ttu-id="7a927-112">src2 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="7a927-112">src2 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a927-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7a927-113">Remarks</span></span>



| <span data-ttu-id="7a927-114">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="7a927-114">Pixel shader versions</span></span> | <span data-ttu-id="7a927-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="7a927-115">1\_1</span></span> | <span data-ttu-id="7a927-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="7a927-116">1\_2</span></span> | <span data-ttu-id="7a927-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="7a927-117">1\_3</span></span> | <span data-ttu-id="7a927-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="7a927-118">1\_4</span></span> | <span data-ttu-id="7a927-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7a927-119">2\_0</span></span> | <span data-ttu-id="7a927-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="7a927-120">2\_x</span></span> | <span data-ttu-id="7a927-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7a927-121">2\_sw</span></span> | <span data-ttu-id="7a927-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7a927-122">3\_0</span></span> | <span data-ttu-id="7a927-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7a927-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="7a927-124">lrp</span><span class="sxs-lookup"><span data-stu-id="7a927-124">lrp</span></span>                   | <span data-ttu-id="7a927-125">x</span><span class="sxs-lookup"><span data-stu-id="7a927-125">x</span></span>    | <span data-ttu-id="7a927-126">x</span><span class="sxs-lookup"><span data-stu-id="7a927-126">x</span></span>    | <span data-ttu-id="7a927-127">x</span><span class="sxs-lookup"><span data-stu-id="7a927-127">x</span></span>    | <span data-ttu-id="7a927-128">x</span><span class="sxs-lookup"><span data-stu-id="7a927-128">x</span></span>    | <span data-ttu-id="7a927-129">x</span><span class="sxs-lookup"><span data-stu-id="7a927-129">x</span></span>    | <span data-ttu-id="7a927-130">x</span><span class="sxs-lookup"><span data-stu-id="7a927-130">x</span></span>    | <span data-ttu-id="7a927-131">x</span><span class="sxs-lookup"><span data-stu-id="7a927-131">x</span></span>     | <span data-ttu-id="7a927-132">x</span><span class="sxs-lookup"><span data-stu-id="7a927-132">x</span></span>    | <span data-ttu-id="7a927-133">x</span><span class="sxs-lookup"><span data-stu-id="7a927-133">x</span></span>     |



 

<span data-ttu-id="7a927-134">Esta instrucción realiza la interpolación lineal basada en la fórmula siguiente.</span><span class="sxs-lookup"><span data-stu-id="7a927-134">This instruction performs the linear interpolation based on the following formula.</span></span>


```
 
dest = src0 * src1 + (1-src0) * src2
// which is the same as
dest = src2 + src0 * (src1 - src2)
```



## <a name="related-topics"></a><span data-ttu-id="7a927-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7a927-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a927-136">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="7a927-136">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




