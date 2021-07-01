---
title: bem - ps
description: Aplicar una transformación de mapa de entorno de protuberancia falsa.
ms.assetid: b41009d4-a2bb-4397-ad23-c95ef2620a66
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1adae07e3e2ebbca085981ca03a3b6449e2ffd9d
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129934"
---
# <a name="bem---ps"></a><span data-ttu-id="c79e6-103">bem - ps</span><span class="sxs-lookup"><span data-stu-id="c79e6-103">bem - ps</span></span>

<span data-ttu-id="c79e6-104">Aplicar una transformación de mapa de entorno de protuberancia falsa.</span><span class="sxs-lookup"><span data-stu-id="c79e6-104">Apply a fake bump environment-map transform.</span></span>

## <a name="syntax"></a><span data-ttu-id="c79e6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c79e6-105">Syntax</span></span>



| <span data-ttu-id="c79e6-106">bem dst.rg, src0, src1</span><span class="sxs-lookup"><span data-stu-id="c79e6-106">bem dst.rg, src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="c79e6-107">where</span><span class="sxs-lookup"><span data-stu-id="c79e6-107">where</span></span>

-   <span data-ttu-id="c79e6-108">dst.rg dst es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="c79e6-108">dst.rg dst is the destination register.</span></span> <span data-ttu-id="c79e6-109">Se debe usar la máscara de escritura del componente rojo y verde.</span><span class="sxs-lookup"><span data-stu-id="c79e6-109">The red and green component write mask must be used.</span></span>
-   <span data-ttu-id="c79e6-110">src0 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="c79e6-110">src0 is a source register.</span></span>
-   <span data-ttu-id="c79e6-111">src1 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="c79e6-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="c79e6-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c79e6-112">Remarks</span></span>



| <span data-ttu-id="c79e6-113">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="c79e6-113">Pixel shader versions</span></span> | <span data-ttu-id="c79e6-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="c79e6-114">1\_1</span></span> | <span data-ttu-id="c79e6-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="c79e6-115">1\_2</span></span> | <span data-ttu-id="c79e6-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="c79e6-116">1\_3</span></span> | <span data-ttu-id="c79e6-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="c79e6-117">1\_4</span></span> | <span data-ttu-id="c79e6-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c79e6-118">2\_0</span></span> | <span data-ttu-id="c79e6-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c79e6-119">2\_x</span></span> | <span data-ttu-id="c79e6-120">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="c79e6-120">2\_sw</span></span> | <span data-ttu-id="c79e6-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c79e6-121">3\_0</span></span> | <span data-ttu-id="c79e6-122">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="c79e6-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="c79e6-123">Bem</span><span class="sxs-lookup"><span data-stu-id="c79e6-123">bem</span></span>                   |      |      |      | <span data-ttu-id="c79e6-124">x</span><span class="sxs-lookup"><span data-stu-id="c79e6-124">x</span></span>    |      |      |       |      |       |



 

<span data-ttu-id="c79e6-125">Esta instrucción realiza el cálculo siguiente.</span><span class="sxs-lookup"><span data-stu-id="c79e6-125">This instruction performs the following calculation.</span></span>


```
(Given n == dest register #)
dest.r = src0.r + D3DTSS_BUMPENVMAT00(stage n) * src1.r 
                + D3DTSS_BUMPENVMAT10(stage n) * src1.g

dest.g = src0.g + D3DTSS_BUMPENVMAT01(stage n) * src1.r
                + D3DTSS_BUMPENVMAT11(stage n) * src1.g
```



<span data-ttu-id="c79e6-126">Reglas para usar bem:</span><span class="sxs-lookup"><span data-stu-id="c79e6-126">Rules for using bem:</span></span>

1.  <span data-ttu-id="c79e6-127">bem debe aparecer en la primera fase de un sombreador (es decir, antes de un marcador de fase).</span><span class="sxs-lookup"><span data-stu-id="c79e6-127">bem must appear in the first phase of a shader (that is, before a phase marker).</span></span>
2.  <span data-ttu-id="c79e6-128">bem consume dos ranuras de instrucciones aritméticas.</span><span class="sxs-lookup"><span data-stu-id="c79e6-128">bem consumes two arithmetic instruction slots.</span></span>
3.  <span data-ttu-id="c79e6-129">Solo se permite un uso de esta instrucción por sombreador.</span><span class="sxs-lookup"><span data-stu-id="c79e6-129">Only one use of this instruction is allowed per shader.</span></span>
4.  <span data-ttu-id="c79e6-130">La máscara de escritura de destino debe ser .rg /.xy.</span><span class="sxs-lookup"><span data-stu-id="c79e6-130">Destination writemask must be .rg /.xy.</span></span>
5.  <span data-ttu-id="c79e6-131">Esta instrucción no se puede emitir de forma coe emitida.</span><span class="sxs-lookup"><span data-stu-id="c79e6-131">This instruction cannot be co-issued.</span></span>
6.  <span data-ttu-id="c79e6-132">Aparte de la restricción de que la máscara de escritura de destino sea .rg, los modificadores de origen src0, src1 y modificadores de instrucción no están entrenados.</span><span class="sxs-lookup"><span data-stu-id="c79e6-132">Aside from the restriction that destination write mask be .rg, modifiers on source src0, src1, and instruction modifiers are unconstrained.</span></span>

## <a name="instruction-information"></a><span data-ttu-id="c79e6-133">Información de instrucciones</span><span class="sxs-lookup"><span data-stu-id="c79e6-133">Instruction Information</span></span>



| <span data-ttu-id="c79e6-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="c79e6-134">Requirement</span></span>                         | <span data-ttu-id="c79e6-135">Valor</span><span class="sxs-lookup"><span data-stu-id="c79e6-135">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="c79e6-136">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="c79e6-136">Minimum operating system</span></span> | <span data-ttu-id="c79e6-137">Windows 98</span><span class="sxs-lookup"><span data-stu-id="c79e6-137">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="c79e6-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c79e6-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c79e6-139">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="c79e6-139">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




