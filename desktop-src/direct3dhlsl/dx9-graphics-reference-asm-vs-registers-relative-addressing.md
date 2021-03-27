---
title: Direccionamiento relativo (HLSL VS Reference)
description: La sintaxis \ \ solo se puede usar en tipos de registro que se pueden tratar relativamente en determinados modelos de sombreador.
ms.assetid: 9f9d2499-73a5-4c9d-9dce-94c914933334
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c11d6f6c4b448e1dee5f4237696c110519bc0dd0
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2019
ms.locfileid: "104358522"
---
# <a name="relative-addressing-hlsl-vs-reference"></a><span data-ttu-id="af0c4-103">Direccionamiento relativo (HLSL VS Reference)</span><span class="sxs-lookup"><span data-stu-id="af0c4-103">Relative Addressing (HLSL VS reference)</span></span>

<span data-ttu-id="af0c4-104">La \[ \] Sintaxis solo se puede usar en tipos de registro que se pueden tratar relativamente en determinados modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="af0c4-104">The \[ \] syntax can be used only in register types that can be relatively addressed in certain shader models.</span></span> <span data-ttu-id="af0c4-105">Los formatos de sintaxis admitidos \[ \] se enumeran de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="af0c4-105">The supported forms of \[ \] syntax are listed as follows:</span></span>

<span data-ttu-id="af0c4-106">Donde:</span><span class="sxs-lookup"><span data-stu-id="af0c4-106">Where:</span></span>

-   <span data-ttu-id="af0c4-107">"R" denota cualquier tipo de registro que pueda ser relativamente direccionado.</span><span class="sxs-lookup"><span data-stu-id="af0c4-107">"R" denotes any register type that can be relatively addressed.</span></span>
-   <span data-ttu-id="af0c4-108">"A" denota cualquier registro que se puede utilizar como índice para abordar otros registros de forma relativamente.</span><span class="sxs-lookup"><span data-stu-id="af0c4-108">"A" denotes any register that can be used as an index to relatively address other registers.</span></span>
-   <span data-ttu-id="af0c4-109">N0-ni, M0-MJ y k son enteros >= 0.</span><span class="sxs-lookup"><span data-stu-id="af0c4-109">n0 - ni, m0 - mj, and k are integers >= 0.</span></span>



