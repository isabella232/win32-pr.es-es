---
title: Direccionamiento relativo (referencia de HLSL VS)
description: En el caso de los sombreadores de vértices, la sintaxis \ \ solo se puede usar en tipos de registro que se puedan abordar relativamente en determinados modelos de sombreador.
ms.assetid: 9f9d2499-73a5-4c9d-9dce-94c914933334
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2bbba694878ba84ac3c2fa9c4e8058bb0d91830e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406698"
---
# <a name="relative-addressing-hlsl-vs-reference"></a><span data-ttu-id="237db-103">Direccionamiento relativo (referencia de HLSL VS)</span><span class="sxs-lookup"><span data-stu-id="237db-103">Relative Addressing (HLSL VS reference)</span></span>

<span data-ttu-id="237db-104">La \[ \] sintaxis solo se puede usar en tipos de registro que se puedan abordar relativamente en determinados modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="237db-104">The \[ \] syntax can be used only in register types that can be relatively addressed in certain shader models.</span></span> <span data-ttu-id="237db-105">Las formas de \[ \] sintaxis admitidas se enumeran de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="237db-105">The supported forms of \[ \] syntax are listed as follows:</span></span>

<span data-ttu-id="237db-106">Donde:</span><span class="sxs-lookup"><span data-stu-id="237db-106">Where:</span></span>

-   <span data-ttu-id="237db-107">"R" denota cualquier tipo de registro que se pueda abordar relativamente.</span><span class="sxs-lookup"><span data-stu-id="237db-107">"R" denotes any register type that can be relatively addressed.</span></span>
-   <span data-ttu-id="237db-108">"A" denota cualquier registro que se pueda usar como índice para abordar relativamente otros registros.</span><span class="sxs-lookup"><span data-stu-id="237db-108">"A" denotes any register that can be used as an index to relatively address other registers.</span></span>
-   <span data-ttu-id="237db-109">n0 - ni, m0 - mj y k son enteros >= 0.</span><span class="sxs-lookup"><span data-stu-id="237db-109">n0 - ni, m0 - mj, and k are integers >= 0.</span></span>



