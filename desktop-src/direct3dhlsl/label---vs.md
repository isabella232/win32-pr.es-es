---
title: etiqueta-frente
description: Marque la instrucción siguiente como un índice de etiqueta. | etiqueta-frente
ms.assetid: e1aee8bc-4655-4bd5-8012-bd7a2d46e712
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6e2b72fe21301aa66d8428dc3696ceb3f12e6214
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998238"
---
# <a name="label---vs"></a><span data-ttu-id="d7f2d-104">etiqueta-frente</span><span class="sxs-lookup"><span data-stu-id="d7f2d-104">label - vs</span></span>

<span data-ttu-id="d7f2d-105">Marque la instrucción siguiente como un índice de etiqueta.</span><span class="sxs-lookup"><span data-stu-id="d7f2d-105">Mark the next instruction as having a label index.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7f2d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d7f2d-106">Syntax</span></span>



| <span data-ttu-id="d7f2d-107">etiqueta l\#</span><span class="sxs-lookup"><span data-stu-id="d7f2d-107">label l\#</span></span> |
|-----------|



 

<span data-ttu-id="d7f2d-108">donde \# identifica el número de etiqueta.</span><span class="sxs-lookup"><span data-stu-id="d7f2d-108">where \# identifies the label number.</span></span>

<span data-ttu-id="d7f2d-109">Para vs \_ 2 \_ 0 y vs \_ 2 \_ x, el número de etiqueta debe estar entre 0 y 15.</span><span class="sxs-lookup"><span data-stu-id="d7f2d-109">For vs\_2\_0, and vs\_2\_x, the label number must be between between 0 and 15.</span></span>

<span data-ttu-id="d7f2d-110">En vs \_ 2 \_ SW, vs \_ 3 \_ 0 y vs \_ 3 \_ SW, el número de etiqueta debe estar entre 0 y 2047.</span><span class="sxs-lookup"><span data-stu-id="d7f2d-110">For vs\_2\_sw, vs\_3\_0 and vs\_3\_sw, the label number must be between between 0 and 2047.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7f2d-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d7f2d-111">Remarks</span></span>



| <span data-ttu-id="d7f2d-112">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="d7f2d-112">Vertex shader versions</span></span> | <span data-ttu-id="d7f2d-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="d7f2d-113">1\_1</span></span> | <span data-ttu-id="d7f2d-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d7f2d-114">2\_0</span></span> | <span data-ttu-id="d7f2d-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="d7f2d-115">2\_x</span></span> | <span data-ttu-id="d7f2d-116">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="d7f2d-116">2\_sw</span></span> | <span data-ttu-id="d7f2d-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d7f2d-117">3\_0</span></span> | <span data-ttu-id="d7f2d-118">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="d7f2d-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="d7f2d-119">etiqueta</span><span class="sxs-lookup"><span data-stu-id="d7f2d-119">label</span></span>                  |      | <span data-ttu-id="d7f2d-120">x</span><span class="sxs-lookup"><span data-stu-id="d7f2d-120">x</span></span>    | <span data-ttu-id="d7f2d-121">x</span><span class="sxs-lookup"><span data-stu-id="d7f2d-121">x</span></span>    | <span data-ttu-id="d7f2d-122">x</span><span class="sxs-lookup"><span data-stu-id="d7f2d-122">x</span></span>     | <span data-ttu-id="d7f2d-123">x</span><span class="sxs-lookup"><span data-stu-id="d7f2d-123">x</span></span>    | <span data-ttu-id="d7f2d-124">x</span><span class="sxs-lookup"><span data-stu-id="d7f2d-124">x</span></span>     |



 

<span data-ttu-id="d7f2d-125">Esta instrucción define una etiqueta que se encuentra en la siguiente instrucción del sombreador.</span><span class="sxs-lookup"><span data-stu-id="d7f2d-125">This instruction defines a label located at the next shader instruction.</span></span> <span data-ttu-id="d7f2d-126">La instrucción de etiqueta solo puede estar presente directamente después de una instrucción [RET](ret---vs.md) (que define el final de la subrutina o el programa principal anterior).</span><span class="sxs-lookup"><span data-stu-id="d7f2d-126">The label instruction can only be present directly after a [ret](ret---vs.md) instruction (which defines the end of the previous subroutine or main program).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d7f2d-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d7f2d-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7f2d-128">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="d7f2d-128">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




