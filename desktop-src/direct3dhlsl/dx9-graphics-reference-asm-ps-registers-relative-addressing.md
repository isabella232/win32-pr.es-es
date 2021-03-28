---
title: Direccionamiento relativo (referencia de PS de HLSL)
description: La sintaxis \ \ solo se puede usar en tipos de registro que se pueden tratar relativamente en determinados modelos de sombreador.
ms.assetid: 37e2bab9-f6fe-438a-8a2d-c963634ef8c3
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 38c7be68245cfedbb27898e0fbb689e9e43755ca
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2019
ms.locfileid: "103785063"
---
# <a name="relative-addressing-hlsl-ps-reference"></a><span data-ttu-id="b9589-103">Direccionamiento relativo (referencia de PS de HLSL)</span><span class="sxs-lookup"><span data-stu-id="b9589-103">Relative addressing (HLSL PS reference)</span></span>

<span data-ttu-id="b9589-104">La \[ \] Sintaxis solo se puede usar en tipos de registro que se pueden tratar relativamente en determinados modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="b9589-104">The \[ \] syntax can be used only in register types that can be relatively addressed in certain shader models.</span></span> <span data-ttu-id="b9589-105">Los formatos de sintaxis admitidos \[ \] se enumeran de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="b9589-105">The supported forms of \[ \] syntax are listed as follows:</span></span>

<span data-ttu-id="b9589-106">Donde:</span><span class="sxs-lookup"><span data-stu-id="b9589-106">Where:</span></span>

-   <span data-ttu-id="b9589-107">"R" denota cualquier tipo de registro que pueda ser relativamente direccionado.</span><span class="sxs-lookup"><span data-stu-id="b9589-107">"R" denotes any register type that can be relatively addressed.</span></span>
-   <span data-ttu-id="b9589-108">"A" denota cualquier registro que se puede utilizar como índice para abordar otros registros de forma relativamente.</span><span class="sxs-lookup"><span data-stu-id="b9589-108">"A" denotes any register that can be used as an index to relatively address other registers.</span></span>
-   <span data-ttu-id="b9589-109">N0-ni, M0-MJ y k son enteros >= 0.</span><span class="sxs-lookup"><span data-stu-id="b9589-109">n0 - ni, m0 - mj, and k are integers >= 0.</span></span>



