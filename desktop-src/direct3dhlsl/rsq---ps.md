---
title: RSQ-PS
description: Calcula la raíz cuadrada recíproca (solo positivo) del escalar de origen. | RSQ-PS
ms.assetid: deb1bd12-6347-4b1e-b21b-f3ef48da4c13
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 13777810c67ba38b2c8f47f0c0db0cf9b70771ad
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986435"
---
# <a name="rsq---ps"></a><span data-ttu-id="a5637-104">RSQ-PS</span><span class="sxs-lookup"><span data-stu-id="a5637-104">rsq - ps</span></span>

<span data-ttu-id="a5637-105">Calcula la raíz cuadrada recíproca (solo positivo) del escalar de origen.</span><span class="sxs-lookup"><span data-stu-id="a5637-105">Computes the reciprocal square root (positive only) of the source scalar.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5637-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a5637-106">Syntax</span></span>



| <span data-ttu-id="a5637-107">RSQ DST, src</span><span class="sxs-lookup"><span data-stu-id="a5637-107">rsq dst, src</span></span> |
|--------------|



 

<span data-ttu-id="a5637-108">, donde</span><span class="sxs-lookup"><span data-stu-id="a5637-108">where</span></span>

-   <span data-ttu-id="a5637-109">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="a5637-109">dst is the destination register.</span></span>
-   <span data-ttu-id="a5637-110">src es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="a5637-110">src is a source register.</span></span> <span data-ttu-id="a5637-111">El registro de origen requiere el uso explícito de replicate swizzle, es decir, se debe especificar exactamente uno de los componentes. x,. y,. z,. w swizzle (o. r,. g,. b,. a equivalentes).</span><span class="sxs-lookup"><span data-stu-id="a5637-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5637-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a5637-112">Remarks</span></span>



| <span data-ttu-id="a5637-113">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="a5637-113">Pixel shader versions</span></span> | <span data-ttu-id="a5637-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="a5637-114">1\_1</span></span> | <span data-ttu-id="a5637-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="a5637-115">1\_2</span></span> | <span data-ttu-id="a5637-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="a5637-116">1\_3</span></span> | <span data-ttu-id="a5637-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="a5637-117">1\_4</span></span> | <span data-ttu-id="a5637-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a5637-118">2\_0</span></span> | <span data-ttu-id="a5637-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="a5637-119">2\_x</span></span> | <span data-ttu-id="a5637-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a5637-120">2\_sw</span></span> | <span data-ttu-id="a5637-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a5637-121">3\_0</span></span> | <span data-ttu-id="a5637-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a5637-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="a5637-123">rsq</span><span class="sxs-lookup"><span data-stu-id="a5637-123">rsq</span></span>                   |      |      |      |      | <span data-ttu-id="a5637-124">x</span><span class="sxs-lookup"><span data-stu-id="a5637-124">x</span></span>    | <span data-ttu-id="a5637-125">x</span><span class="sxs-lookup"><span data-stu-id="a5637-125">x</span></span>    | <span data-ttu-id="a5637-126">x</span><span class="sxs-lookup"><span data-stu-id="a5637-126">x</span></span>     | <span data-ttu-id="a5637-127">x</span><span class="sxs-lookup"><span data-stu-id="a5637-127">x</span></span>    | <span data-ttu-id="a5637-128">x</span><span class="sxs-lookup"><span data-stu-id="a5637-128">x</span></span>     |



 

<span data-ttu-id="a5637-129">El valor absoluto se toma antes del procesamiento.</span><span class="sxs-lookup"><span data-stu-id="a5637-129">The absolute value is taken before processing.</span></span>

<span data-ttu-id="a5637-130">La precisión debe ser al menos de 1,0/(2 ² ²) error absoluto en el intervalo (1,0, 4,0) porque las implementaciones comunes separan la mantisa y el exponente.</span><span class="sxs-lookup"><span data-stu-id="a5637-130">Precision should be at least 1.0/(2²²) absolute error over the range (1.0, 4.0) because common implementations will separate mantissa and exponent.</span></span>

<span data-ttu-id="a5637-131">La salida debe ser exactamente 1,0 si la entrada es exactamente 1,0.</span><span class="sxs-lookup"><span data-stu-id="a5637-131">The output must be exactly 1.0 if the input is exactly 1.0.</span></span> <span data-ttu-id="a5637-132">Un origen de 0,0 produce infinito.</span><span class="sxs-lookup"><span data-stu-id="a5637-132">A source of 0.0 yields infinity.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5637-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a5637-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5637-134">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="a5637-134">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




