---
title: Direccionamiento relativo (referencia de HLSL PS)
description: En el caso de los sombreadores de píxeles, la sintaxis \ \ solo se puede usar en tipos de registro que se puedan abordar relativamente en determinados modelos de sombreador.
ms.assetid: 37e2bab9-f6fe-438a-8a2d-c963634ef8c3
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8bdafe23696c460da75d87cf1f6d5a968c89ed28
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405488"
---
# <a name="relative-addressing-hlsl-ps-reference"></a><span data-ttu-id="c471c-103">Direccionamiento relativo (referencia de HLSL PS)</span><span class="sxs-lookup"><span data-stu-id="c471c-103">Relative addressing (HLSL PS reference)</span></span>

<span data-ttu-id="c471c-104">La \[ \] sintaxis solo se puede usar en tipos de registro que se puedan abordar relativamente en determinados modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="c471c-104">The \[ \] syntax can be used only in register types that can be relatively addressed in certain shader models.</span></span> <span data-ttu-id="c471c-105">Las formas de \[ \] sintaxis admitidas se enumeran de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="c471c-105">The supported forms of \[ \] syntax are listed as follows:</span></span>

<span data-ttu-id="c471c-106">Donde:</span><span class="sxs-lookup"><span data-stu-id="c471c-106">Where:</span></span>

-   <span data-ttu-id="c471c-107">"R" denota cualquier tipo de registro que se pueda abordar relativamente.</span><span class="sxs-lookup"><span data-stu-id="c471c-107">"R" denotes any register type that can be relatively addressed.</span></span>
-   <span data-ttu-id="c471c-108">"A" denota cualquier registro que se pueda usar como índice para abordar relativamente otros registros.</span><span class="sxs-lookup"><span data-stu-id="c471c-108">"A" denotes any register that can be used as an index to relatively address other registers.</span></span>
-   <span data-ttu-id="c471c-109">n0 - ni, m0 - mj y k son enteros >= 0.</span><span class="sxs-lookup"><span data-stu-id="c471c-109">n0 - ni, m0 - mj, and k are integers >= 0.</span></span>