| <span data-ttu-id="b9589-110">\[\]Sintaxis de</span><span class="sxs-lookup"><span data-stu-id="b9589-110">\[ \] syntax</span></span>                              | <span data-ttu-id="b9589-111">Índice efectivo</span><span class="sxs-lookup"><span data-stu-id="b9589-111">Effective index</span></span>                       | <span data-ttu-id="b9589-112">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b9589-112">Examples</span></span>                         |
|-------------------------------------------|---------------------------------------|----------------------------------|
| <span data-ttu-id="b9589-113">R \[ A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="b9589-113">R\[ A + m0 + ... + mj \]</span></span>                  | <span data-ttu-id="b9589-114">A + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="b9589-114">A + m0 + ... + mj</span></span>                     | <span data-ttu-id="b9589-115">c \[ a0. x + 3 + 7 \]</span><span class="sxs-lookup"><span data-stu-id="b9589-115">c\[ a0.x + 3 + 7 \]</span></span>              |
| <span data-ttu-id="b9589-116">R \[ k \] (= RK)</span><span class="sxs-lookup"><span data-stu-id="b9589-116">R\[ k \] ( = Rk )</span></span>                         | <span data-ttu-id="b9589-117">k</span><span class="sxs-lookup"><span data-stu-id="b9589-117">k</span></span>                                     | <span data-ttu-id="b9589-118">c \[ 10 \] (= C10)</span><span class="sxs-lookup"><span data-stu-id="b9589-118">c\[ 10 \] ( = c10 )</span></span>              |
| <span data-ttu-id="b9589-119">R \[ A \]</span><span class="sxs-lookup"><span data-stu-id="b9589-119">R\[ A \]</span></span>                                  | <span data-ttu-id="b9589-120">Un</span><span class="sxs-lookup"><span data-stu-id="b9589-120">A</span></span>                                     | <span data-ttu-id="b9589-121">c \[ a0. y \]</span><span class="sxs-lookup"><span data-stu-id="b9589-121">c\[ a0.y \]</span></span>                      |
| <span data-ttu-id="b9589-122">RK \[ N0 +... + ni + A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="b9589-122">Rk\[ n0 + ... + ni + A + m0 + ... + mj \]</span></span> | <span data-ttu-id="b9589-123">A + k + N0 +... + ni + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="b9589-123">A + k + n0 + ... + ni + m0 + ... + mj</span></span> | <span data-ttu-id="b9589-124">C8 \[ 3 + 2 + a0. w + 5 + 6 + 1 \]</span><span class="sxs-lookup"><span data-stu-id="b9589-124">c8\[ 3 + 2 + a0.w + 5 + 6 + 1 \]</span></span> |
| <span data-ttu-id="b9589-125">R \[ N0 +... + ni + A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="b9589-125">R\[ n0 + ... + ni + A + m0 + ... + mj \]</span></span>  | <span data-ttu-id="b9589-126">A + N0 +... + ni + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="b9589-126">A + n0 + ... + ni + m0 + ... + mj</span></span>     | <span data-ttu-id="b9589-127">c \[ 2 + 1 + al + 3 + 4 + 5 \]</span><span class="sxs-lookup"><span data-stu-id="b9589-127">c\[ 2 + 1 + aL + 3 + 4 + 5 \]</span></span>    |
| <span data-ttu-id="b9589-128">RK \[ A \]</span><span class="sxs-lookup"><span data-stu-id="b9589-128">Rk\[ A \]</span></span>                                 | <span data-ttu-id="b9589-129">A + k</span><span class="sxs-lookup"><span data-stu-id="b9589-129">A + k</span></span>                                 | <span data-ttu-id="b9589-130">C12 \[ al \] , C0 \[ a0. z \]</span><span class="sxs-lookup"><span data-stu-id="b9589-130">c12\[ aL \], c0\[ a0.z \]</span></span>        |
| <span data-ttu-id="b9589-131">RK \[ A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="b9589-131">Rk\[ A + m0 + ... + mj \]</span></span>                 | <span data-ttu-id="b9589-132">A + k + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="b9589-132">A + k + m0 + ... + mj</span></span>                 | <span data-ttu-id="b9589-133">v1 \[ al + 4 + 8 \]</span><span class="sxs-lookup"><span data-stu-id="b9589-133">v1\[ aL + 4 + 8 \]</span></span>               |
| <span data-ttu-id="b9589-134">R \[ N0 +... + ni + A \]</span><span class="sxs-lookup"><span data-stu-id="b9589-134">R\[ n0 + ... + ni + A \]</span></span>                  | <span data-ttu-id="b9589-135">A + N0 +... + ni</span><span class="sxs-lookup"><span data-stu-id="b9589-135">A + n0 + ... + ni</span></span>                     | <span data-ttu-id="b9589-136">o \[ 3 + 1 + al \]</span><span class="sxs-lookup"><span data-stu-id="b9589-136">o\[ 3 + 1 + aL \]</span></span>                |
| <span data-ttu-id="b9589-137">RK \[ N0 +... + ni + A \]</span><span class="sxs-lookup"><span data-stu-id="b9589-137">Rk\[ n0 + ... + ni + A \]</span></span>                 | <span data-ttu-id="b9589-138">A + k + N0 +... + ni</span><span class="sxs-lookup"><span data-stu-id="b9589-138">A + k + n0 + ... + ni</span></span>                 | <span data-ttu-id="b9589-139">O1 \[ 2 + 1 + 3 + al \]</span><span class="sxs-lookup"><span data-stu-id="b9589-139">o1\[ 2 + 1 + 3 + aL \]</span></span>           |



 

<span data-ttu-id="b9589-140">Los registros están disponibles en las siguientes versiones:</span><span class="sxs-lookup"><span data-stu-id="b9589-140">The registers are available in the following versions:</span></span>



| <span data-ttu-id="b9589-141">Tipo de registro</span><span class="sxs-lookup"><span data-stu-id="b9589-141">Register type</span></span>                                                                                   | <span data-ttu-id="b9589-142">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="b9589-142">Pixel Shader Versions</span></span> |
|-------------------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="b9589-143">[contador de bucle](dx9-graphics-reference-asm-ps-registers-loop-counter.md): al en registros de entrada</span><span class="sxs-lookup"><span data-stu-id="b9589-143">[loop counter](dx9-graphics-reference-asm-ps-registers-loop-counter.md): aL on input registers</span></span> | <span data-ttu-id="b9589-144">PS \_ 3 \_ 0 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="b9589-144">ps\_3\_0 and higher</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="b9589-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b9589-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9589-146">Registra</span><span class="sxs-lookup"><span data-stu-id="b9589-146">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




