---
title: DP4-vs
description: Calcula el producto de cuatro componentes de los registros de origen. | DP4-vs
ms.assetid: ee3d3c8d-6031-4264-80ba-2b200a721310
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 747695436094dd5d2e9787e3eeca525b292f14c4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986362"
---
# <a name="dp4---vs"></a><span data-ttu-id="29929-104">DP4-vs</span><span class="sxs-lookup"><span data-stu-id="29929-104">dp4 - vs</span></span>

<span data-ttu-id="29929-105">Calcula el producto de cuatro componentes de los registros de origen.</span><span class="sxs-lookup"><span data-stu-id="29929-105">Computes the four-component dot product of the source registers.</span></span>

## <a name="syntax"></a><span data-ttu-id="29929-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="29929-106">Syntax</span></span>



| <span data-ttu-id="29929-107">DP4 DST, src0, SRC1</span><span class="sxs-lookup"><span data-stu-id="29929-107">dp4 dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="29929-108">, donde</span><span class="sxs-lookup"><span data-stu-id="29929-108">where</span></span>

-   <span data-ttu-id="29929-109">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="29929-109">dst is the destination register.</span></span>
-   <span data-ttu-id="29929-110">src0 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="29929-110">src0 is a source register.</span></span>
-   <span data-ttu-id="29929-111">SRC1 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="29929-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="29929-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="29929-112">Remarks</span></span>



| <span data-ttu-id="29929-113">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="29929-113">Vertex shader versions</span></span> | <span data-ttu-id="29929-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="29929-114">1\_1</span></span> | <span data-ttu-id="29929-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="29929-115">2\_0</span></span> | <span data-ttu-id="29929-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="29929-116">2\_x</span></span> | <span data-ttu-id="29929-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="29929-117">2\_sw</span></span> | <span data-ttu-id="29929-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="29929-118">3\_0</span></span> | <span data-ttu-id="29929-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="29929-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="29929-120">dp4</span><span class="sxs-lookup"><span data-stu-id="29929-120">dp4</span></span>                    | <span data-ttu-id="29929-121">x</span><span class="sxs-lookup"><span data-stu-id="29929-121">x</span></span>    | <span data-ttu-id="29929-122">x</span><span class="sxs-lookup"><span data-stu-id="29929-122">x</span></span>    | <span data-ttu-id="29929-123">x</span><span class="sxs-lookup"><span data-stu-id="29929-123">x</span></span>    | <span data-ttu-id="29929-124">x</span><span class="sxs-lookup"><span data-stu-id="29929-124">x</span></span>     | <span data-ttu-id="29929-125">x</span><span class="sxs-lookup"><span data-stu-id="29929-125">x</span></span>    | <span data-ttu-id="29929-126">x</span><span class="sxs-lookup"><span data-stu-id="29929-126">x</span></span>     |



 

<span data-ttu-id="29929-127">En el siguiente fragmento de código se muestran las operaciones realizadas:</span><span class="sxs-lookup"><span data-stu-id="29929-127">The following code fragment shows the operations performed:</span></span>


```
dest.w = (src0.x * src1.x) + (src0.y * src1.y) + 
         (src0.z * src1.z) + (src0.w * src1.w);
dest.x = dest.y = dest.z = dest.w;
```



## <a name="related-topics"></a><span data-ttu-id="29929-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="29929-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29929-129">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="29929-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




