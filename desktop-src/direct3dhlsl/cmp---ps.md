---
title: CMP-PS
description: Elija SRC1 si src0 0. De lo contrario, elija src2. La comparación se realiza por canal.
ms.assetid: 8fabd548-3f5e-4b78-bf1e-16e4f1548ccd
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: da3da1062d02e995876a1f67e5c4e19518774760
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104077089"
---
# <a name="cmp---ps"></a><span data-ttu-id="5f8e4-105">CMP-PS</span><span class="sxs-lookup"><span data-stu-id="5f8e4-105">cmp - ps</span></span>

<span data-ttu-id="5f8e4-106">Elija SRC1 si src0 >= 0.</span><span class="sxs-lookup"><span data-stu-id="5f8e4-106">Choose src1 if src0 >= 0.</span></span> <span data-ttu-id="5f8e4-107">De lo contrario, elija src2.</span><span class="sxs-lookup"><span data-stu-id="5f8e4-107">Otherwise, choose src2.</span></span> <span data-ttu-id="5f8e4-108">La comparación se realiza por canal.</span><span class="sxs-lookup"><span data-stu-id="5f8e4-108">The comparison is done per channel.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f8e4-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5f8e4-109">Syntax</span></span>



| <span data-ttu-id="5f8e4-110">CMP DST, src0, SRC1, src2</span><span class="sxs-lookup"><span data-stu-id="5f8e4-110">cmp dst, src0, src1, src2</span></span> |
|---------------------------|



 

<span data-ttu-id="5f8e4-111">, donde</span><span class="sxs-lookup"><span data-stu-id="5f8e4-111">where</span></span>

-   <span data-ttu-id="5f8e4-112">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="5f8e4-112">dst is the destination register.</span></span>
-   <span data-ttu-id="5f8e4-113">src0 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="5f8e4-113">src0 is a source register.</span></span>
-   <span data-ttu-id="5f8e4-114">SRC1 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="5f8e4-114">src1 is a source register.</span></span>
-   <span data-ttu-id="5f8e4-115">src2 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="5f8e4-115">src2 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f8e4-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5f8e4-116">Remarks</span></span>



| <span data-ttu-id="5f8e4-117">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="5f8e4-117">Pixel shader versions</span></span> | <span data-ttu-id="5f8e4-118">1\_1</span><span class="sxs-lookup"><span data-stu-id="5f8e4-118">1\_1</span></span> | <span data-ttu-id="5f8e4-119">1\_2</span><span class="sxs-lookup"><span data-stu-id="5f8e4-119">1\_2</span></span> | <span data-ttu-id="5f8e4-120">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="5f8e4-120">1\_3</span></span> | <span data-ttu-id="5f8e4-121">1\_4</span><span class="sxs-lookup"><span data-stu-id="5f8e4-121">1\_4</span></span> | <span data-ttu-id="5f8e4-122">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5f8e4-122">2\_0</span></span> | <span data-ttu-id="5f8e4-123">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5f8e4-123">2\_x</span></span> | <span data-ttu-id="5f8e4-124">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5f8e4-124">2\_sw</span></span> | <span data-ttu-id="5f8e4-125">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5f8e4-125">3\_0</span></span> | <span data-ttu-id="5f8e4-126">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5f8e4-126">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="5f8e4-127">CMP</span><span class="sxs-lookup"><span data-stu-id="5f8e4-127">cmp</span></span>                   |      | <span data-ttu-id="5f8e4-128">x</span><span class="sxs-lookup"><span data-stu-id="5f8e4-128">x</span></span>    | <span data-ttu-id="5f8e4-129">x</span><span class="sxs-lookup"><span data-stu-id="5f8e4-129">x</span></span>    | <span data-ttu-id="5f8e4-130">x</span><span class="sxs-lookup"><span data-stu-id="5f8e4-130">x</span></span>    | <span data-ttu-id="5f8e4-131">x</span><span class="sxs-lookup"><span data-stu-id="5f8e4-131">x</span></span>    | <span data-ttu-id="5f8e4-132">x</span><span class="sxs-lookup"><span data-stu-id="5f8e4-132">x</span></span>    | <span data-ttu-id="5f8e4-133">x</span><span class="sxs-lookup"><span data-stu-id="5f8e4-133">x</span></span>     | <span data-ttu-id="5f8e4-134">x</span><span class="sxs-lookup"><span data-stu-id="5f8e4-134">x</span></span>    | <span data-ttu-id="5f8e4-135">x</span><span class="sxs-lookup"><span data-stu-id="5f8e4-135">x</span></span>     |



 

<span data-ttu-id="5f8e4-136">Existen algunas limitaciones adicionales para las versiones 1 \_ 2 y 1 \_ 3:</span><span class="sxs-lookup"><span data-stu-id="5f8e4-136">There are a few additional limitations for versions 1\_2 and 1\_3:</span></span>

-   <span data-ttu-id="5f8e4-137">Cada sombreador puede utilizar hasta tres instrucciones de CMP como máximo.</span><span class="sxs-lookup"><span data-stu-id="5f8e4-137">Each shader can use up to a maximum of three cmp instructions.</span></span>
-   <span data-ttu-id="5f8e4-138">El registro de destino no puede ser el mismo que ninguno de los registros de origen.</span><span class="sxs-lookup"><span data-stu-id="5f8e4-138">The destination register cannot be the same as any of the source registers.</span></span>

<span data-ttu-id="5f8e4-139">En este ejemplo se realiza una comparación de cuatro canales.</span><span class="sxs-lookup"><span data-stu-id="5f8e4-139">This example does a four-channel comparison.</span></span>


```
ps_1_4
def c0, -0.6, 0.6, 0, 0.6
def c1  0,0,0,0
def c2  1,1,1,1

mov r1, c1
mov r2, c2

cmp r0, c0, r1, r2   // r0 is assigned 1,0,0,0 based on the following:

// r0.x = c2.x because c0.x < 0
// r0.y = c1.y because c0.y >= 0
// r0.z = c1.z because c0.z >= 0
// r0.w = c1.w because c0.w >= 0
```



## <a name="related-topics"></a><span data-ttu-id="5f8e4-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5f8e4-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f8e4-141">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="5f8e4-141">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




