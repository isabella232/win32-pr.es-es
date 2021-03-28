---
title: ABS-PS
description: Calcula el valor absoluto. | ABS-PS
ms.assetid: e97db550-2a03-421a-86f4-a6fc5f8e0bca
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 070a513aaa0d336d5ac404b1748fdd162edfd532
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362030"
---
# <a name="abs---ps"></a><span data-ttu-id="bb137-104">ABS-PS</span><span class="sxs-lookup"><span data-stu-id="bb137-104">abs - ps</span></span>

<span data-ttu-id="bb137-105">Calcula el valor absoluto.</span><span class="sxs-lookup"><span data-stu-id="bb137-105">Computes absolute value.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb137-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bb137-106">Syntax</span></span>



|              |
|--------------|
| <span data-ttu-id="bb137-107">ABS DST, src</span><span class="sxs-lookup"><span data-stu-id="bb137-107">abs dst, src</span></span> |



 

<span data-ttu-id="bb137-108">, donde</span><span class="sxs-lookup"><span data-stu-id="bb137-108">where</span></span>

-   <span data-ttu-id="bb137-109">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="bb137-109">dst is the destination register.</span></span>
-   <span data-ttu-id="bb137-110">src es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="bb137-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb137-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bb137-111">Remarks</span></span>



|                       |      |      |      |      |      |      |       |      |       |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="bb137-112">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="bb137-112">Pixel shader versions</span></span> | <span data-ttu-id="bb137-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="bb137-113">1\_1</span></span> | <span data-ttu-id="bb137-114">1\_2</span><span class="sxs-lookup"><span data-stu-id="bb137-114">1\_2</span></span> | <span data-ttu-id="bb137-115">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="bb137-115">1\_3</span></span> | <span data-ttu-id="bb137-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="bb137-116">1\_4</span></span> | <span data-ttu-id="bb137-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bb137-117">2\_0</span></span> | <span data-ttu-id="bb137-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="bb137-118">2\_x</span></span> | <span data-ttu-id="bb137-119">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="bb137-119">2\_sw</span></span> | <span data-ttu-id="bb137-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bb137-120">3\_0</span></span> | <span data-ttu-id="bb137-121">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="bb137-121">3\_sw</span></span> |
| <span data-ttu-id="bb137-122">abs</span><span class="sxs-lookup"><span data-stu-id="bb137-122">abs</span></span>                   |      |      |      |      | <span data-ttu-id="bb137-123">x</span><span class="sxs-lookup"><span data-stu-id="bb137-123">x</span></span>    | <span data-ttu-id="bb137-124">x</span><span class="sxs-lookup"><span data-stu-id="bb137-124">x</span></span>    | <span data-ttu-id="bb137-125">x</span><span class="sxs-lookup"><span data-stu-id="bb137-125">x</span></span>     | <span data-ttu-id="bb137-126">x</span><span class="sxs-lookup"><span data-stu-id="bb137-126">x</span></span>    | <span data-ttu-id="bb137-127">x</span><span class="sxs-lookup"><span data-stu-id="bb137-127">x</span></span>     |



 

<span data-ttu-id="bb137-128">Esta instrucción funciona como se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="bb137-128">This instruction works as shown here.</span></span>


```
dest.x = abs(src.x)
dest.y = abs(src.y)
dest.z = abs(src.z)
dest.w = abs(src.w)
```



## <a name="instruction-information"></a><span data-ttu-id="bb137-129">Información de instrucciones</span><span class="sxs-lookup"><span data-stu-id="bb137-129">Instruction Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="bb137-130">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="bb137-130">Minimum operating system</span></span> | <span data-ttu-id="bb137-131">Windows 98</span><span class="sxs-lookup"><span data-stu-id="bb137-131">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="bb137-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bb137-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb137-133">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="bb137-133">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




