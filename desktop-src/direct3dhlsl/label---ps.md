---
title: etiqueta-PS
description: Marque la instrucción siguiente como un índice de etiqueta. | etiqueta-PS
ms.assetid: 21afa062-c536-4891-ba69-ca5284b0539c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f3fb266b649642c82293e8310b6302c6763ddc27
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998156"
---
# <a name="label---ps"></a><span data-ttu-id="ff4eb-104">etiqueta-PS</span><span class="sxs-lookup"><span data-stu-id="ff4eb-104">label - ps</span></span>

<span data-ttu-id="ff4eb-105">Marque la instrucción siguiente como un índice de etiqueta.</span><span class="sxs-lookup"><span data-stu-id="ff4eb-105">Mark the next instruction as having a label index.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff4eb-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ff4eb-106">Syntax</span></span>



| <span data-ttu-id="ff4eb-107">etiqueta l\#</span><span class="sxs-lookup"><span data-stu-id="ff4eb-107">label l\#</span></span> |
|-----------|



 

<span data-ttu-id="ff4eb-108">donde \# identifica el número de etiqueta.</span><span class="sxs-lookup"><span data-stu-id="ff4eb-108">where \# identifies the label number.</span></span>

<span data-ttu-id="ff4eb-109">Para PS \_ 2 \_ x, el número de etiqueta debe estar entre 0 y 15.</span><span class="sxs-lookup"><span data-stu-id="ff4eb-109">For ps\_2\_x, the label number must be between between 0 and 15.</span></span>

<span data-ttu-id="ff4eb-110">Para PS \_ 2 \_ SW, PS \_ 3 \_ 0 y PS \_ 3 \_ SW, el número de etiqueta debe estar entre 0 y 2047.</span><span class="sxs-lookup"><span data-stu-id="ff4eb-110">For ps\_2\_sw, ps\_3\_0, and ps\_3\_sw, the label number must be between between 0 and 2047.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff4eb-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ff4eb-111">Remarks</span></span>



| <span data-ttu-id="ff4eb-112">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="ff4eb-112">Pixel shader versions</span></span> | <span data-ttu-id="ff4eb-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="ff4eb-113">1\_1</span></span> | <span data-ttu-id="ff4eb-114">1\_2</span><span class="sxs-lookup"><span data-stu-id="ff4eb-114">1\_2</span></span> | <span data-ttu-id="ff4eb-115">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="ff4eb-115">1\_3</span></span> | <span data-ttu-id="ff4eb-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="ff4eb-116">1\_4</span></span> | <span data-ttu-id="ff4eb-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ff4eb-117">2\_0</span></span> | <span data-ttu-id="ff4eb-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="ff4eb-118">2\_x</span></span> | <span data-ttu-id="ff4eb-119">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="ff4eb-119">2\_sw</span></span> | <span data-ttu-id="ff4eb-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ff4eb-120">3\_0</span></span> | <span data-ttu-id="ff4eb-121">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="ff4eb-121">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="ff4eb-122">etiqueta</span><span class="sxs-lookup"><span data-stu-id="ff4eb-122">label</span></span>                 |      |      |      |      |      | <span data-ttu-id="ff4eb-123">x</span><span class="sxs-lookup"><span data-stu-id="ff4eb-123">x</span></span>    | <span data-ttu-id="ff4eb-124">x</span><span class="sxs-lookup"><span data-stu-id="ff4eb-124">x</span></span>     | <span data-ttu-id="ff4eb-125">x</span><span class="sxs-lookup"><span data-stu-id="ff4eb-125">x</span></span>    | <span data-ttu-id="ff4eb-126">x</span><span class="sxs-lookup"><span data-stu-id="ff4eb-126">x</span></span>     |



 

<span data-ttu-id="ff4eb-127">Esta instrucción define una etiqueta que se encuentra en la siguiente instrucción del sombreador.</span><span class="sxs-lookup"><span data-stu-id="ff4eb-127">This instruction defines a label located at the next shader instruction.</span></span> <span data-ttu-id="ff4eb-128">La instrucción de etiqueta solo puede estar presente directamente después de una instrucción [RET](ret---ps.md) (que define el final de la subrutina o el programa principal anterior).</span><span class="sxs-lookup"><span data-stu-id="ff4eb-128">The label instruction can only be present directly after a [ret](ret---ps.md) instruction (which defines the end of the previous subroutine or main program).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ff4eb-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ff4eb-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff4eb-130">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="ff4eb-130">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




