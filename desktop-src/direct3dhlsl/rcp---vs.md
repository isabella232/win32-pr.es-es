---
title: RCP-vs
description: Calcula el recíproco del escalar del origen. | RCP-vs
ms.assetid: be638a42-b693-461d-ab0a-3a6c0fa1acfc
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 145a998cbca9dc3721d9c7d6ba251d539286a3f1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986683"
---
# <a name="rcp---vs"></a><span data-ttu-id="618eb-104">RCP-vs</span><span class="sxs-lookup"><span data-stu-id="618eb-104">rcp - vs</span></span>

<span data-ttu-id="618eb-105">Calcula el recíproco del escalar del origen.</span><span class="sxs-lookup"><span data-stu-id="618eb-105">Computes the reciprocal of the source scalar.</span></span>

## <a name="syntax"></a><span data-ttu-id="618eb-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="618eb-106">Syntax</span></span>



| <span data-ttu-id="618eb-107">RCP DST, src</span><span class="sxs-lookup"><span data-stu-id="618eb-107">rcp dst, src</span></span> |
|--------------|



 

<span data-ttu-id="618eb-108">, donde</span><span class="sxs-lookup"><span data-stu-id="618eb-108">where</span></span>

-   <span data-ttu-id="618eb-109">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="618eb-109">dst is the destination register.</span></span>
-   <span data-ttu-id="618eb-110">src es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="618eb-110">src is a source register.</span></span> <span data-ttu-id="618eb-111">El registro de origen requiere el uso explícito de replicate swizzle, es decir, se debe especificar exactamente uno de los componentes. x,. y,. z,. w swizzle (o. r,. g,. b,. a equivalentes).</span><span class="sxs-lookup"><span data-stu-id="618eb-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="618eb-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="618eb-112">Remarks</span></span>



| <span data-ttu-id="618eb-113">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="618eb-113">Vertex shader versions</span></span> | <span data-ttu-id="618eb-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="618eb-114">1\_1</span></span> | <span data-ttu-id="618eb-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="618eb-115">2\_0</span></span> | <span data-ttu-id="618eb-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="618eb-116">2\_x</span></span> | <span data-ttu-id="618eb-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="618eb-117">2\_sw</span></span> | <span data-ttu-id="618eb-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="618eb-118">3\_0</span></span> | <span data-ttu-id="618eb-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="618eb-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="618eb-120">rcp</span><span class="sxs-lookup"><span data-stu-id="618eb-120">rcp</span></span>                    | <span data-ttu-id="618eb-121">x</span><span class="sxs-lookup"><span data-stu-id="618eb-121">x</span></span>    | <span data-ttu-id="618eb-122">x</span><span class="sxs-lookup"><span data-stu-id="618eb-122">x</span></span>    | <span data-ttu-id="618eb-123">x</span><span class="sxs-lookup"><span data-stu-id="618eb-123">x</span></span>    | <span data-ttu-id="618eb-124">x</span><span class="sxs-lookup"><span data-stu-id="618eb-124">x</span></span>     | <span data-ttu-id="618eb-125">x</span><span class="sxs-lookup"><span data-stu-id="618eb-125">x</span></span>    | <span data-ttu-id="618eb-126">x</span><span class="sxs-lookup"><span data-stu-id="618eb-126">x</span></span>     |



 

<span data-ttu-id="618eb-127">En el siguiente fragmento de código se muestran las operaciones realizadas.</span><span class="sxs-lookup"><span data-stu-id="618eb-127">The following code fragment shows the operations performed.</span></span>


```
float f = src0;
if(f == 0.0f)
{
    f = FLT_MAX;
}
else 
{
    if(f != 1.0)
    {
        f = 1/f;
    }
}

dest = f;
```



<span data-ttu-id="618eb-128">La salida debe ser exactamente 1,0 si la entrada es exactamente 1,0.</span><span class="sxs-lookup"><span data-stu-id="618eb-128">The output must be exactly 1.0 if the input is exactly 1.0.</span></span> <span data-ttu-id="618eb-129">Un origen de 0,0 produce infinito.</span><span class="sxs-lookup"><span data-stu-id="618eb-129">A source of 0.0 yields infinity.</span></span>

<span data-ttu-id="618eb-130">La precisión debe ser al menos de 1,0/(2 ² ²) error absoluto en el intervalo (1,0, 2,0) porque las implementaciones comunes separan la mantisa y el exponente.</span><span class="sxs-lookup"><span data-stu-id="618eb-130">Precision should be at least 1.0/(2²²) absolute error over the range (1.0, 2.0) because common implementations will separate mantissa and exponent.</span></span>

<span data-ttu-id="618eb-131">Si el origen no tiene ningún subíndice, se usa el componente x.</span><span class="sxs-lookup"><span data-stu-id="618eb-131">If the source has no subscripts, the x-component is used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="618eb-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="618eb-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="618eb-133">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="618eb-133">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




