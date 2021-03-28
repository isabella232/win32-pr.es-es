---
title: DSY-PS
description: Calcula la tasa de cambio en la dirección y del destino de representación.
ms.assetid: b35862d7-fc43-4cf8-bfe3-3eccbda2a133
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c5f595d836ed8eb8525175ddb81e743cb7a04811
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419907"
---
# <a name="dsy---ps"></a><span data-ttu-id="42ac0-103">DSY-PS</span><span class="sxs-lookup"><span data-stu-id="42ac0-103">dsy - ps</span></span>

<span data-ttu-id="42ac0-104">Calcula la tasa de cambio en la dirección y del destino de representación.</span><span class="sxs-lookup"><span data-stu-id="42ac0-104">Compute the rate of change in the render target's y-direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="42ac0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="42ac0-105">Syntax</span></span>



| <span data-ttu-id="42ac0-106">DSY DST, src</span><span class="sxs-lookup"><span data-stu-id="42ac0-106">dsy dst, src</span></span> |
|--------------|



 

<span data-ttu-id="42ac0-107">Donde:</span><span class="sxs-lookup"><span data-stu-id="42ac0-107">Where:</span></span>

-   <span data-ttu-id="42ac0-108">DST es un registro de destino.</span><span class="sxs-lookup"><span data-stu-id="42ac0-108">dst is a destination register.</span></span>
-   <span data-ttu-id="42ac0-109">src es un registro de origen de entrada.</span><span class="sxs-lookup"><span data-stu-id="42ac0-109">src is an input source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="42ac0-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="42ac0-110">Remarks</span></span>



| <span data-ttu-id="42ac0-111">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="42ac0-111">Pixel shader versions</span></span> | <span data-ttu-id="42ac0-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="42ac0-112">1\_1</span></span> | <span data-ttu-id="42ac0-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="42ac0-113">1\_2</span></span> | <span data-ttu-id="42ac0-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="42ac0-114">1\_3</span></span> | <span data-ttu-id="42ac0-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="42ac0-115">1\_4</span></span> | <span data-ttu-id="42ac0-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="42ac0-116">2\_0</span></span> | <span data-ttu-id="42ac0-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="42ac0-117">2\_x</span></span> | <span data-ttu-id="42ac0-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="42ac0-118">2\_sw</span></span> | <span data-ttu-id="42ac0-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="42ac0-119">3\_0</span></span> | <span data-ttu-id="42ac0-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="42ac0-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="42ac0-121">dsy</span><span class="sxs-lookup"><span data-stu-id="42ac0-121">dsy</span></span>                   |      |      |      |      |      | <span data-ttu-id="42ac0-122">x</span><span class="sxs-lookup"><span data-stu-id="42ac0-122">x</span></span>    | <span data-ttu-id="42ac0-123">x</span><span class="sxs-lookup"><span data-stu-id="42ac0-123">x</span></span>     | <span data-ttu-id="42ac0-124">x</span><span class="sxs-lookup"><span data-stu-id="42ac0-124">x</span></span>    | <span data-ttu-id="42ac0-125">x</span><span class="sxs-lookup"><span data-stu-id="42ac0-125">x</span></span>     |



 

<span data-ttu-id="42ac0-126">La tasa de cambio calculada a partir del registro de origen es una aproximación en el contenido del mismo registro en píxeles adyacentes que ejecutan el sombreador de píxeles en el paso de bloqueo con el píxel actual.</span><span class="sxs-lookup"><span data-stu-id="42ac0-126">The rate of change computed from the source register is an approximation on the contents of the same register in adjacent pixel(s) running the pixel shader in lock-step with the current pixel.</span></span>

<span data-ttu-id="42ac0-127">Las instrucciones [DSX](dsx---ps.md) y DSY calculan su resultado examinando el contenido actual del registro de origen (por componente) para los distintos píxeles del área local que se ejecuta en el paso de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="42ac0-127">The [dsx](dsx---ps.md) And dsy instructions compute their result by looking at the current contents of the source register (per component) for the various pixels in the local area executing in the lock-step.</span></span> <span data-ttu-id="42ac0-128">La fórmula exacta que se usa para calcular el degradado varía en función del hardware, pero debe ser coherente con la manera en que el hardware realiza las mismas operaciones como parte del proceso de cálculo del nivel de detalle para el muestreo de textura.</span><span class="sxs-lookup"><span data-stu-id="42ac0-128">The exact formula used to compute the gradient varies depending on the hardware but should be consistent with the way the hardware does the same operations as part of the level-of-detail calculation process for texture sampling.</span></span>

## <a name="related-topics"></a><span data-ttu-id="42ac0-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="42ac0-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42ac0-130">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="42ac0-130">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[<span data-ttu-id="42ac0-131">texldd-PS</span><span class="sxs-lookup"><span data-stu-id="42ac0-131">texldd - ps</span></span>](texldd---ps.md)
</dt> </dl>

 

 