| <span data-ttu-id="237db-110">\[\]sintaxis</span><span class="sxs-lookup"><span data-stu-id="237db-110">\[ \] syntax</span></span>                              | <span data-ttu-id="237db-111">Índice efectivo</span><span class="sxs-lookup"><span data-stu-id="237db-111">Effective index</span></span>                       | <span data-ttu-id="237db-112">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="237db-112">Examples</span></span>                         |
|-------------------------------------------|---------------------------------------|----------------------------------|
| <span data-ttu-id="237db-113">R \[ A + m0 + ... + mj \]</span><span class="sxs-lookup"><span data-stu-id="237db-113">R\[ A + m0 + ... + mj \]</span></span>                  | <span data-ttu-id="237db-114">A + m0 + ... + mj</span><span class="sxs-lookup"><span data-stu-id="237db-114">A + m0 + ... + mj</span></span>                     | <span data-ttu-id="237db-115">c \[ a0.x + 3 + 7 \]</span><span class="sxs-lookup"><span data-stu-id="237db-115">c\[ a0.x + 3 + 7 \]</span></span>              |
| <span data-ttu-id="237db-116">R \[ k ( = \] Rk )</span><span class="sxs-lookup"><span data-stu-id="237db-116">R\[ k \] ( = Rk )</span></span>                         | <span data-ttu-id="237db-117">k</span><span class="sxs-lookup"><span data-stu-id="237db-117">k</span></span>                                     | <span data-ttu-id="237db-118">c \[ 10 \] ( = c10 )</span><span class="sxs-lookup"><span data-stu-id="237db-118">c\[ 10 \] ( = c10 )</span></span>              |
| <span data-ttu-id="237db-119">R \[ A \]</span><span class="sxs-lookup"><span data-stu-id="237db-119">R\[ A \]</span></span>                                  | <span data-ttu-id="237db-120">A</span><span class="sxs-lookup"><span data-stu-id="237db-120">A</span></span>                                     | <span data-ttu-id="237db-121">c \[ a0.y \]</span><span class="sxs-lookup"><span data-stu-id="237db-121">c\[ a0.y \]</span></span>                      |
| <span data-ttu-id="237db-122">Rk \[ n0 + ... + ni + A + m0 + ... + mj \]</span><span class="sxs-lookup"><span data-stu-id="237db-122">Rk\[ n0 + ... + ni + A + m0 + ... + mj \]</span></span> | <span data-ttu-id="237db-123">A + k + n0 + ... + ni + m0 + ... + mj</span><span class="sxs-lookup"><span data-stu-id="237db-123">A + k + n0 + ... + ni + m0 + ... + mj</span></span> | <span data-ttu-id="237db-124">c8 \[ 3 + 2 + a0.w + 5 + 6 + 1 \]</span><span class="sxs-lookup"><span data-stu-id="237db-124">c8\[ 3 + 2 + a0.w + 5 + 6 + 1 \]</span></span> |
| <span data-ttu-id="237db-125">R \[ n0 + ... + ni + A + m0 + ... + mj \]</span><span class="sxs-lookup"><span data-stu-id="237db-125">R\[ n0 + ... + ni + A + m0 + ... + mj \]</span></span>  | <span data-ttu-id="237db-126">A + n0 + ... + ni + m0 + ... + mj</span><span class="sxs-lookup"><span data-stu-id="237db-126">A + n0 + ... + ni + m0 + ... + mj</span></span>     | <span data-ttu-id="237db-127">c \[ 2 + 1 + aL + 3 + 4 + 5 \]</span><span class="sxs-lookup"><span data-stu-id="237db-127">c\[ 2 + 1 + aL + 3 + 4 + 5 \]</span></span>    |
| <span data-ttu-id="237db-128">Rk \[ A \]</span><span class="sxs-lookup"><span data-stu-id="237db-128">Rk\[ A \]</span></span>                                 | <span data-ttu-id="237db-129">A + k</span><span class="sxs-lookup"><span data-stu-id="237db-129">A + k</span></span>                                 | <span data-ttu-id="237db-130">c12 \[ aL \] , c0 \[ a0.z \]</span><span class="sxs-lookup"><span data-stu-id="237db-130">c12\[ aL \], c0\[ a0.z \]</span></span>        |
| <span data-ttu-id="237db-131">Rk \[ A + m0 + ... + mj \]</span><span class="sxs-lookup"><span data-stu-id="237db-131">Rk\[ A + m0 + ... + mj \]</span></span>                 | <span data-ttu-id="237db-132">A + k + m0 + ... + mj</span><span class="sxs-lookup"><span data-stu-id="237db-132">A + k + m0 + ... + mj</span></span>                 | <span data-ttu-id="237db-133">v1 \[ aL + 4 + 8 \]</span><span class="sxs-lookup"><span data-stu-id="237db-133">v1\[ aL + 4 + 8 \]</span></span>               |
| <span data-ttu-id="237db-134">R \[ n0 + ... + ni + A \]</span><span class="sxs-lookup"><span data-stu-id="237db-134">R\[ n0 + ... + ni + A \]</span></span>                  | <span data-ttu-id="237db-135">A + n0 + ... + ni</span><span class="sxs-lookup"><span data-stu-id="237db-135">A + n0 + ... + ni</span></span>                     | <span data-ttu-id="237db-136">o \[ 3 + 1 + aL \]</span><span class="sxs-lookup"><span data-stu-id="237db-136">o\[ 3 + 1 + aL \]</span></span>                |
| <span data-ttu-id="237db-137">Rk \[ n0 + ... + ni + A \]</span><span class="sxs-lookup"><span data-stu-id="237db-137">Rk\[ n0 + ... + ni + A \]</span></span>                 | <span data-ttu-id="237db-138">A + k + n0 + ... + ni</span><span class="sxs-lookup"><span data-stu-id="237db-138">A + k + n0 + ... + ni</span></span>                 | <span data-ttu-id="237db-139">o1 \[ 2 + 1 + 3 + aL \]</span><span class="sxs-lookup"><span data-stu-id="237db-139">o1\[ 2 + 1 + 3 + aL \]</span></span>           |



 

<span data-ttu-id="237db-140">Los registros están disponibles en las siguientes versiones:</span><span class="sxs-lookup"><span data-stu-id="237db-140">The registers are available in the following versions:</span></span>



| <span data-ttu-id="237db-141">Tipo de registro</span><span class="sxs-lookup"><span data-stu-id="237db-141">Register type</span></span> | <span data-ttu-id="237db-142">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="237db-142">Vertex Shader Versions</span></span> |
|---------------|------------------------|
| <span data-ttu-id="237db-143">a0</span><span class="sxs-lookup"><span data-stu-id="237db-143">a0</span></span>            | <span data-ttu-id="237db-144">Todo</span><span class="sxs-lookup"><span data-stu-id="237db-144">All</span></span>                    |
| <span data-ttu-id="237db-145">aL</span><span class="sxs-lookup"><span data-stu-id="237db-145">aL</span></span>            | <span data-ttu-id="237db-146">vs \_ 2 \_ 0 y superiores</span><span class="sxs-lookup"><span data-stu-id="237db-146">vs\_2\_0 and higher</span></span>    |
| <span data-ttu-id="237db-147">cn</span><span class="sxs-lookup"><span data-stu-id="237db-147">cn</span></span>            | <span data-ttu-id="237db-148">vs \_ 1 \_ 1 y superiores</span><span class="sxs-lookup"><span data-stu-id="237db-148">vs\_1\_1 and higher</span></span>    |
| <span data-ttu-id="237db-149">on</span><span class="sxs-lookup"><span data-stu-id="237db-149">on</span></span>            | <span data-ttu-id="237db-150">vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="237db-150">vs\_3\_0</span></span>               |



 

## <a name="related-topics"></a><span data-ttu-id="237db-151">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="237db-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="237db-152">Registros del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="237db-152">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




