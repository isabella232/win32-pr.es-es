---
title: Agregar-PS
description: Agrega dos vectores. | Agregar-PS
ms.assetid: f7d29a66-879b-4160-82fd-0a1b2076559a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f8c6ef7c14ac54610301f283d076751b0c4d4a5e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986222"
---
# <a name="add---ps"></a><span data-ttu-id="82e7a-104">Agregar-PS</span><span class="sxs-lookup"><span data-stu-id="82e7a-104">add - ps</span></span>

<span data-ttu-id="82e7a-105">Agrega dos vectores.</span><span class="sxs-lookup"><span data-stu-id="82e7a-105">Adds two vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="82e7a-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="82e7a-106">Syntax</span></span>



| <span data-ttu-id="82e7a-107">Agregar DST, src0, SRC1</span><span class="sxs-lookup"><span data-stu-id="82e7a-107">add dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="82e7a-108">, donde</span><span class="sxs-lookup"><span data-stu-id="82e7a-108">where</span></span>

-   <span data-ttu-id="82e7a-109">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="82e7a-109">dst is the destination register.</span></span>
-   <span data-ttu-id="82e7a-110">src0 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="82e7a-110">src0 is a source register.</span></span>
-   <span data-ttu-id="82e7a-111">SRC1 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="82e7a-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="82e7a-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="82e7a-112">Remarks</span></span>



| <span data-ttu-id="82e7a-113">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="82e7a-113">Pixel shader versions</span></span> | <span data-ttu-id="82e7a-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="82e7a-114">1\_1</span></span> | <span data-ttu-id="82e7a-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="82e7a-115">1\_2</span></span> | <span data-ttu-id="82e7a-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="82e7a-116">1\_3</span></span> | <span data-ttu-id="82e7a-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="82e7a-117">1\_4</span></span> | <span data-ttu-id="82e7a-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="82e7a-118">2\_0</span></span> | <span data-ttu-id="82e7a-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="82e7a-119">2\_x</span></span> | <span data-ttu-id="82e7a-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="82e7a-120">2\_sw</span></span> | <span data-ttu-id="82e7a-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="82e7a-121">3\_0</span></span> | <span data-ttu-id="82e7a-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="82e7a-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="82e7a-123">add</span><span class="sxs-lookup"><span data-stu-id="82e7a-123">add</span></span>                   | <span data-ttu-id="82e7a-124">x</span><span class="sxs-lookup"><span data-stu-id="82e7a-124">x</span></span>    | <span data-ttu-id="82e7a-125">x</span><span class="sxs-lookup"><span data-stu-id="82e7a-125">x</span></span>    | <span data-ttu-id="82e7a-126">x</span><span class="sxs-lookup"><span data-stu-id="82e7a-126">x</span></span>    | <span data-ttu-id="82e7a-127">x</span><span class="sxs-lookup"><span data-stu-id="82e7a-127">x</span></span>    | <span data-ttu-id="82e7a-128">x</span><span class="sxs-lookup"><span data-stu-id="82e7a-128">x</span></span>    | <span data-ttu-id="82e7a-129">x</span><span class="sxs-lookup"><span data-stu-id="82e7a-129">x</span></span>    | <span data-ttu-id="82e7a-130">x</span><span class="sxs-lookup"><span data-stu-id="82e7a-130">x</span></span>     | <span data-ttu-id="82e7a-131">x</span><span class="sxs-lookup"><span data-stu-id="82e7a-131">x</span></span>    | <span data-ttu-id="82e7a-132">x</span><span class="sxs-lookup"><span data-stu-id="82e7a-132">x</span></span>     |



 

<span data-ttu-id="82e7a-133">En el fragmento de código siguiente se muestran las operaciones realizadas.</span><span class="sxs-lookup"><span data-stu-id="82e7a-133">The following code snippet shows the operations performed.</span></span>


```
dest.x = src0.x + src1.x;
dest.y = src0.y + src1.y;
dest.z = src0.z + src1.z;
dest.w = src0.w + src1.w;
```



## <a name="instruction-information"></a><span data-ttu-id="82e7a-134">Información de instrucciones</span><span class="sxs-lookup"><span data-stu-id="82e7a-134">Instruction Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="82e7a-135">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="82e7a-135">Minimum operating system</span></span> | <span data-ttu-id="82e7a-136">Windows 98</span><span class="sxs-lookup"><span data-stu-id="82e7a-136">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="82e7a-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="82e7a-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82e7a-138">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="82e7a-138">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




