---
title: RSQ-vs
description: Calcula la raíz cuadrada recíproca (solo positivo) del escalar de origen. | RSQ-vs
ms.assetid: 1ac37dad-0cea-41af-8dae-f299896462b1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f477d6f7d8a7ff94472c689bf5844183e2f016ee
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986559"
---
# <a name="rsq---vs"></a><span data-ttu-id="4e3db-104">RSQ-vs</span><span class="sxs-lookup"><span data-stu-id="4e3db-104">rsq - vs</span></span>

<span data-ttu-id="4e3db-105">Calcula la raíz cuadrada recíproca (solo positivo) del escalar de origen.</span><span class="sxs-lookup"><span data-stu-id="4e3db-105">Computes the reciprocal square root (positive only) of the source scalar.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e3db-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4e3db-106">Syntax</span></span>



| <span data-ttu-id="4e3db-107">RSQ DST, src</span><span class="sxs-lookup"><span data-stu-id="4e3db-107">rsq dst, src</span></span> |
|--------------|



 

<span data-ttu-id="4e3db-108">, donde</span><span class="sxs-lookup"><span data-stu-id="4e3db-108">where</span></span>

-   <span data-ttu-id="4e3db-109">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="4e3db-109">dst is the destination register.</span></span>
-   <span data-ttu-id="4e3db-110">src es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="4e3db-110">src is a source register.</span></span> <span data-ttu-id="4e3db-111">El registro de origen requiere el uso explícito de replicate swizzle, es decir, se debe especificar exactamente uno de los componentes. x,. y,. z,. w swizzle (o. r,. g,. b,. a equivalentes).</span><span class="sxs-lookup"><span data-stu-id="4e3db-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e3db-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4e3db-112">Remarks</span></span>



| <span data-ttu-id="4e3db-113">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="4e3db-113">Vertex shader versions</span></span> | <span data-ttu-id="4e3db-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="4e3db-114">1\_1</span></span> | <span data-ttu-id="4e3db-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4e3db-115">2\_0</span></span> | <span data-ttu-id="4e3db-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="4e3db-116">2\_x</span></span> | <span data-ttu-id="4e3db-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4e3db-117">2\_sw</span></span> | <span data-ttu-id="4e3db-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4e3db-118">3\_0</span></span> | <span data-ttu-id="4e3db-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4e3db-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="4e3db-120">rsq</span><span class="sxs-lookup"><span data-stu-id="4e3db-120">rsq</span></span>                    | <span data-ttu-id="4e3db-121">x</span><span class="sxs-lookup"><span data-stu-id="4e3db-121">x</span></span>    | <span data-ttu-id="4e3db-122">x</span><span class="sxs-lookup"><span data-stu-id="4e3db-122">x</span></span>    | <span data-ttu-id="4e3db-123">x</span><span class="sxs-lookup"><span data-stu-id="4e3db-123">x</span></span>    | <span data-ttu-id="4e3db-124">x</span><span class="sxs-lookup"><span data-stu-id="4e3db-124">x</span></span>     | <span data-ttu-id="4e3db-125">x</span><span class="sxs-lookup"><span data-stu-id="4e3db-125">x</span></span>    | <span data-ttu-id="4e3db-126">x</span><span class="sxs-lookup"><span data-stu-id="4e3db-126">x</span></span>     |



 

<span data-ttu-id="4e3db-127">En el siguiente fragmento de código se muestran las operaciones realizadas.</span><span class="sxs-lookup"><span data-stu-id="4e3db-127">The following code fragment shows the operations performed.</span></span>


```
float f = abs(src0);
if (f == 0)
    f = FLT_MAX
else
{
    if (f != 1.0)
        f = 1.0/(float)sqrt(f);
}

dest.z = dest.y = dest.z = dest.w = f;
```



<span data-ttu-id="4e3db-128">El valor absoluto se toma antes del procesamiento.</span><span class="sxs-lookup"><span data-stu-id="4e3db-128">The absolute value is taken before processing.</span></span>

<span data-ttu-id="4e3db-129">La precisión debe ser al menos de 1,0/(2 ² ²) error absoluto en el intervalo (1,0, 4,0) porque las implementaciones comunes separan la mantisa y el exponente.</span><span class="sxs-lookup"><span data-stu-id="4e3db-129">Precision should be at least 1.0/(2²²) absolute error over the range (1.0, 4.0) because common implementations will separate mantissa and exponent.</span></span>

<span data-ttu-id="4e3db-130">Si el origen no tiene ningún subíndice, se usa el componente x.</span><span class="sxs-lookup"><span data-stu-id="4e3db-130">If source has no subscripts, the x-component is used.</span></span> <span data-ttu-id="4e3db-131">La salida debe ser exactamente 1,0 si la entrada es exactamente 1,0.</span><span class="sxs-lookup"><span data-stu-id="4e3db-131">The output must be exactly 1.0 if the input is exactly 1.0.</span></span> <span data-ttu-id="4e3db-132">Un origen de 0,0 produce infinito.</span><span class="sxs-lookup"><span data-stu-id="4e3db-132">A source of 0.0 yields infinity.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4e3db-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4e3db-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e3db-134">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="4e3db-134">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




