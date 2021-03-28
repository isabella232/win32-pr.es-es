---
title: BEM-PS
description: Aplicar una transformación de mapa de entorno de rugosidad falsa.
ms.assetid: b41009d4-a2bb-4397-ad23-c95ef2620a66
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7c591555e2cbd2c6eaebf6e392bb94d6ec50e748
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419953"
---
# <a name="bem---ps"></a><span data-ttu-id="789ae-103">BEM-PS</span><span class="sxs-lookup"><span data-stu-id="789ae-103">bem - ps</span></span>

<span data-ttu-id="789ae-104">Aplicar una transformación de mapa de entorno de rugosidad falsa.</span><span class="sxs-lookup"><span data-stu-id="789ae-104">Apply a fake bump environment-map transform.</span></span>

## <a name="syntax"></a><span data-ttu-id="789ae-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="789ae-105">Syntax</span></span>



| <span data-ttu-id="789ae-106">BEM DST. RG, src0, SRC1</span><span class="sxs-lookup"><span data-stu-id="789ae-106">bem dst.rg, src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="789ae-107">, donde</span><span class="sxs-lookup"><span data-stu-id="789ae-107">where</span></span>

-   <span data-ttu-id="789ae-108">DST. RG DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="789ae-108">dst.rg dst is the destination register.</span></span> <span data-ttu-id="789ae-109">Se debe usar la máscara de escritura del componente rojo y verde.</span><span class="sxs-lookup"><span data-stu-id="789ae-109">The red and green component write mask must be used.</span></span>
-   <span data-ttu-id="789ae-110">src0 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="789ae-110">src0 is a source register.</span></span>
-   <span data-ttu-id="789ae-111">SRC1 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="789ae-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="789ae-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="789ae-112">Remarks</span></span>



| <span data-ttu-id="789ae-113">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="789ae-113">Pixel shader versions</span></span> | <span data-ttu-id="789ae-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="789ae-114">1\_1</span></span> | <span data-ttu-id="789ae-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="789ae-115">1\_2</span></span> | <span data-ttu-id="789ae-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="789ae-116">1\_3</span></span> | <span data-ttu-id="789ae-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="789ae-117">1\_4</span></span> | <span data-ttu-id="789ae-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="789ae-118">2\_0</span></span> | <span data-ttu-id="789ae-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="789ae-119">2\_x</span></span> | <span data-ttu-id="789ae-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="789ae-120">2\_sw</span></span> | <span data-ttu-id="789ae-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="789ae-121">3\_0</span></span> | <span data-ttu-id="789ae-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="789ae-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="789ae-123">bem</span><span class="sxs-lookup"><span data-stu-id="789ae-123">bem</span></span>                   |      |      |      | <span data-ttu-id="789ae-124">x</span><span class="sxs-lookup"><span data-stu-id="789ae-124">x</span></span>    |      |      |       |      |       |



 

<span data-ttu-id="789ae-125">Esta instrucción realiza el cálculo siguiente.</span><span class="sxs-lookup"><span data-stu-id="789ae-125">This instruction performs the following calculation.</span></span>


```
(Given n == dest register #)
dest.r = src0.r + D3DTSS_BUMPENVMAT00(stage n) * src1.r 
                + D3DTSS_BUMPENVMAT10(stage n) * src1.g

dest.g = src0.g + D3DTSS_BUMPENVMAT01(stage n) * src1.r
                + D3DTSS_BUMPENVMAT11(stage n) * src1.g
```



<span data-ttu-id="789ae-126">Reglas para usar BEM:</span><span class="sxs-lookup"><span data-stu-id="789ae-126">Rules for using bem:</span></span>

1.  <span data-ttu-id="789ae-127">BEM debe aparecer en la primera fase de un sombreador (es decir, antes de un marcador de fase).</span><span class="sxs-lookup"><span data-stu-id="789ae-127">bem must appear in the first phase of a shader (that is, before a phase marker).</span></span>
2.  <span data-ttu-id="789ae-128">BEM consume dos ranuras de Instrucciones aritméticas.</span><span class="sxs-lookup"><span data-stu-id="789ae-128">bem consumes two arithmetic instruction slots.</span></span>
3.  <span data-ttu-id="789ae-129">Solo se permite un uso de esta instrucción por sombreador.</span><span class="sxs-lookup"><span data-stu-id="789ae-129">Only one use of this instruction is allowed per shader.</span></span>
4.  <span data-ttu-id="789ae-130">El writemask de destino debe ser. RG/.XY.</span><span class="sxs-lookup"><span data-stu-id="789ae-130">Destination writemask must be .rg /.xy.</span></span>
5.  <span data-ttu-id="789ae-131">Esta instrucción no se puede comemisión de forma conjunta.</span><span class="sxs-lookup"><span data-stu-id="789ae-131">This instruction cannot be co-issued.</span></span>
6.  <span data-ttu-id="789ae-132">Aparte de la restricción de que la máscara de escritura de destino sea. RG, los modificadores de los modificadores de instrucción src0, SRC1 y Instruction de origen no están restringidos.</span><span class="sxs-lookup"><span data-stu-id="789ae-132">Aside from the restriction that destination write mask be .rg, modifiers on source src0, src1, and instruction modifiers are unconstrained.</span></span>

## <a name="instruction-information"></a><span data-ttu-id="789ae-133">Información de instrucciones</span><span class="sxs-lookup"><span data-stu-id="789ae-133">Instruction Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="789ae-134">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="789ae-134">Minimum operating system</span></span> | <span data-ttu-id="789ae-135">Windows 98</span><span class="sxs-lookup"><span data-stu-id="789ae-135">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="789ae-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="789ae-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="789ae-137">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="789ae-137">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




