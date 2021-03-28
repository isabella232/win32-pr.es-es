---
title: RET-vs
description: Se devuelve de una subrutina o de una función principal.
ms.assetid: ee3a6a7a-c068-442f-9f86-c637b5707224
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3b91a9f2fb30dbd243e29043a1655d441215bc75
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104358477"
---
# <a name="ret---vs"></a><span data-ttu-id="64a2a-103">RET-vs</span><span class="sxs-lookup"><span data-stu-id="64a2a-103">ret - vs</span></span>

<span data-ttu-id="64a2a-104">Se devuelve de una subrutina o de una función principal.</span><span class="sxs-lookup"><span data-stu-id="64a2a-104">Return from a subroutine or a main function.</span></span>

## <a name="syntax"></a><span data-ttu-id="64a2a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="64a2a-105">Syntax</span></span>



| <span data-ttu-id="64a2a-106">direcc</span><span class="sxs-lookup"><span data-stu-id="64a2a-106">ret</span></span> |
|-----|



 

## <a name="remarks"></a><span data-ttu-id="64a2a-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="64a2a-107">Remarks</span></span>



| <span data-ttu-id="64a2a-108">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="64a2a-108">Vertex shader versions</span></span> | <span data-ttu-id="64a2a-109">1\_1</span><span class="sxs-lookup"><span data-stu-id="64a2a-109">1\_1</span></span> | <span data-ttu-id="64a2a-110">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="64a2a-110">2\_0</span></span> | <span data-ttu-id="64a2a-111">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="64a2a-111">2\_x</span></span> | <span data-ttu-id="64a2a-112">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="64a2a-112">2\_sw</span></span> | <span data-ttu-id="64a2a-113">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="64a2a-113">3\_0</span></span> | <span data-ttu-id="64a2a-114">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="64a2a-114">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="64a2a-115">direcc</span><span class="sxs-lookup"><span data-stu-id="64a2a-115">ret</span></span>                    |      | <span data-ttu-id="64a2a-116">x</span><span class="sxs-lookup"><span data-stu-id="64a2a-116">x</span></span>    | <span data-ttu-id="64a2a-117">x</span><span class="sxs-lookup"><span data-stu-id="64a2a-117">x</span></span>    | <span data-ttu-id="64a2a-118">x</span><span class="sxs-lookup"><span data-stu-id="64a2a-118">x</span></span>     | <span data-ttu-id="64a2a-119">x</span><span class="sxs-lookup"><span data-stu-id="64a2a-119">x</span></span>    | <span data-ttu-id="64a2a-120">x</span><span class="sxs-lookup"><span data-stu-id="64a2a-120">x</span></span>     |



 

<span data-ttu-id="64a2a-121">Esta instrucción toma la dirección de una instrucción de la pila de direcciones devuelta y continúa la ejecución de ella.</span><span class="sxs-lookup"><span data-stu-id="64a2a-121">This instruction takes the address of an instruction from the return address stack and continues execution from it.</span></span> <span data-ttu-id="64a2a-122">En el caso de la función Main, esta instrucción detiene la ejecución del sombreador.</span><span class="sxs-lookup"><span data-stu-id="64a2a-122">In the case of the main function, this instruction stops shader execution.</span></span>

<span data-ttu-id="64a2a-123">La instrucción RET consume una ranura de instrucciones del sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="64a2a-123">The ret instruction consumes one vertex shader instruction slot.</span></span>

<span data-ttu-id="64a2a-124">Si un sombreador no contiene subrutinas, el uso de RET al final del programa principal es opcional.</span><span class="sxs-lookup"><span data-stu-id="64a2a-124">If a shader contains no subroutines, using ret at the end of the main program is optional.</span></span>

<span data-ttu-id="64a2a-125">No se permiten varias instrucciones Return en el programa principal o en cualquier subrutina, la primera instrucción return se trata como el final del programa o subrutina principal.</span><span class="sxs-lookup"><span data-stu-id="64a2a-125">Multiple return statements are not permitted in the main program or in any subroutine, the first return statement is treated as the end of the main program or subroutine.</span></span>

## <a name="related-topics"></a><span data-ttu-id="64a2a-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="64a2a-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64a2a-127">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="64a2a-127">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




