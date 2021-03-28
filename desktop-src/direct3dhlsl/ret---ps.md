---
title: RET-PS
description: Toma la dirección de una instrucción de la pila de direcciones devuelta y continúa la ejecución de ella. En el caso de la función Main, esta instrucción detiene la ejecución del sombreador.
ms.assetid: f853a137-8944-4f6e-89c0-7fd37d1a468e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b0535a4fcd66a1872b5eaa9ec97c292de710b48c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104983834"
---
# <a name="ret---ps"></a><span data-ttu-id="2d893-104">RET-PS</span><span class="sxs-lookup"><span data-stu-id="2d893-104">ret - ps</span></span>

<span data-ttu-id="2d893-105">Toma la dirección de una instrucción de la pila de direcciones devuelta y continúa la ejecución de ella.</span><span class="sxs-lookup"><span data-stu-id="2d893-105">Takes the address of an instruction from the return address stack and continues execution from it.</span></span> <span data-ttu-id="2d893-106">En el caso de la función Main, esta instrucción detiene la ejecución del sombreador.</span><span class="sxs-lookup"><span data-stu-id="2d893-106">In the case of the main function, this instruction stops shader execution.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d893-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2d893-107">Syntax</span></span>



| <span data-ttu-id="2d893-108">direcc</span><span class="sxs-lookup"><span data-stu-id="2d893-108">ret</span></span> |
|-----|



 

## <a name="remarks"></a><span data-ttu-id="2d893-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2d893-109">Remarks</span></span>



| <span data-ttu-id="2d893-110">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="2d893-110">Pixel shader versions</span></span> | <span data-ttu-id="2d893-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="2d893-111">1\_1</span></span> | <span data-ttu-id="2d893-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="2d893-112">1\_2</span></span> | <span data-ttu-id="2d893-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="2d893-113">1\_3</span></span> | <span data-ttu-id="2d893-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="2d893-114">1\_4</span></span> | <span data-ttu-id="2d893-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2d893-115">2\_0</span></span> | <span data-ttu-id="2d893-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="2d893-116">2\_x</span></span> | <span data-ttu-id="2d893-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="2d893-117">2\_sw</span></span> | <span data-ttu-id="2d893-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2d893-118">3\_0</span></span> | <span data-ttu-id="2d893-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="2d893-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="2d893-120">direcc</span><span class="sxs-lookup"><span data-stu-id="2d893-120">ret</span></span>                   |      |      |      |      |      | <span data-ttu-id="2d893-121">x</span><span class="sxs-lookup"><span data-stu-id="2d893-121">x</span></span>    | <span data-ttu-id="2d893-122">x</span><span class="sxs-lookup"><span data-stu-id="2d893-122">x</span></span>     | <span data-ttu-id="2d893-123">x</span><span class="sxs-lookup"><span data-stu-id="2d893-123">x</span></span>    | <span data-ttu-id="2d893-124">x</span><span class="sxs-lookup"><span data-stu-id="2d893-124">x</span></span>     |



 

<span data-ttu-id="2d893-125">Esta instrucción toma la dirección de una instrucción de la pila de direcciones devuelta y continúa la ejecución de ella.</span><span class="sxs-lookup"><span data-stu-id="2d893-125">This instruction takes the address of an instruction from the return address stack and continues execution from it.</span></span> <span data-ttu-id="2d893-126">En el caso de la función Main, esta instrucción detiene la ejecución del sombreador.</span><span class="sxs-lookup"><span data-stu-id="2d893-126">In the case of the main function, this instruction stops shader execution.</span></span>

<span data-ttu-id="2d893-127">La instrucción RET consume una ranura de instrucciones del sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="2d893-127">The ret instruction consumes one vertex shader instruction slot.</span></span>

<span data-ttu-id="2d893-128">Si un sombreador no contiene subrutinas, el uso de RET al final del programa principal es opcional.</span><span class="sxs-lookup"><span data-stu-id="2d893-128">If a shader contains no subroutines, using ret at the end of the main program is optional.</span></span>

<span data-ttu-id="2d893-129">No se permiten varias instrucciones Return en el programa principal o en cualquier subrutina, la primera instrucción return se trata como el final del programa o subrutina principal.</span><span class="sxs-lookup"><span data-stu-id="2d893-129">Multiple return statements are not permitted in the main program or in any subroutine, the first return statement is treated as the end of the main program or subroutine.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2d893-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2d893-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d893-131">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="2d893-131">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




