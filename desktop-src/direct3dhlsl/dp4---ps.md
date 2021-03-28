---
title: DP4-PS
description: Calcula el producto de cuatro componentes de los registros de origen. | DP4-PS
ms.assetid: 83ef6097-cacf-4498-842b-3eb03e57bd6f
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2562259af164b8680d54e9a120abaa405fd781c5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104083642"
---
# <a name="dp4---ps"></a><span data-ttu-id="f935a-104">DP4-PS</span><span class="sxs-lookup"><span data-stu-id="f935a-104">dp4 - ps</span></span>

<span data-ttu-id="f935a-105">Calcula el producto de cuatro componentes de los registros de origen.</span><span class="sxs-lookup"><span data-stu-id="f935a-105">Computes the four-component dot product of the source registers.</span></span>

## <a name="syntax"></a><span data-ttu-id="f935a-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f935a-106">Syntax</span></span>



| <span data-ttu-id="f935a-107">DP4 DST, src0, SRC1</span><span class="sxs-lookup"><span data-stu-id="f935a-107">dp4 dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="f935a-108">, donde</span><span class="sxs-lookup"><span data-stu-id="f935a-108">where</span></span>

-   <span data-ttu-id="f935a-109">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="f935a-109">dst is the destination register.</span></span>
-   <span data-ttu-id="f935a-110">src0 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="f935a-110">src0 is a source register.</span></span>
-   <span data-ttu-id="f935a-111">SRC1 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="f935a-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="f935a-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f935a-112">Remarks</span></span>



| <span data-ttu-id="f935a-113">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="f935a-113">Pixel shader versions</span></span> | <span data-ttu-id="f935a-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="f935a-114">1\_1</span></span> | <span data-ttu-id="f935a-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="f935a-115">1\_2</span></span> | <span data-ttu-id="f935a-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="f935a-116">1\_3</span></span> | <span data-ttu-id="f935a-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="f935a-117">1\_4</span></span> | <span data-ttu-id="f935a-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f935a-118">2\_0</span></span> | <span data-ttu-id="f935a-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="f935a-119">2\_x</span></span> | <span data-ttu-id="f935a-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f935a-120">2\_sw</span></span> | <span data-ttu-id="f935a-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f935a-121">3\_0</span></span> | <span data-ttu-id="f935a-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f935a-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="f935a-123">dp4</span><span class="sxs-lookup"><span data-stu-id="f935a-123">dp4</span></span>                   |      | <span data-ttu-id="f935a-124">x</span><span class="sxs-lookup"><span data-stu-id="f935a-124">x</span></span>    | <span data-ttu-id="f935a-125">x</span><span class="sxs-lookup"><span data-stu-id="f935a-125">x</span></span>    | <span data-ttu-id="f935a-126">x</span><span class="sxs-lookup"><span data-stu-id="f935a-126">x</span></span>    | <span data-ttu-id="f935a-127">x</span><span class="sxs-lookup"><span data-stu-id="f935a-127">x</span></span>    | <span data-ttu-id="f935a-128">x</span><span class="sxs-lookup"><span data-stu-id="f935a-128">x</span></span>    | <span data-ttu-id="f935a-129">x</span><span class="sxs-lookup"><span data-stu-id="f935a-129">x</span></span>     | <span data-ttu-id="f935a-130">x</span><span class="sxs-lookup"><span data-stu-id="f935a-130">x</span></span>    | <span data-ttu-id="f935a-131">x</span><span class="sxs-lookup"><span data-stu-id="f935a-131">x</span></span>     |



 

<span data-ttu-id="f935a-132">En el fragmento de código siguiente se muestran las operaciones realizadas:</span><span class="sxs-lookup"><span data-stu-id="f935a-132">The following code snippet shows the operations performed:</span></span>


```
dest.x = dest.y = dest.z = dest.w = 
    (src0.x * src1.x) + (src0.y * src1.y) + 
    (src0.z * src1.z) + (src0.w * src1.w);
```



<span data-ttu-id="f935a-133">Limitaciones de PS \_ 1 \_ 2 y PS \_ 1 \_ 3:</span><span class="sxs-lookup"><span data-stu-id="f935a-133">Limitations for ps\_1\_2 and ps\_1\_3:</span></span>

-   <span data-ttu-id="f935a-134">Cada sombreador puede usar un máximo de cuatro instrucciones DP4.</span><span class="sxs-lookup"><span data-stu-id="f935a-134">Each shader can use up to a maximum of four dp4 instructions.</span></span>
-   <span data-ttu-id="f935a-135">Cada instrucción de DP4 cuenta como dos Instrucciones aritméticas.</span><span class="sxs-lookup"><span data-stu-id="f935a-135">Each dp4 instruction counts as two arithmetic instructions.</span></span>

<span data-ttu-id="f935a-136">Limitaciones de \_ las versiones 1 X:</span><span class="sxs-lookup"><span data-stu-id="f935a-136">Limitations for 1\_X versions:</span></span>

-   <span data-ttu-id="f935a-137">Esta instrucción no se puede compedir de forma conjunta porque DP4 se ejecuta en la canalización vector y alfa.</span><span class="sxs-lookup"><span data-stu-id="f935a-137">This instruction cannot be co-issued because dp4 runs in both the vector and alpha pipeline.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f935a-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f935a-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f935a-139">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="f935a-139">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




