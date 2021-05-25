---
title: abs - vs
description: Calcula el valor absoluto. | abs - vs
ms.assetid: d3b4cf06-dc87-4c71-aa2d-5ade4cf98caa
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 612ed14fb538a419a0e7f0b1cf07904d654bb010
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343320"
---
# <a name="abs---vs"></a><span data-ttu-id="07e38-104">abs - vs</span><span class="sxs-lookup"><span data-stu-id="07e38-104">abs - vs</span></span>

<span data-ttu-id="07e38-105">Calcula el valor absoluto.</span><span class="sxs-lookup"><span data-stu-id="07e38-105">Computes absolute value.</span></span>

## <a name="syntax"></a><span data-ttu-id="07e38-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="07e38-106">Syntax</span></span>

<span data-ttu-id="07e38-107">**abs dst, src**</span><span class="sxs-lookup"><span data-stu-id="07e38-107">**abs dst, src**</span></span>

<span data-ttu-id="07e38-108">where</span><span class="sxs-lookup"><span data-stu-id="07e38-108">where</span></span>

- <span data-ttu-id="07e38-109">dst es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="07e38-109">dst is the destination register.</span></span>
- <span data-ttu-id="07e38-110">src es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="07e38-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="07e38-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="07e38-111">Remarks</span></span>



| <span data-ttu-id="07e38-112">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="07e38-112">Vertex shader versions</span></span> | <span data-ttu-id="07e38-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="07e38-113">1\_1</span></span> | <span data-ttu-id="07e38-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="07e38-114">2\_0</span></span> | <span data-ttu-id="07e38-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="07e38-115">2\_x</span></span> | <span data-ttu-id="07e38-116">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="07e38-116">2\_sw</span></span> | <span data-ttu-id="07e38-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="07e38-117">3\_0</span></span> | <span data-ttu-id="07e38-118">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="07e38-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="07e38-119">abs</span><span class="sxs-lookup"><span data-stu-id="07e38-119">abs</span></span>                    |      | <span data-ttu-id="07e38-120">x</span><span class="sxs-lookup"><span data-stu-id="07e38-120">x</span></span>    | <span data-ttu-id="07e38-121">x</span><span class="sxs-lookup"><span data-stu-id="07e38-121">x</span></span>    | <span data-ttu-id="07e38-122">x</span><span class="sxs-lookup"><span data-stu-id="07e38-122">x</span></span>     | <span data-ttu-id="07e38-123">x</span><span class="sxs-lookup"><span data-stu-id="07e38-123">x</span></span>    | <span data-ttu-id="07e38-124">x</span><span class="sxs-lookup"><span data-stu-id="07e38-124">x</span></span>     |



 

<span data-ttu-id="07e38-125">Esta instrucción funciona como se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="07e38-125">This instruction works as shown here.</span></span>


```
dest.x = abs(src.x)
dest.y = abs(src.y)
dest.z = abs(src.z)
dest.w = abs(src.w)
```



## <a name="related-topics"></a><span data-ttu-id="07e38-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="07e38-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07e38-127">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="07e38-127">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




