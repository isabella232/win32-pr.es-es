---
title: ps
description: Esta instrucción especifica el número de versión del sombreador y funciona en todas las versiones del sombreador.
ms.assetid: 953b1d66-09c1-4ad5-96d4-acb49a1f244c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bdf251d8b5618916365348ab3bf62a89ea552de1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996964"
---
# <a name="ps"></a><span data-ttu-id="79f16-103">ps</span><span class="sxs-lookup"><span data-stu-id="79f16-103">ps</span></span>

<span data-ttu-id="79f16-104">Esta instrucción especifica el número de versión del sombreador y funciona en todas las versiones del sombreador.</span><span class="sxs-lookup"><span data-stu-id="79f16-104">This instruction specifies the shader version number and works on all shader versions.</span></span>

## <a name="syntax"></a><span data-ttu-id="79f16-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="79f16-105">Syntax</span></span>


```
ps_mainVer_subVer
```



## <a name="input-arguments"></a><span data-ttu-id="79f16-106">Argumentos de entrada</span><span class="sxs-lookup"><span data-stu-id="79f16-106">Input Arguments</span></span>

<span data-ttu-id="79f16-107">Los argumentos de entrada contienen un único número de versión principal con un único número de versión.</span><span class="sxs-lookup"><span data-stu-id="79f16-107">Input arguments contain a single main version number with a single sub version number.</span></span> <span data-ttu-id="79f16-108">Las combinaciones permitidas se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="79f16-108">The allowable combinations are listed in the table below.</span></span>



| <span data-ttu-id="79f16-109">Versiones principales</span><span class="sxs-lookup"><span data-stu-id="79f16-109">Main versions</span></span> | <span data-ttu-id="79f16-110">Versiones secundarias</span><span class="sxs-lookup"><span data-stu-id="79f16-110">Sub versions</span></span>                   |
|---------------|--------------------------------|
| <span data-ttu-id="79f16-111">1</span><span class="sxs-lookup"><span data-stu-id="79f16-111">1</span></span>             | <span data-ttu-id="79f16-112">1, 2, 3, 4</span><span class="sxs-lookup"><span data-stu-id="79f16-112">1, 2, 3, 4</span></span>                     |
| <span data-ttu-id="79f16-113">2</span><span class="sxs-lookup"><span data-stu-id="79f16-113">2</span></span>             | <span data-ttu-id="79f16-114">0, x (extendido), SW (software)</span><span class="sxs-lookup"><span data-stu-id="79f16-114">0, x (extended), sw (software)</span></span> |
| <span data-ttu-id="79f16-115">3</span><span class="sxs-lookup"><span data-stu-id="79f16-115">3</span></span>             | <span data-ttu-id="79f16-116">0, SW (software)</span><span class="sxs-lookup"><span data-stu-id="79f16-116">0, sw (software)</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="79f16-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="79f16-117">Remarks</span></span>



| <span data-ttu-id="79f16-118">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="79f16-118">Pixel shader versions</span></span> | <span data-ttu-id="79f16-119">1\_1</span><span class="sxs-lookup"><span data-stu-id="79f16-119">1\_1</span></span> | <span data-ttu-id="79f16-120">1\_2</span><span class="sxs-lookup"><span data-stu-id="79f16-120">1\_2</span></span> | <span data-ttu-id="79f16-121">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="79f16-121">1\_3</span></span> | <span data-ttu-id="79f16-122">1\_4</span><span class="sxs-lookup"><span data-stu-id="79f16-122">1\_4</span></span> | <span data-ttu-id="79f16-123">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="79f16-123">2\_0</span></span> | <span data-ttu-id="79f16-124">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="79f16-124">2\_x</span></span> | <span data-ttu-id="79f16-125">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="79f16-125">2\_sw</span></span> | <span data-ttu-id="79f16-126">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="79f16-126">3\_0</span></span> | <span data-ttu-id="79f16-127">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="79f16-127">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="79f16-128">ps</span><span class="sxs-lookup"><span data-stu-id="79f16-128">ps</span></span>                    | <span data-ttu-id="79f16-129">x</span><span class="sxs-lookup"><span data-stu-id="79f16-129">x</span></span>    | <span data-ttu-id="79f16-130">x</span><span class="sxs-lookup"><span data-stu-id="79f16-130">x</span></span>    | <span data-ttu-id="79f16-131">x</span><span class="sxs-lookup"><span data-stu-id="79f16-131">x</span></span>    | <span data-ttu-id="79f16-132">x</span><span class="sxs-lookup"><span data-stu-id="79f16-132">x</span></span>    | <span data-ttu-id="79f16-133">x</span><span class="sxs-lookup"><span data-stu-id="79f16-133">x</span></span>    | <span data-ttu-id="79f16-134">x</span><span class="sxs-lookup"><span data-stu-id="79f16-134">x</span></span>    | <span data-ttu-id="79f16-135">x</span><span class="sxs-lookup"><span data-stu-id="79f16-135">x</span></span>     | <span data-ttu-id="79f16-136">x</span><span class="sxs-lookup"><span data-stu-id="79f16-136">x</span></span>    | <span data-ttu-id="79f16-137">x</span><span class="sxs-lookup"><span data-stu-id="79f16-137">x</span></span>     |



 

<span data-ttu-id="79f16-138">Esta instrucción debe ser la primera instrucción que no sea de comentario en un sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="79f16-138">This instruction must be the first non-comment instruction in a pixel shader.</span></span>

<span data-ttu-id="79f16-139">Las versiones aceleradas de hardware del software (versiones sin \_ software en el número de versión), pueden procesar vértices con accelearation de hardware o usar el procesamiento de vértices de software.</span><span class="sxs-lookup"><span data-stu-id="79f16-139">Hardware accelerated versions of the software (versions without \_sw in the version number), can process vertices with hardware accelearation or use software vertex processing.</span></span> <span data-ttu-id="79f16-140">Las versiones de software (versiones con \_ SW en el número de versión) solo procesan los vértices con software.</span><span class="sxs-lookup"><span data-stu-id="79f16-140">Software versions (versions with \_sw in the version number) process vertices only with software.</span></span>

## <a name="examples"></a><span data-ttu-id="79f16-141">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="79f16-141">Examples</span></span>

<span data-ttu-id="79f16-142">Este ejemplo parcial declara un sombreador de píxeles de la versión 1 \_ 1.</span><span class="sxs-lookup"><span data-stu-id="79f16-142">This partial example declares a version 1\_1 pixel shader.</span></span>


```
ps_1_1
```



<span data-ttu-id="79f16-143">Este ejemplo parcial declara un sombreador de cuatro píxeles de la versión 1 \_ .</span><span class="sxs-lookup"><span data-stu-id="79f16-143">This partial example declares a version 1\_4 pixel shader.</span></span>


```
ps_1_4
```



## <a name="related-topics"></a><span data-ttu-id="79f16-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="79f16-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79f16-145">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="79f16-145">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




