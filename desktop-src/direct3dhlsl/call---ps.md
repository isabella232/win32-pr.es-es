---
title: llamada a PS
description: Realiza una llamada de función a la instrucción marcada con la etiqueta proporcionada. | llamada a PS
ms.assetid: d5f5e5a1-f205-477d-a11b-ff9eeeec6c95
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 27be29c478afdf92c29fefd16a82319e0899d2ec
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998113"
---
# <a name="call---ps"></a><span data-ttu-id="c838b-104">llamada a PS</span><span class="sxs-lookup"><span data-stu-id="c838b-104">call - ps</span></span>

<span data-ttu-id="c838b-105">Realiza una llamada de función a la instrucción marcada con la etiqueta proporcionada.</span><span class="sxs-lookup"><span data-stu-id="c838b-105">Performs a function call to the instruction marked with the provided label.</span></span>

## <a name="syntax"></a><span data-ttu-id="c838b-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c838b-106">Syntax</span></span>



| <span data-ttu-id="c838b-107">llamar a l\#</span><span class="sxs-lookup"><span data-stu-id="c838b-107">call l\#</span></span> |
|----------|



 

<span data-ttu-id="c838b-108">Donde:</span><span class="sxs-lookup"><span data-stu-id="c838b-108">Where:</span></span>

-   <span data-ttu-id="c838b-109">l \# es una [etiqueta-PS](label---ps.md) que marca el principio de la subrutina a la que se va a llamar.</span><span class="sxs-lookup"><span data-stu-id="c838b-109">l\# is a [label - ps](label---ps.md) marking the beginning of the subroutine to be called.</span></span>

## <a name="remarks"></a><span data-ttu-id="c838b-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c838b-110">Remarks</span></span>



| <span data-ttu-id="c838b-111">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="c838b-111">Pixel shader versions</span></span> | <span data-ttu-id="c838b-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="c838b-112">1\_1</span></span> | <span data-ttu-id="c838b-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="c838b-113">1\_2</span></span> | <span data-ttu-id="c838b-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="c838b-114">1\_3</span></span> | <span data-ttu-id="c838b-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="c838b-115">1\_4</span></span> | <span data-ttu-id="c838b-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c838b-116">2\_0</span></span> | <span data-ttu-id="c838b-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c838b-117">2\_x</span></span> | <span data-ttu-id="c838b-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c838b-118">2\_sw</span></span> | <span data-ttu-id="c838b-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c838b-119">3\_0</span></span> | <span data-ttu-id="c838b-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c838b-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="c838b-121">llamada</span><span class="sxs-lookup"><span data-stu-id="c838b-121">call</span></span>                  |      |      |      |      |      | <span data-ttu-id="c838b-122">x</span><span class="sxs-lookup"><span data-stu-id="c838b-122">x</span></span>    | <span data-ttu-id="c838b-123">x</span><span class="sxs-lookup"><span data-stu-id="c838b-123">x</span></span>     | <span data-ttu-id="c838b-124">x</span><span class="sxs-lookup"><span data-stu-id="c838b-124">x</span></span>    | <span data-ttu-id="c838b-125">x</span><span class="sxs-lookup"><span data-stu-id="c838b-125">x</span></span>     |



 

<span data-ttu-id="c838b-126">Esta instrucción hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="c838b-126">This instruction does the following:</span></span>

1.  <span data-ttu-id="c838b-127">Dirección de extracción de la instrucción siguiente a la pila de direcciones devuelta.</span><span class="sxs-lookup"><span data-stu-id="c838b-127">Push address of the next instruction to the return address stack.</span></span>
2.  <span data-ttu-id="c838b-128">Continúe con la ejecución de la instrucción marcada por la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="c838b-128">Continue execution from the instruction marked by the label.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c838b-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c838b-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c838b-130">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="c838b-130">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




