---
title: DP3-vs
description: Calcula el producto de tres componentes de los registros de origen. | DP3-vs
ms.assetid: a5263a18-ed53-41eb-85ca-2cff872e03d8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 81580401f25ddcf7ce1c1d53475d0c3beba74a89
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104279933"
---
# <a name="dp3---vs"></a><span data-ttu-id="2c1d0-104">DP3-vs</span><span class="sxs-lookup"><span data-stu-id="2c1d0-104">dp3 - vs</span></span>

<span data-ttu-id="2c1d0-105">Calcula el producto de tres componentes de los registros de origen.</span><span class="sxs-lookup"><span data-stu-id="2c1d0-105">Computes the three-component dot product of the source registers.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c1d0-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2c1d0-106">Syntax</span></span>



| <span data-ttu-id="2c1d0-107">DP3 DST, src0, SRC1</span><span class="sxs-lookup"><span data-stu-id="2c1d0-107">dp3 dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="2c1d0-108">, donde</span><span class="sxs-lookup"><span data-stu-id="2c1d0-108">where</span></span>

-   <span data-ttu-id="2c1d0-109">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="2c1d0-109">dst is the destination register.</span></span>
-   <span data-ttu-id="2c1d0-110">src0 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="2c1d0-110">src0 is a source register.</span></span>
-   <span data-ttu-id="2c1d0-111">SRC1 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="2c1d0-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c1d0-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2c1d0-112">Remarks</span></span>



| <span data-ttu-id="2c1d0-113">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="2c1d0-113">Vertex shader versions</span></span> | <span data-ttu-id="2c1d0-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="2c1d0-114">1\_1</span></span> | <span data-ttu-id="2c1d0-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2c1d0-115">2\_0</span></span> | <span data-ttu-id="2c1d0-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="2c1d0-116">2\_x</span></span> | <span data-ttu-id="2c1d0-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="2c1d0-117">2\_sw</span></span> | <span data-ttu-id="2c1d0-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2c1d0-118">3\_0</span></span> | <span data-ttu-id="2c1d0-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="2c1d0-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="2c1d0-120">dp3</span><span class="sxs-lookup"><span data-stu-id="2c1d0-120">dp3</span></span>                    | <span data-ttu-id="2c1d0-121">x</span><span class="sxs-lookup"><span data-stu-id="2c1d0-121">x</span></span>    | <span data-ttu-id="2c1d0-122">x</span><span class="sxs-lookup"><span data-stu-id="2c1d0-122">x</span></span>    | <span data-ttu-id="2c1d0-123">x</span><span class="sxs-lookup"><span data-stu-id="2c1d0-123">x</span></span>    | <span data-ttu-id="2c1d0-124">x</span><span class="sxs-lookup"><span data-stu-id="2c1d0-124">x</span></span>     | <span data-ttu-id="2c1d0-125">x</span><span class="sxs-lookup"><span data-stu-id="2c1d0-125">x</span></span>    | <span data-ttu-id="2c1d0-126">x</span><span class="sxs-lookup"><span data-stu-id="2c1d0-126">x</span></span>     |



 

<span data-ttu-id="2c1d0-127">En el siguiente fragmento de código se muestran las operaciones realizadas:</span><span class="sxs-lookup"><span data-stu-id="2c1d0-127">The following code fragment shows the operations performed:</span></span>


```
dest.w = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
dest.x = dest.y = dest.z = dest.w;
```



## <a name="related-topics"></a><span data-ttu-id="2c1d0-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2c1d0-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c1d0-129">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="2c1d0-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




