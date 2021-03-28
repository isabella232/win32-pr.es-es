---
title: Sub-PS
description: Resta orígenes. | Sub-PS
ms.assetid: e130724f-63bf-4d7f-bc9f-6a4441a788b8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4998892aa06eff55632600a9c2f7fe359c11f830
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "103820498"
---
# <a name="sub---ps"></a><span data-ttu-id="df786-104">Sub-PS</span><span class="sxs-lookup"><span data-stu-id="df786-104">sub - ps</span></span>

<span data-ttu-id="df786-105">Resta orígenes.</span><span class="sxs-lookup"><span data-stu-id="df786-105">Subtracts sources.</span></span>

## <a name="syntax"></a><span data-ttu-id="df786-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="df786-106">Syntax</span></span>



| <span data-ttu-id="df786-107">Sub DST, src0, SRC1</span><span class="sxs-lookup"><span data-stu-id="df786-107">sub dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="df786-108">, donde</span><span class="sxs-lookup"><span data-stu-id="df786-108">where</span></span>

-   <span data-ttu-id="df786-109">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="df786-109">dst is the destination register.</span></span>
-   <span data-ttu-id="df786-110">src0 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="df786-110">src0 is a source register.</span></span>
-   <span data-ttu-id="df786-111">SRC1 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="df786-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="df786-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="df786-112">Remarks</span></span>



| <span data-ttu-id="df786-113">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="df786-113">Pixel shader versions</span></span> | <span data-ttu-id="df786-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="df786-114">1\_1</span></span> | <span data-ttu-id="df786-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="df786-115">1\_2</span></span> | <span data-ttu-id="df786-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="df786-116">1\_3</span></span> | <span data-ttu-id="df786-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="df786-117">1\_4</span></span> | <span data-ttu-id="df786-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="df786-118">2\_0</span></span> | <span data-ttu-id="df786-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="df786-119">2\_x</span></span> | <span data-ttu-id="df786-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="df786-120">2\_sw</span></span> | <span data-ttu-id="df786-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="df786-121">3\_0</span></span> | <span data-ttu-id="df786-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="df786-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="df786-123">sub</span><span class="sxs-lookup"><span data-stu-id="df786-123">sub</span></span>                   | <span data-ttu-id="df786-124">x</span><span class="sxs-lookup"><span data-stu-id="df786-124">x</span></span>    | <span data-ttu-id="df786-125">x</span><span class="sxs-lookup"><span data-stu-id="df786-125">x</span></span>    | <span data-ttu-id="df786-126">x</span><span class="sxs-lookup"><span data-stu-id="df786-126">x</span></span>    | <span data-ttu-id="df786-127">x</span><span class="sxs-lookup"><span data-stu-id="df786-127">x</span></span>    | <span data-ttu-id="df786-128">x</span><span class="sxs-lookup"><span data-stu-id="df786-128">x</span></span>    | <span data-ttu-id="df786-129">x</span><span class="sxs-lookup"><span data-stu-id="df786-129">x</span></span>    | <span data-ttu-id="df786-130">x</span><span class="sxs-lookup"><span data-stu-id="df786-130">x</span></span>     | <span data-ttu-id="df786-131">x</span><span class="sxs-lookup"><span data-stu-id="df786-131">x</span></span>    | <span data-ttu-id="df786-132">x</span><span class="sxs-lookup"><span data-stu-id="df786-132">x</span></span>     |



 

<span data-ttu-id="df786-133">Esta instrucción realiza la resta que se muestra en esta fórmula.</span><span class="sxs-lookup"><span data-stu-id="df786-133">This instruction performs the subtraction shown in this formula.</span></span>


```
dest = src0 - src1
```



## <a name="related-topics"></a><span data-ttu-id="df786-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="df786-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df786-135">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="df786-135">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




