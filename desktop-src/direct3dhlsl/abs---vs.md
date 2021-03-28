---
title: ABS-vs
description: Calcula el valor absoluto. | ABS-vs
ms.assetid: d3b4cf06-dc87-4c71-aa2d-5ade4cf98caa
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 07667954de97e2a1da3999237930fb33796d9030
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104279934"
---
# <a name="abs---vs"></a><span data-ttu-id="af78a-104">ABS-vs</span><span class="sxs-lookup"><span data-stu-id="af78a-104">abs - vs</span></span>

<span data-ttu-id="af78a-105">Calcula el valor absoluto.</span><span class="sxs-lookup"><span data-stu-id="af78a-105">Computes absolute value.</span></span>

## <a name="syntax"></a><span data-ttu-id="af78a-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="af78a-106">Syntax</span></span>



|              |
|--------------|
| <span data-ttu-id="af78a-107">ABS DST, src</span><span class="sxs-lookup"><span data-stu-id="af78a-107">abs dst, src</span></span> |



 

<span data-ttu-id="af78a-108">, donde</span><span class="sxs-lookup"><span data-stu-id="af78a-108">where</span></span>

-   <span data-ttu-id="af78a-109">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="af78a-109">dst is the destination register.</span></span>
-   <span data-ttu-id="af78a-110">src es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="af78a-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="af78a-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="af78a-111">Remarks</span></span>



|                        |      |      |      |       |      |       |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="af78a-112">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="af78a-112">Vertex shader versions</span></span> | <span data-ttu-id="af78a-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="af78a-113">1\_1</span></span> | <span data-ttu-id="af78a-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="af78a-114">2\_0</span></span> | <span data-ttu-id="af78a-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="af78a-115">2\_x</span></span> | <span data-ttu-id="af78a-116">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="af78a-116">2\_sw</span></span> | <span data-ttu-id="af78a-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="af78a-117">3\_0</span></span> | <span data-ttu-id="af78a-118">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="af78a-118">3\_sw</span></span> |
| <span data-ttu-id="af78a-119">abs</span><span class="sxs-lookup"><span data-stu-id="af78a-119">abs</span></span>                    |      | <span data-ttu-id="af78a-120">x</span><span class="sxs-lookup"><span data-stu-id="af78a-120">x</span></span>    | <span data-ttu-id="af78a-121">x</span><span class="sxs-lookup"><span data-stu-id="af78a-121">x</span></span>    | <span data-ttu-id="af78a-122">x</span><span class="sxs-lookup"><span data-stu-id="af78a-122">x</span></span>     | <span data-ttu-id="af78a-123">x</span><span class="sxs-lookup"><span data-stu-id="af78a-123">x</span></span>    | <span data-ttu-id="af78a-124">x</span><span class="sxs-lookup"><span data-stu-id="af78a-124">x</span></span>     |



 

<span data-ttu-id="af78a-125">Esta instrucción funciona como se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="af78a-125">This instruction works as shown here.</span></span>


```
dest.x = abs(src.x)
dest.y = abs(src.y)
dest.z = abs(src.z)
dest.w = abs(src.w)
```



## <a name="related-topics"></a><span data-ttu-id="af78a-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="af78a-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af78a-127">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="af78a-127">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




