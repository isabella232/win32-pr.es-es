---
title: Mad-vs
description: Multiplica y agrega orígenes.
ms.assetid: 059f0bf6-d143-4efc-b074-0ed026edb008
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 01e96bb63395fe9e5dd27a17fbb5c0ddd9bf3c17
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104358483"
---
# <a name="mad---vs"></a><span data-ttu-id="7b318-103">Mad-vs</span><span class="sxs-lookup"><span data-stu-id="7b318-103">mad - vs</span></span>

<span data-ttu-id="7b318-104">Multiplica y agrega orígenes.</span><span class="sxs-lookup"><span data-stu-id="7b318-104">Multiplies and adds sources.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b318-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7b318-105">Syntax</span></span>



| <span data-ttu-id="7b318-106">Mad DST, src0, SRC1, src2</span><span class="sxs-lookup"><span data-stu-id="7b318-106">mad dst, src0, src1, src2</span></span> |
|---------------------------|



 

<span data-ttu-id="7b318-107">, donde</span><span class="sxs-lookup"><span data-stu-id="7b318-107">where</span></span>

-   <span data-ttu-id="7b318-108">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="7b318-108">dst is the destination register.</span></span>
-   <span data-ttu-id="7b318-109">src0 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="7b318-109">src0 is a source register.</span></span>
-   <span data-ttu-id="7b318-110">SRC1 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="7b318-110">src1 is a source register.</span></span>
-   <span data-ttu-id="7b318-111">src2 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="7b318-111">src2 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b318-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7b318-112">Remarks</span></span>



| <span data-ttu-id="7b318-113">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="7b318-113">Vertex shader versions</span></span> | <span data-ttu-id="7b318-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="7b318-114">1\_1</span></span> | <span data-ttu-id="7b318-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7b318-115">2\_0</span></span> | <span data-ttu-id="7b318-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="7b318-116">2\_x</span></span> | <span data-ttu-id="7b318-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7b318-117">2\_sw</span></span> | <span data-ttu-id="7b318-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7b318-118">3\_0</span></span> | <span data-ttu-id="7b318-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7b318-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="7b318-120">Mad</span><span class="sxs-lookup"><span data-stu-id="7b318-120">mad</span></span>                    | <span data-ttu-id="7b318-121">x</span><span class="sxs-lookup"><span data-stu-id="7b318-121">x</span></span>    | <span data-ttu-id="7b318-122">x</span><span class="sxs-lookup"><span data-stu-id="7b318-122">x</span></span>    | <span data-ttu-id="7b318-123">x</span><span class="sxs-lookup"><span data-stu-id="7b318-123">x</span></span>    | <span data-ttu-id="7b318-124">x</span><span class="sxs-lookup"><span data-stu-id="7b318-124">x</span></span>     | <span data-ttu-id="7b318-125">x</span><span class="sxs-lookup"><span data-stu-id="7b318-125">x</span></span>    | <span data-ttu-id="7b318-126">x</span><span class="sxs-lookup"><span data-stu-id="7b318-126">x</span></span>     |



 

<span data-ttu-id="7b318-127">En el siguiente fragmento de código se muestran las operaciones realizadas.</span><span class="sxs-lookup"><span data-stu-id="7b318-127">The following code fragment shows the operations performed.</span></span>


```
dest.x = src0.x * src1.x + src2.x;
dest.y = src0.y * src1.y + src2.y;
dest.z = src0.z * src1.z + src2.z;
dest.w = src0.w * src1.w + src2.w;
```



## <a name="related-topics"></a><span data-ttu-id="7b318-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7b318-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b318-129">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="7b318-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




