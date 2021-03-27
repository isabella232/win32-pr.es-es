---
title: Agregar vs
description: Agrega dos vectores. | Agregar vs
ms.assetid: f66d3264-68be-4a4f-84fc-cc0f6c4245c9
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 678e7f815a819be2abf1d985516fe081d3c09c94
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "103914314"
---
# <a name="add---vs"></a><span data-ttu-id="a5b0c-104">Agregar vs</span><span class="sxs-lookup"><span data-stu-id="a5b0c-104">add - vs</span></span>

<span data-ttu-id="a5b0c-105">Agrega dos vectores.</span><span class="sxs-lookup"><span data-stu-id="a5b0c-105">Adds two vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5b0c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a5b0c-106">Syntax</span></span>



| <span data-ttu-id="a5b0c-107">Agregar DST, src0, SRC1</span><span class="sxs-lookup"><span data-stu-id="a5b0c-107">add dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="a5b0c-108">, donde</span><span class="sxs-lookup"><span data-stu-id="a5b0c-108">where</span></span>

-   <span data-ttu-id="a5b0c-109">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="a5b0c-109">dst is the destination register.</span></span>
-   <span data-ttu-id="a5b0c-110">src0 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="a5b0c-110">src0 is a source register.</span></span>
-   <span data-ttu-id="a5b0c-111">SRC1 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="a5b0c-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5b0c-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a5b0c-112">Remarks</span></span>



| <span data-ttu-id="a5b0c-113">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="a5b0c-113">Vertex shader versions</span></span> | <span data-ttu-id="a5b0c-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="a5b0c-114">1\_1</span></span> | <span data-ttu-id="a5b0c-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a5b0c-115">2\_0</span></span> | <span data-ttu-id="a5b0c-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="a5b0c-116">2\_x</span></span> | <span data-ttu-id="a5b0c-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a5b0c-117">2\_sw</span></span> | <span data-ttu-id="a5b0c-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a5b0c-118">3\_0</span></span> | <span data-ttu-id="a5b0c-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a5b0c-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="a5b0c-120">add</span><span class="sxs-lookup"><span data-stu-id="a5b0c-120">add</span></span>                    | <span data-ttu-id="a5b0c-121">x</span><span class="sxs-lookup"><span data-stu-id="a5b0c-121">x</span></span>    | <span data-ttu-id="a5b0c-122">x</span><span class="sxs-lookup"><span data-stu-id="a5b0c-122">x</span></span>    | <span data-ttu-id="a5b0c-123">x</span><span class="sxs-lookup"><span data-stu-id="a5b0c-123">x</span></span>    | <span data-ttu-id="a5b0c-124">x</span><span class="sxs-lookup"><span data-stu-id="a5b0c-124">x</span></span>     | <span data-ttu-id="a5b0c-125">x</span><span class="sxs-lookup"><span data-stu-id="a5b0c-125">x</span></span>    | <span data-ttu-id="a5b0c-126">x</span><span class="sxs-lookup"><span data-stu-id="a5b0c-126">x</span></span>     |



 

<span data-ttu-id="a5b0c-127">En el siguiente fragmento de código se muestran las operaciones realizadas.</span><span class="sxs-lookup"><span data-stu-id="a5b0c-127">The following code fragment shows the operations performed.</span></span>


```
dest.x = src0.x + src1.x;
dest.y = src0.y + src1.y;
dest.z = src0.z + src1.z;
dest.w = src0.w + src1.w;
```



## <a name="related-topics"></a><span data-ttu-id="a5b0c-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a5b0c-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5b0c-129">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="a5b0c-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




