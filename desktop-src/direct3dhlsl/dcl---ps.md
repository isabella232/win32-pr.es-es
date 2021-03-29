---
title: 'DCL: (SM2, SM3-PS ASM)'
description: Declare un registro de entrada del sombreador de píxeles.
ms.assetid: d6fcd94e-80d7-4e8a-8b4f-ff86c980cc38
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ad61ea8d733ed01fcd2e57ba06c38e0b3efac682
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419959"
---
# <a name="dcl---sm2-sm3---ps-asm"></a><span data-ttu-id="95895-103">DCL: (SM2, SM3-PS ASM)</span><span class="sxs-lookup"><span data-stu-id="95895-103">dcl - (sm2, sm3 - ps asm)</span></span>

<span data-ttu-id="95895-104">Declare un registro de entrada del sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="95895-104">Declare a pixel shader input register.</span></span>

## <a name="syntax"></a><span data-ttu-id="95895-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="95895-105">Syntax</span></span>



|                           |
|---------------------------|
| <span data-ttu-id="95895-106">DCL \[ \_ PP \] dest \[ . Mask\]</span><span class="sxs-lookup"><span data-stu-id="95895-106">dcl\[\_pp\] dest\[.mask\]</span></span> |



 

<span data-ttu-id="95895-107">Donde:</span><span class="sxs-lookup"><span data-stu-id="95895-107">Where:</span></span>

-   <span data-ttu-id="95895-108">\[\_PP \] es una precisión parcial opcional.</span><span class="sxs-lookup"><span data-stu-id="95895-108">\[\_pp\] is optional partial precision.</span></span> <span data-ttu-id="95895-109">Vea [precisión parcial](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md).</span><span class="sxs-lookup"><span data-stu-id="95895-109">See [Partial Precision](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md).</span></span>
-   <span data-ttu-id="95895-110">dest es un registro de destino.</span><span class="sxs-lookup"><span data-stu-id="95895-110">dest is a destination register.</span></span> <span data-ttu-id="95895-111">Debe ser un registro de [color de entrada](dx9-graphics-reference-asm-ps-registers-input-color.md) (VN) o un [registro de coordenadas de textura](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (TN).</span><span class="sxs-lookup"><span data-stu-id="95895-111">It must be either a [Input Color Register](dx9-graphics-reference-asm-ps-registers-input-color.md) (vn), or an [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (tn).</span></span>
-   <span data-ttu-id="95895-112">\[. Mask \] es una máscara de escritura opcional que controla los componentes del registro de destino en los que se puede escribir.</span><span class="sxs-lookup"><span data-stu-id="95895-112">\[.mask\] is an optional write mask that controls which components of the destination register that can be written to.</span></span> <span data-ttu-id="95895-113">Consulte [máscara de escritura de registro de destino](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).</span><span class="sxs-lookup"><span data-stu-id="95895-113">See [Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="95895-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="95895-114">Remarks</span></span>



| <span data-ttu-id="95895-115">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="95895-115">Pixel shader versions</span></span> | <span data-ttu-id="95895-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="95895-116">1\_1</span></span> | <span data-ttu-id="95895-117">1\_2</span><span class="sxs-lookup"><span data-stu-id="95895-117">1\_2</span></span> | <span data-ttu-id="95895-118">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="95895-118">1\_3</span></span> | <span data-ttu-id="95895-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="95895-119">1\_4</span></span> | <span data-ttu-id="95895-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="95895-120">2\_0</span></span> | <span data-ttu-id="95895-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="95895-121">2\_x</span></span> | <span data-ttu-id="95895-122">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="95895-122">2\_sw</span></span> | <span data-ttu-id="95895-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="95895-123">3\_0</span></span> | <span data-ttu-id="95895-124">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="95895-124">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="95895-125">DCL</span><span class="sxs-lookup"><span data-stu-id="95895-125">dcl</span></span>                   |      |      |      |      | <span data-ttu-id="95895-126">x</span><span class="sxs-lookup"><span data-stu-id="95895-126">x</span></span>    | <span data-ttu-id="95895-127">x</span><span class="sxs-lookup"><span data-stu-id="95895-127">x</span></span>    | <span data-ttu-id="95895-128">x</span><span class="sxs-lookup"><span data-stu-id="95895-128">x</span></span>     | <span data-ttu-id="95895-129">x</span><span class="sxs-lookup"><span data-stu-id="95895-129">x</span></span>    | <span data-ttu-id="95895-130">x</span><span class="sxs-lookup"><span data-stu-id="95895-130">x</span></span>     |



 

<span data-ttu-id="95895-131">Todas las instrucciones de DCL deben aparecer antes de la primera instrucción ejecutable.</span><span class="sxs-lookup"><span data-stu-id="95895-131">All dcl instructions must appear before the first executable instruction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="95895-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="95895-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95895-133">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="95895-133">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




