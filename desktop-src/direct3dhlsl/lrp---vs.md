---
title: LRP-vs
description: Interpola linealmente entre el segundo y tercer registro de origen mediante una proporción especificada en el primer registro de origen. | LRP-vs
ms.assetid: 8438bcf3-9b00-4963-b2a3-54fd1c345961
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 485d7720dc2c71ee599db93d179de8e665bfab77
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998152"
---
# <a name="lrp---vs"></a><span data-ttu-id="5161f-104">LRP-vs</span><span class="sxs-lookup"><span data-stu-id="5161f-104">lrp - vs</span></span>

<span data-ttu-id="5161f-105">Interpola linealmente entre el segundo y tercer registro de origen mediante una proporción especificada en el primer registro de origen.</span><span class="sxs-lookup"><span data-stu-id="5161f-105">Interpolates linearly between the second and third source registers by a proportion specified in the first source register.</span></span>

## <a name="syntax"></a><span data-ttu-id="5161f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5161f-106">Syntax</span></span>



| <span data-ttu-id="5161f-107">LRP DST, src0, SRC1, src2</span><span class="sxs-lookup"><span data-stu-id="5161f-107">lrp dst, src0, src1, src2</span></span> |
|---------------------------|



 

<span data-ttu-id="5161f-108">, donde</span><span class="sxs-lookup"><span data-stu-id="5161f-108">where</span></span>

-   <span data-ttu-id="5161f-109">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="5161f-109">dst is the destination register.</span></span>
-   <span data-ttu-id="5161f-110">src0 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="5161f-110">src0 is a source register.</span></span>
-   <span data-ttu-id="5161f-111">SRC1 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="5161f-111">src1 is a source register.</span></span>
-   <span data-ttu-id="5161f-112">src2 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="5161f-112">src2 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="5161f-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5161f-113">Remarks</span></span>



| <span data-ttu-id="5161f-114">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="5161f-114">Vertex shader versions</span></span> | <span data-ttu-id="5161f-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="5161f-115">1\_1</span></span> | <span data-ttu-id="5161f-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5161f-116">2\_0</span></span> | <span data-ttu-id="5161f-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5161f-117">2\_x</span></span> | <span data-ttu-id="5161f-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5161f-118">2\_sw</span></span> | <span data-ttu-id="5161f-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5161f-119">3\_0</span></span> | <span data-ttu-id="5161f-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5161f-120">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="5161f-121">lrp</span><span class="sxs-lookup"><span data-stu-id="5161f-121">lrp</span></span>                    |      | <span data-ttu-id="5161f-122">x</span><span class="sxs-lookup"><span data-stu-id="5161f-122">x</span></span>    | <span data-ttu-id="5161f-123">x</span><span class="sxs-lookup"><span data-stu-id="5161f-123">x</span></span>    | <span data-ttu-id="5161f-124">x</span><span class="sxs-lookup"><span data-stu-id="5161f-124">x</span></span>     | <span data-ttu-id="5161f-125">x</span><span class="sxs-lookup"><span data-stu-id="5161f-125">x</span></span>    | <span data-ttu-id="5161f-126">x</span><span class="sxs-lookup"><span data-stu-id="5161f-126">x</span></span>     |



 

<span data-ttu-id="5161f-127">Esta instrucción realiza la interpolación lineal basada en la fórmula siguiente.</span><span class="sxs-lookup"><span data-stu-id="5161f-127">This instruction performs the linear interpolation based on the following formula.</span></span>


```
dest.x = src0.x * (src1.x - src2.x) + src2.x;
dest.y = src0.y * (src1.y - src2.y) + src2.y;
dest.z = src0.z * (src1.z - src2.z) + src2.z;
dest.w = src0.w * (src1.w - src2.w) + src2.w;
```



## <a name="related-topics"></a><span data-ttu-id="5161f-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5161f-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5161f-129">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="5161f-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




