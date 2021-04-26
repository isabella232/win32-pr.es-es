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
ms.openlocfilehash: e4d73ee738f575d93c2316e4ec47dced7cb128d3
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994752"
---
# <a name="abs---vs"></a><span data-ttu-id="5da8f-104">abs - vs</span><span class="sxs-lookup"><span data-stu-id="5da8f-104">abs - vs</span></span>

<span data-ttu-id="5da8f-105">Calcula el valor absoluto.</span><span class="sxs-lookup"><span data-stu-id="5da8f-105">Computes absolute value.</span></span>

## <a name="syntax"></a><span data-ttu-id="5da8f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5da8f-106">Syntax</span></span>



|              |
|--------------|
| <span data-ttu-id="5da8f-107">abs dst, src</span><span class="sxs-lookup"><span data-stu-id="5da8f-107">abs dst, src</span></span> |



 

<span data-ttu-id="5da8f-108">where</span><span class="sxs-lookup"><span data-stu-id="5da8f-108">where</span></span>

-   <span data-ttu-id="5da8f-109">dst es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="5da8f-109">dst is the destination register.</span></span>
-   <span data-ttu-id="5da8f-110">src es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="5da8f-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="5da8f-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5da8f-111">Remarks</span></span>



| <span data-ttu-id="5da8f-112">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="5da8f-112">Vertex shader versions</span></span> | <span data-ttu-id="5da8f-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="5da8f-113">1\_1</span></span> | <span data-ttu-id="5da8f-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5da8f-114">2\_0</span></span> | <span data-ttu-id="5da8f-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5da8f-115">2\_x</span></span> | <span data-ttu-id="5da8f-116">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="5da8f-116">2\_sw</span></span> | <span data-ttu-id="5da8f-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5da8f-117">3\_0</span></span> | <span data-ttu-id="5da8f-118">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="5da8f-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="5da8f-119">abs</span><span class="sxs-lookup"><span data-stu-id="5da8f-119">abs</span></span>                    |      | <span data-ttu-id="5da8f-120">x</span><span class="sxs-lookup"><span data-stu-id="5da8f-120">x</span></span>    | <span data-ttu-id="5da8f-121">x</span><span class="sxs-lookup"><span data-stu-id="5da8f-121">x</span></span>    | <span data-ttu-id="5da8f-122">x</span><span class="sxs-lookup"><span data-stu-id="5da8f-122">x</span></span>     | <span data-ttu-id="5da8f-123">x</span><span class="sxs-lookup"><span data-stu-id="5da8f-123">x</span></span>    | <span data-ttu-id="5da8f-124">x</span><span class="sxs-lookup"><span data-stu-id="5da8f-124">x</span></span>     |



 

<span data-ttu-id="5da8f-125">Esta instrucción funciona como se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="5da8f-125">This instruction works as shown here.</span></span>


```
dest.x = abs(src.x)
dest.y = abs(src.y)
dest.z = abs(src.z)
dest.w = abs(src.w)
```



## <a name="related-topics"></a><span data-ttu-id="5da8f-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5da8f-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5da8f-127">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="5da8f-127">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




