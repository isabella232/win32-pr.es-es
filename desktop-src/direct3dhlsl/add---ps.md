---
title: add - ps
description: Agrega dos vectores. | add - ps
ms.assetid: f7d29a66-879b-4160-82fd-0a1b2076559a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 54092caf19a486b68b92ef63d992f11289a51c93
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/01/2021
ms.locfileid: "113130094"
---
# <a name="add---ps"></a><span data-ttu-id="b3a3d-104">add - ps</span><span class="sxs-lookup"><span data-stu-id="b3a3d-104">add - ps</span></span>

<span data-ttu-id="b3a3d-105">Agrega dos vectores.</span><span class="sxs-lookup"><span data-stu-id="b3a3d-105">Adds two vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3a3d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b3a3d-106">Syntax</span></span>



| <span data-ttu-id="b3a3d-107">add dst, src0, src1</span><span class="sxs-lookup"><span data-stu-id="b3a3d-107">add dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="b3a3d-108">where</span><span class="sxs-lookup"><span data-stu-id="b3a3d-108">where</span></span>

-   <span data-ttu-id="b3a3d-109">dst es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="b3a3d-109">dst is the destination register.</span></span>
-   <span data-ttu-id="b3a3d-110">src0 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="b3a3d-110">src0 is a source register.</span></span>
-   <span data-ttu-id="b3a3d-111">src1 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="b3a3d-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3a3d-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b3a3d-112">Remarks</span></span>



| <span data-ttu-id="b3a3d-113">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="b3a3d-113">Pixel shader versions</span></span> | <span data-ttu-id="b3a3d-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="b3a3d-114">1\_1</span></span> | <span data-ttu-id="b3a3d-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="b3a3d-115">1\_2</span></span> | <span data-ttu-id="b3a3d-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="b3a3d-116">1\_3</span></span> | <span data-ttu-id="b3a3d-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="b3a3d-117">1\_4</span></span> | <span data-ttu-id="b3a3d-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b3a3d-118">2\_0</span></span> | <span data-ttu-id="b3a3d-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b3a3d-119">2\_x</span></span> | <span data-ttu-id="b3a3d-120">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="b3a3d-120">2\_sw</span></span> | <span data-ttu-id="b3a3d-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b3a3d-121">3\_0</span></span> | <span data-ttu-id="b3a3d-122">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="b3a3d-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="b3a3d-123">add</span><span class="sxs-lookup"><span data-stu-id="b3a3d-123">add</span></span>                   | <span data-ttu-id="b3a3d-124">x</span><span class="sxs-lookup"><span data-stu-id="b3a3d-124">x</span></span>    | <span data-ttu-id="b3a3d-125">x</span><span class="sxs-lookup"><span data-stu-id="b3a3d-125">x</span></span>    | <span data-ttu-id="b3a3d-126">x</span><span class="sxs-lookup"><span data-stu-id="b3a3d-126">x</span></span>    | <span data-ttu-id="b3a3d-127">x</span><span class="sxs-lookup"><span data-stu-id="b3a3d-127">x</span></span>    | <span data-ttu-id="b3a3d-128">x</span><span class="sxs-lookup"><span data-stu-id="b3a3d-128">x</span></span>    | <span data-ttu-id="b3a3d-129">x</span><span class="sxs-lookup"><span data-stu-id="b3a3d-129">x</span></span>    | <span data-ttu-id="b3a3d-130">x</span><span class="sxs-lookup"><span data-stu-id="b3a3d-130">x</span></span>     | <span data-ttu-id="b3a3d-131">x</span><span class="sxs-lookup"><span data-stu-id="b3a3d-131">x</span></span>    | <span data-ttu-id="b3a3d-132">x</span><span class="sxs-lookup"><span data-stu-id="b3a3d-132">x</span></span>     |



 

<span data-ttu-id="b3a3d-133">El siguiente fragmento de código muestra las operaciones realizadas.</span><span class="sxs-lookup"><span data-stu-id="b3a3d-133">The following code snippet shows the operations performed.</span></span>


```
dest.x = src0.x + src1.x;
dest.y = src0.y + src1.y;
dest.z = src0.z + src1.z;
dest.w = src0.w + src1.w;
```



## <a name="instruction-information"></a><span data-ttu-id="b3a3d-134">Información de instrucciones</span><span class="sxs-lookup"><span data-stu-id="b3a3d-134">Instruction Information</span></span>



|   <span data-ttu-id="b3a3d-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3a3d-135">Requirement</span></span>                       | <span data-ttu-id="b3a3d-136">Valor</span><span class="sxs-lookup"><span data-stu-id="b3a3d-136">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="b3a3d-137">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="b3a3d-137">Minimum operating system</span></span> | <span data-ttu-id="b3a3d-138">Windows 98</span><span class="sxs-lookup"><span data-stu-id="b3a3d-138">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b3a3d-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b3a3d-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3a3d-140">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="b3a3d-140">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