| <span data-ttu-id="c471c-110">\[\]sintaxis</span><span class="sxs-lookup"><span data-stu-id="c471c-110">\[ \] syntax</span></span>                              | <span data-ttu-id="c471c-111">Índice efectivo</span><span class="sxs-lookup"><span data-stu-id="c471c-111">Effective index</span></span>                       | <span data-ttu-id="c471c-112">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c471c-112">Examples</span></span>                         |
|-------------------------------------------|---------------------------------------|----------------------------------|
| <span data-ttu-id="c471c-113">R \[ A + m0 + ... + mj \]</span><span class="sxs-lookup"><span data-stu-id="c471c-113">R\[ A + m0 + ... + mj \]</span></span>                  | <span data-ttu-id="c471c-114">A + m0 + ... + mj</span><span class="sxs-lookup"><span data-stu-id="c471c-114">A + m0 + ... + mj</span></span>                     | <span data-ttu-id="c471c-115">c \[ a0.x + 3 + 7 \]</span><span class="sxs-lookup"><span data-stu-id="c471c-115">c\[ a0.x + 3 + 7 \]</span></span>              |
| <span data-ttu-id="c471c-116">R \[ k ( = \] Rk )</span><span class="sxs-lookup"><span data-stu-id="c471c-116">R\[ k \] ( = Rk )</span></span>                         | <span data-ttu-id="c471c-117">k</span><span class="sxs-lookup"><span data-stu-id="c471c-117">k</span></span>                                     | <span data-ttu-id="c471c-118">c \[ 10 \] ( = c10 )</span><span class="sxs-lookup"><span data-stu-id="c471c-118">c\[ 10 \] ( = c10 )</span></span>              |
| <span data-ttu-id="c471c-119">R \[ A \]</span><span class="sxs-lookup"><span data-stu-id="c471c-119">R\[ A \]</span></span>                                  | <span data-ttu-id="c471c-120">A</span><span class="sxs-lookup"><span data-stu-id="c471c-120">A</span></span>                                     | <span data-ttu-id="c471c-121">c \[ a0.y \]</span><span class="sxs-lookup"><span data-stu-id="c471c-121">c\[ a0.y \]</span></span>                      |
| <span data-ttu-id="c471c-122">Rk \[ n0 + ... + ni + A + m0 + ... + mj \]</span><span class="sxs-lookup"><span data-stu-id="c471c-122">Rk\[ n0 + ... + ni + A + m0 + ... + mj \]</span></span> | <span data-ttu-id="c471c-123">A + k + n0 + ... + ni + m0 + ... + mj</span><span class="sxs-lookup"><span data-stu-id="c471c-123">A + k + n0 + ... + ni + m0 + ... + mj</span></span> | <span data-ttu-id="c471c-124">c8 \[ 3 + 2 + a0.w + 5 + 6 + 1 \]</span><span class="sxs-lookup"><span data-stu-id="c471c-124">c8\[ 3 + 2 + a0.w + 5 + 6 + 1 \]</span></span> |
| <span data-ttu-id="c471c-125">R \[ n0 + ... + ni + A + m0 + ... + mj \]</span><span class="sxs-lookup"><span data-stu-id="c471c-125">R\[ n0 + ... + ni + A + m0 + ... + mj \]</span></span>  | <span data-ttu-id="c471c-126">A + n0 + ... + ni + m0 + ... + mj</span><span class="sxs-lookup"><span data-stu-id="c471c-126">A + n0 + ... + ni + m0 + ... + mj</span></span>     | <span data-ttu-id="c471c-127">c \[ 2 + 1 + aL + 3 + 4 + 5 \]</span><span class="sxs-lookup"><span data-stu-id="c471c-127">c\[ 2 + 1 + aL + 3 + 4 + 5 \]</span></span>    |
| <span data-ttu-id="c471c-128">Rk \[ A \]</span><span class="sxs-lookup"><span data-stu-id="c471c-128">Rk\[ A \]</span></span>                                 | <span data-ttu-id="c471c-129">A + k</span><span class="sxs-lookup"><span data-stu-id="c471c-129">A + k</span></span>                                 | <span data-ttu-id="c471c-130">c12 \[ aL \] , c0 \[ a0.z \]</span><span class="sxs-lookup"><span data-stu-id="c471c-130">c12\[ aL \], c0\[ a0.z \]</span></span>        |
| <span data-ttu-id="c471c-131">Rk \[ A + m0 + ... + mj \]</span><span class="sxs-lookup"><span data-stu-id="c471c-131">Rk\[ A + m0 + ... + mj \]</span></span>                 | <span data-ttu-id="c471c-132">A + k + m0 + ... + mj</span><span class="sxs-lookup"><span data-stu-id="c471c-132">A + k + m0 + ... + mj</span></span>                 | <span data-ttu-id="c471c-133">v1 \[ aL + 4 + 8 \]</span><span class="sxs-lookup"><span data-stu-id="c471c-133">v1\[ aL + 4 + 8 \]</span></span>               |
| <span data-ttu-id="c471c-134">R \[ n0 + ... + ni + A \]</span><span class="sxs-lookup"><span data-stu-id="c471c-134">R\[ n0 + ... + ni + A \]</span></span>                  | <span data-ttu-id="c471c-135">A + n0 + ... + ni</span><span class="sxs-lookup"><span data-stu-id="c471c-135">A + n0 + ... + ni</span></span>                     | <span data-ttu-id="c471c-136">o \[ 3 + 1 + aL \]</span><span class="sxs-lookup"><span data-stu-id="c471c-136">o\[ 3 + 1 + aL \]</span></span>                |
| <span data-ttu-id="c471c-137">Rk \[ n0 + ... + ni + A \]</span><span class="sxs-lookup"><span data-stu-id="c471c-137">Rk\[ n0 + ... + ni + A \]</span></span>                 | <span data-ttu-id="c471c-138">A + k + n0 + ... + ni</span><span class="sxs-lookup"><span data-stu-id="c471c-138">A + k + n0 + ... + ni</span></span>                 | <span data-ttu-id="c471c-139">o1 \[ 2 + 1 + 3 + aL \]</span><span class="sxs-lookup"><span data-stu-id="c471c-139">o1\[ 2 + 1 + 3 + aL \]</span></span>           |



 

<span data-ttu-id="c471c-140">Los registros están disponibles en las siguientes versiones:</span><span class="sxs-lookup"><span data-stu-id="c471c-140">The registers are available in the following versions:</span></span>



| <span data-ttu-id="c471c-141">Tipo de registro</span><span class="sxs-lookup"><span data-stu-id="c471c-141">Register type</span></span>                                                                                   | <span data-ttu-id="c471c-142">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="c471c-142">Pixel Shader Versions</span></span> |
|-------------------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="c471c-143">[loop counter](dx9-graphics-reference-asm-ps-registers-loop-counter.md): aL en los registros de entrada</span><span class="sxs-lookup"><span data-stu-id="c471c-143">[loop counter](dx9-graphics-reference-asm-ps-registers-loop-counter.md): aL on input registers</span></span> | <span data-ttu-id="c471c-144">ps \_ 3 \_ 0 y superior</span><span class="sxs-lookup"><span data-stu-id="c471c-144">ps\_3\_0 and higher</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="c471c-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c471c-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c471c-146">Registros</span><span class="sxs-lookup"><span data-stu-id="c471c-146">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




