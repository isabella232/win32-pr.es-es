---
title: mul-vs
description: Multiplica los orígenes en el destino. | mul-vs
ms.assetid: 0b048cc2-b165-418f-893e-6dee28ca5ad3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e33ac35831b19f771f4f5b64d94bcc47c6657db5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998109"
---
# <a name="mul---vs"></a><span data-ttu-id="7a509-104">mul-vs</span><span class="sxs-lookup"><span data-stu-id="7a509-104">mul - vs</span></span>

<span data-ttu-id="7a509-105">Multiplica los orígenes en el destino.</span><span class="sxs-lookup"><span data-stu-id="7a509-105">Multiplies sources into the destination.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a509-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7a509-106">Syntax</span></span>



| <span data-ttu-id="7a509-107">mul DST, src0, SRC1</span><span class="sxs-lookup"><span data-stu-id="7a509-107">mul dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="7a509-108">, donde</span><span class="sxs-lookup"><span data-stu-id="7a509-108">where</span></span>

-   <span data-ttu-id="7a509-109">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="7a509-109">dst is the destination register.</span></span>
-   <span data-ttu-id="7a509-110">src0 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="7a509-110">src0 is a source register.</span></span>
-   <span data-ttu-id="7a509-111">SRC1 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="7a509-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a509-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7a509-112">Remarks</span></span>



| <span data-ttu-id="7a509-113">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="7a509-113">Vertex shader versions</span></span> | <span data-ttu-id="7a509-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="7a509-114">1\_1</span></span> | <span data-ttu-id="7a509-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7a509-115">2\_0</span></span> | <span data-ttu-id="7a509-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="7a509-116">2\_x</span></span> | <span data-ttu-id="7a509-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7a509-117">2\_sw</span></span> | <span data-ttu-id="7a509-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7a509-118">3\_0</span></span> | <span data-ttu-id="7a509-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7a509-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="7a509-120">mul</span><span class="sxs-lookup"><span data-stu-id="7a509-120">mul</span></span>                    | <span data-ttu-id="7a509-121">x</span><span class="sxs-lookup"><span data-stu-id="7a509-121">x</span></span>    | <span data-ttu-id="7a509-122">x</span><span class="sxs-lookup"><span data-stu-id="7a509-122">x</span></span>    | <span data-ttu-id="7a509-123">x</span><span class="sxs-lookup"><span data-stu-id="7a509-123">x</span></span>    | <span data-ttu-id="7a509-124">x</span><span class="sxs-lookup"><span data-stu-id="7a509-124">x</span></span>     | <span data-ttu-id="7a509-125">x</span><span class="sxs-lookup"><span data-stu-id="7a509-125">x</span></span>    | <span data-ttu-id="7a509-126">x</span><span class="sxs-lookup"><span data-stu-id="7a509-126">x</span></span>     |



 

<span data-ttu-id="7a509-127">En el siguiente fragmento de código se muestran las operaciones realizadas.</span><span class="sxs-lookup"><span data-stu-id="7a509-127">The following code fragment shows the operations performed.</span></span>


```
dest.x = src0.x * src1.x;
dest.y = src0.y * src1.y;
dest.z = src0.z * src1.z;
dest.w = src0.w * src1.w;
```



## <a name="related-topics"></a><span data-ttu-id="7a509-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7a509-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a509-129">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="7a509-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




