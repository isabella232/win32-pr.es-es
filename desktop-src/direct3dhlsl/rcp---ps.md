---
title: RCP-PS
description: Calcula el recíproco del escalar del origen. | RCP-PS
ms.assetid: d8dfc2b3-4404-47ec-aeaf-1adb7e7a342e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2df8ad2d673d96dced84630b1a641c7e4f27ceb2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986526"
---
# <a name="rcp---ps"></a><span data-ttu-id="3eea7-104">RCP-PS</span><span class="sxs-lookup"><span data-stu-id="3eea7-104">rcp - ps</span></span>

<span data-ttu-id="3eea7-105">Calcula el recíproco del escalar del origen.</span><span class="sxs-lookup"><span data-stu-id="3eea7-105">Computes the reciprocal of the source scalar.</span></span>

## <a name="syntax"></a><span data-ttu-id="3eea7-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3eea7-106">Syntax</span></span>



| <span data-ttu-id="3eea7-107">RCP DST, src</span><span class="sxs-lookup"><span data-stu-id="3eea7-107">rcp dst, src</span></span> |
|--------------|



 

<span data-ttu-id="3eea7-108">, donde</span><span class="sxs-lookup"><span data-stu-id="3eea7-108">where</span></span>

-   <span data-ttu-id="3eea7-109">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="3eea7-109">dst is the destination register.</span></span>
-   <span data-ttu-id="3eea7-110">src es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="3eea7-110">src is a source register.</span></span> <span data-ttu-id="3eea7-111">El registro de origen requiere el uso explícito de replicate swizzle, es decir, se debe especificar exactamente uno de los componentes. x,. y,. z,. w swizzle (o. r,. g,. b,. a equivalentes).</span><span class="sxs-lookup"><span data-stu-id="3eea7-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="3eea7-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3eea7-112">Remarks</span></span>



| <span data-ttu-id="3eea7-113">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="3eea7-113">Pixel shader versions</span></span> | <span data-ttu-id="3eea7-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="3eea7-114">1\_1</span></span> | <span data-ttu-id="3eea7-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="3eea7-115">1\_2</span></span> | <span data-ttu-id="3eea7-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="3eea7-116">1\_3</span></span> | <span data-ttu-id="3eea7-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="3eea7-117">1\_4</span></span> | <span data-ttu-id="3eea7-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3eea7-118">2\_0</span></span> | <span data-ttu-id="3eea7-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="3eea7-119">2\_x</span></span> | <span data-ttu-id="3eea7-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3eea7-120">2\_sw</span></span> | <span data-ttu-id="3eea7-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3eea7-121">3\_0</span></span> | <span data-ttu-id="3eea7-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3eea7-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="3eea7-123">rcp</span><span class="sxs-lookup"><span data-stu-id="3eea7-123">rcp</span></span>                   |      |      |      |      | <span data-ttu-id="3eea7-124">x</span><span class="sxs-lookup"><span data-stu-id="3eea7-124">x</span></span>    | <span data-ttu-id="3eea7-125">x</span><span class="sxs-lookup"><span data-stu-id="3eea7-125">x</span></span>    | <span data-ttu-id="3eea7-126">x</span><span class="sxs-lookup"><span data-stu-id="3eea7-126">x</span></span>     | <span data-ttu-id="3eea7-127">x</span><span class="sxs-lookup"><span data-stu-id="3eea7-127">x</span></span>    | <span data-ttu-id="3eea7-128">x</span><span class="sxs-lookup"><span data-stu-id="3eea7-128">x</span></span>     |



 

<span data-ttu-id="3eea7-129">La salida debe ser exactamente 1,0 si la entrada es exactamente 1,0.</span><span class="sxs-lookup"><span data-stu-id="3eea7-129">The output must be exactly 1.0 if the input is exactly 1.0.</span></span> <span data-ttu-id="3eea7-130">Un origen de 0,0 produce infinito.</span><span class="sxs-lookup"><span data-stu-id="3eea7-130">A source of 0.0 yields infinity.</span></span>

<span data-ttu-id="3eea7-131">El resultado escalar se replica en todos los canales de la máscara de escritura de destino.</span><span class="sxs-lookup"><span data-stu-id="3eea7-131">The scalar result is replicated to all channels in the destination write mask.</span></span>

<span data-ttu-id="3eea7-132">La precisión debe ser al menos de 1,0/(2 ² ²) error absoluto en el intervalo (1,0, 2,0) porque las implementaciones comunes separan la mantisa y el exponente.</span><span class="sxs-lookup"><span data-stu-id="3eea7-132">Precision should be at least 1.0/(2²²) absolute error over the range (1.0, 2.0) because common implementations will separate mantissa and exponent.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3eea7-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3eea7-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3eea7-134">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="3eea7-134">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




