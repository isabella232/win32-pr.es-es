---
title: vs
description: Esta instrucción especifica el número de versión del sombreador. Esta instrucción funciona en todas las versiones de sombreador.
ms.assetid: edcbaff3-eb32-49e6-80de-621b67d4df75
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: baf773d7607aa575bd575339bde072b3dc04b224
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419981"
---
# <a name="vs"></a><span data-ttu-id="82edc-104">vs</span><span class="sxs-lookup"><span data-stu-id="82edc-104">vs</span></span>

<span data-ttu-id="82edc-105">Esta instrucción especifica el número de versión del sombreador.</span><span class="sxs-lookup"><span data-stu-id="82edc-105">This instruction specifies the shader version number.</span></span> <span data-ttu-id="82edc-106">Esta instrucción funciona en todas las versiones de sombreador.</span><span class="sxs-lookup"><span data-stu-id="82edc-106">This instruction works on all shader versions.</span></span>

## <a name="syntax"></a><span data-ttu-id="82edc-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="82edc-107">Syntax</span></span>


```
vs_mainVer_subVer
```



## <a name="input-arguments"></a><span data-ttu-id="82edc-108">Argumentos de entrada</span><span class="sxs-lookup"><span data-stu-id="82edc-108">Input Arguments</span></span>

<span data-ttu-id="82edc-109">Los argumentos de entrada contienen un único número de versión principal con un único número de versión.</span><span class="sxs-lookup"><span data-stu-id="82edc-109">Input arguments contain a single main version number with a single sub version number.</span></span> <span data-ttu-id="82edc-110">Las combinaciones permitidas se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="82edc-110">The allowable combinations are listed in the table below.</span></span>



| <span data-ttu-id="82edc-111">Versiones principales</span><span class="sxs-lookup"><span data-stu-id="82edc-111">Main versions</span></span> | <span data-ttu-id="82edc-112">Versiones secundarias</span><span class="sxs-lookup"><span data-stu-id="82edc-112">Sub versions</span></span>                   |
|---------------|--------------------------------|
| <span data-ttu-id="82edc-113">1</span><span class="sxs-lookup"><span data-stu-id="82edc-113">1</span></span>             | <span data-ttu-id="82edc-114">1</span><span class="sxs-lookup"><span data-stu-id="82edc-114">1</span></span>                              |
| <span data-ttu-id="82edc-115">2</span><span class="sxs-lookup"><span data-stu-id="82edc-115">2</span></span>             | <span data-ttu-id="82edc-116">0, SW (software), x (extendido)</span><span class="sxs-lookup"><span data-stu-id="82edc-116">0, sw (software), x (extended)</span></span> |
| <span data-ttu-id="82edc-117">3</span><span class="sxs-lookup"><span data-stu-id="82edc-117">3</span></span>             | <span data-ttu-id="82edc-118">0, SW (software)</span><span class="sxs-lookup"><span data-stu-id="82edc-118">0, sw (software)</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="82edc-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="82edc-119">Remarks</span></span>



| <span data-ttu-id="82edc-120">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="82edc-120">Vertex shader versions</span></span> | <span data-ttu-id="82edc-121">1\_1</span><span class="sxs-lookup"><span data-stu-id="82edc-121">1\_1</span></span> | <span data-ttu-id="82edc-122">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="82edc-122">2\_0</span></span> | <span data-ttu-id="82edc-123">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="82edc-123">2\_x</span></span> | <span data-ttu-id="82edc-124">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="82edc-124">2\_sw</span></span> | <span data-ttu-id="82edc-125">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="82edc-125">3\_0</span></span> | <span data-ttu-id="82edc-126">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="82edc-126">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="82edc-127">vs</span><span class="sxs-lookup"><span data-stu-id="82edc-127">vs</span></span>                     | <span data-ttu-id="82edc-128">x</span><span class="sxs-lookup"><span data-stu-id="82edc-128">x</span></span>    | <span data-ttu-id="82edc-129">x</span><span class="sxs-lookup"><span data-stu-id="82edc-129">x</span></span>    | <span data-ttu-id="82edc-130">x</span><span class="sxs-lookup"><span data-stu-id="82edc-130">x</span></span>    | <span data-ttu-id="82edc-131">x</span><span class="sxs-lookup"><span data-stu-id="82edc-131">x</span></span>     | <span data-ttu-id="82edc-132">x</span><span class="sxs-lookup"><span data-stu-id="82edc-132">x</span></span>    | <span data-ttu-id="82edc-133">x</span><span class="sxs-lookup"><span data-stu-id="82edc-133">x</span></span>     |



 

<span data-ttu-id="82edc-134">Esta instrucción debe ser la primera instrucción que no sea de comentario en un sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="82edc-134">This instruction must be the first non-comment instruction in a vertex shader.</span></span>

<span data-ttu-id="82edc-135">Esta instrucción es compatible con todas las versiones del sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="82edc-135">This instruction is supported in all vertex shader versions.</span></span>

<span data-ttu-id="82edc-136">Las versiones aceleradas de hardware del software (versiones sin \_ software en el número de versión), pueden procesar vértices con accelearation de hardware o usar el procesamiento de vértices de software.</span><span class="sxs-lookup"><span data-stu-id="82edc-136">Hardware accelerated versions of the software (versions without \_sw in the version number), can process vertices with hardware accelearation or use software vertex processing.</span></span> <span data-ttu-id="82edc-137">Las versiones de software (versiones con \_ SW en el número de versión) solo procesan los vértices con software.</span><span class="sxs-lookup"><span data-stu-id="82edc-137">Software versions (versions with \_sw in the version number) process vertices only with software.</span></span>

## <a name="examples"></a><span data-ttu-id="82edc-138">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="82edc-138">Examples</span></span>

<span data-ttu-id="82edc-139">Este ejemplo parcial declara un sombreador de vértices de la versión 1 \_ 1.</span><span class="sxs-lookup"><span data-stu-id="82edc-139">This partial example declares a version 1\_1 vertex shader.</span></span>


```
vs_1_1
```



<span data-ttu-id="82edc-140">Este ejemplo parcial declara un sombreador de vértices de software de la versión 2.</span><span class="sxs-lookup"><span data-stu-id="82edc-140">This partial example declares a version 2 software vertex shader.</span></span>


```
vs_2_sw
```



## <a name="related-topics"></a><span data-ttu-id="82edc-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="82edc-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82edc-142">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="82edc-142">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