| <span data-ttu-id="af0c4-110">\[\]Sintaxis de</span><span class="sxs-lookup"><span data-stu-id="af0c4-110">\[ \] syntax</span></span>                              | <span data-ttu-id="af0c4-111">Índice efectivo</span><span class="sxs-lookup"><span data-stu-id="af0c4-111">Effective index</span></span>                       | <span data-ttu-id="af0c4-112">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="af0c4-112">Examples</span></span>                         |
|-------------------------------------------|---------------------------------------|----------------------------------|
| <span data-ttu-id="af0c4-113">R \[ A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="af0c4-113">R\[ A + m0 + ... + mj \]</span></span>                  | <span data-ttu-id="af0c4-114">A + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="af0c4-114">A + m0 + ... + mj</span></span>                     | <span data-ttu-id="af0c4-115">c \[ a0. x + 3 + 7 \]</span><span class="sxs-lookup"><span data-stu-id="af0c4-115">c\[ a0.x + 3 + 7 \]</span></span>              |
| <span data-ttu-id="af0c4-116">R \[ k \] (= RK)</span><span class="sxs-lookup"><span data-stu-id="af0c4-116">R\[ k \] ( = Rk )</span></span>                         | <span data-ttu-id="af0c4-117">k</span><span class="sxs-lookup"><span data-stu-id="af0c4-117">k</span></span>                                     | <span data-ttu-id="af0c4-118">c \[ 10 \] (= C10)</span><span class="sxs-lookup"><span data-stu-id="af0c4-118">c\[ 10 \] ( = c10 )</span></span>              |
| <span data-ttu-id="af0c4-119">R \[ A \]</span><span class="sxs-lookup"><span data-stu-id="af0c4-119">R\[ A \]</span></span>                                  | <span data-ttu-id="af0c4-120">Un</span><span class="sxs-lookup"><span data-stu-id="af0c4-120">A</span></span>                                     | <span data-ttu-id="af0c4-121">c \[ a0. y \]</span><span class="sxs-lookup"><span data-stu-id="af0c4-121">c\[ a0.y \]</span></span>                      |
| <span data-ttu-id="af0c4-122">RK \[ N0 +... + ni + A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="af0c4-122">Rk\[ n0 + ... + ni + A + m0 + ... + mj \]</span></span> | <span data-ttu-id="af0c4-123">A + k + N0 +... + ni + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="af0c4-123">A + k + n0 + ... + ni + m0 + ... + mj</span></span> | <span data-ttu-id="af0c4-124">C8 \[ 3 + 2 + a0. w + 5 + 6 + 1 \]</span><span class="sxs-lookup"><span data-stu-id="af0c4-124">c8\[ 3 + 2 + a0.w + 5 + 6 + 1 \]</span></span> |
| <span data-ttu-id="af0c4-125">R \[ N0 +... + ni + A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="af0c4-125">R\[ n0 + ... + ni + A + m0 + ... + mj \]</span></span>  | <span data-ttu-id="af0c4-126">A + N0 +... + ni + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="af0c4-126">A + n0 + ... + ni + m0 + ... + mj</span></span>     | <span data-ttu-id="af0c4-127">c \[ 2 + 1 + al + 3 + 4 + 5 \]</span><span class="sxs-lookup"><span data-stu-id="af0c4-127">c\[ 2 + 1 + aL + 3 + 4 + 5 \]</span></span>    |
| <span data-ttu-id="af0c4-128">RK \[ A \]</span><span class="sxs-lookup"><span data-stu-id="af0c4-128">Rk\[ A \]</span></span>                                 | <span data-ttu-id="af0c4-129">A + k</span><span class="sxs-lookup"><span data-stu-id="af0c4-129">A + k</span></span>                                 | <span data-ttu-id="af0c4-130">C12 \[ al \] , C0 \[ a0. z \]</span><span class="sxs-lookup"><span data-stu-id="af0c4-130">c12\[ aL \], c0\[ a0.z \]</span></span>        |
| <span data-ttu-id="af0c4-131">RK \[ A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="af0c4-131">Rk\[ A + m0 + ... + mj \]</span></span>                 | <span data-ttu-id="af0c4-132">A + k + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="af0c4-132">A + k + m0 + ... + mj</span></span>                 | <span data-ttu-id="af0c4-133">v1 \[ al + 4 + 8 \]</span><span class="sxs-lookup"><span data-stu-id="af0c4-133">v1\[ aL + 4 + 8 \]</span></span>               |
| <span data-ttu-id="af0c4-134">R \[ N0 +... + ni + A \]</span><span class="sxs-lookup"><span data-stu-id="af0c4-134">R\[ n0 + ... + ni + A \]</span></span>                  | <span data-ttu-id="af0c4-135">A + N0 +... + ni</span><span class="sxs-lookup"><span data-stu-id="af0c4-135">A + n0 + ... + ni</span></span>                     | <span data-ttu-id="af0c4-136">o \[ 3 + 1 + al \]</span><span class="sxs-lookup"><span data-stu-id="af0c4-136">o\[ 3 + 1 + aL \]</span></span>                |
| <span data-ttu-id="af0c4-137">RK \[ N0 +... + ni + A \]</span><span class="sxs-lookup"><span data-stu-id="af0c4-137">Rk\[ n0 + ... + ni + A \]</span></span>                 | <span data-ttu-id="af0c4-138">A + k + N0 +... + ni</span><span class="sxs-lookup"><span data-stu-id="af0c4-138">A + k + n0 + ... + ni</span></span>                 | <span data-ttu-id="af0c4-139">O1 \[ 2 + 1 + 3 + al \]</span><span class="sxs-lookup"><span data-stu-id="af0c4-139">o1\[ 2 + 1 + 3 + aL \]</span></span>           |



 

<span data-ttu-id="af0c4-140">Los registros están disponibles en las siguientes versiones:</span><span class="sxs-lookup"><span data-stu-id="af0c4-140">The registers are available in the following versions:</span></span>



| <span data-ttu-id="af0c4-141">Tipo de registro</span><span class="sxs-lookup"><span data-stu-id="af0c4-141">Register type</span></span> | <span data-ttu-id="af0c4-142">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="af0c4-142">Vertex Shader Versions</span></span> |
|---------------|------------------------|
| <span data-ttu-id="af0c4-143">a0</span><span class="sxs-lookup"><span data-stu-id="af0c4-143">a0</span></span>            | <span data-ttu-id="af0c4-144">All</span><span class="sxs-lookup"><span data-stu-id="af0c4-144">All</span></span>                    |
| <span data-ttu-id="af0c4-145">Alabama</span><span class="sxs-lookup"><span data-stu-id="af0c4-145">aL</span></span>            | <span data-ttu-id="af0c4-146">vs \_ 2 \_ 0 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="af0c4-146">vs\_2\_0 and higher</span></span>    |
| <span data-ttu-id="af0c4-147">cn</span><span class="sxs-lookup"><span data-stu-id="af0c4-147">cn</span></span>            | <span data-ttu-id="af0c4-148">vs \_ 1 \_ 1 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="af0c4-148">vs\_1\_1 and higher</span></span>    |
| <span data-ttu-id="af0c4-149">on</span><span class="sxs-lookup"><span data-stu-id="af0c4-149">on</span></span>            | <span data-ttu-id="af0c4-150">vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="af0c4-150">vs\_3\_0</span></span>               |



 

## <a name="related-topics"></a><span data-ttu-id="af0c4-151">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="af0c4-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af0c4-152">Registros del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="af0c4-152">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




