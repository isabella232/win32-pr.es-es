---
title: Predicado Register (referencia de PS de HLSL)
description: Este registro de salida del sombreador de píxeles contiene un valor booleano por canal.
ms.assetid: dc5bff90-4efa-4390-b744-dd1e894ff540
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 54c0706b110e04548c836bed8ae794f8da73747e
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2019
ms.locfileid: "103785068"
---
# <a name="predicate-register-hlsl-ps-reference"></a><span data-ttu-id="75aa3-103">Predicado Register (referencia de PS de HLSL)</span><span class="sxs-lookup"><span data-stu-id="75aa3-103">Predicate register (HLSL PS reference)</span></span>

<span data-ttu-id="75aa3-104">Este registro de salida del sombreador de píxeles contiene un valor booleano por canal.</span><span class="sxs-lookup"><span data-stu-id="75aa3-104">This pixel shader output register contains a per-channel boolean value.</span></span>

<span data-ttu-id="75aa3-105">Un registro de predicado es compatible con las siguientes versiones:</span><span class="sxs-lookup"><span data-stu-id="75aa3-105">A predicate register is supported by the following versions:</span></span>



| <span data-ttu-id="75aa3-106">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="75aa3-106">Pixel shader versions</span></span> | <span data-ttu-id="75aa3-107">1\_1</span><span class="sxs-lookup"><span data-stu-id="75aa3-107">1\_1</span></span> | <span data-ttu-id="75aa3-108">1\_2</span><span class="sxs-lookup"><span data-stu-id="75aa3-108">1\_2</span></span> | <span data-ttu-id="75aa3-109">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="75aa3-109">1\_3</span></span> | <span data-ttu-id="75aa3-110">1\_4</span><span class="sxs-lookup"><span data-stu-id="75aa3-110">1\_4</span></span> | <span data-ttu-id="75aa3-111">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="75aa3-111">2\_0</span></span> | <span data-ttu-id="75aa3-112">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="75aa3-112">2\_sw</span></span> | <span data-ttu-id="75aa3-113">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="75aa3-113">2\_x</span></span> | <span data-ttu-id="75aa3-114">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="75aa3-114">3\_0</span></span> | <span data-ttu-id="75aa3-115">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="75aa3-115">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="75aa3-116">registro de predicado</span><span class="sxs-lookup"><span data-stu-id="75aa3-116">predicate register</span></span>    |      |      |      |      |      |       | <span data-ttu-id="75aa3-117">x</span><span class="sxs-lookup"><span data-stu-id="75aa3-117">x</span></span>    | <span data-ttu-id="75aa3-118">x</span><span class="sxs-lookup"><span data-stu-id="75aa3-118">x</span></span>    | <span data-ttu-id="75aa3-119">x</span><span class="sxs-lookup"><span data-stu-id="75aa3-119">x</span></span>     |



 

<span data-ttu-id="75aa3-120">Estas son las propiedades de registro.</span><span class="sxs-lookup"><span data-stu-id="75aa3-120">Here are the register properties.</span></span>



| <span data-ttu-id="75aa3-121">Tipo de registro</span><span class="sxs-lookup"><span data-stu-id="75aa3-121">Register type</span></span> | <span data-ttu-id="75aa3-122">Count</span><span class="sxs-lookup"><span data-stu-id="75aa3-122">Count</span></span> | <span data-ttu-id="75aa3-123">L/E</span><span class="sxs-lookup"><span data-stu-id="75aa3-123">R/W</span></span> | <span data-ttu-id="75aa3-124">\# Leer puertos</span><span class="sxs-lookup"><span data-stu-id="75aa3-124">\# Read ports</span></span> | <span data-ttu-id="75aa3-125">\# Lecturas/inst.</span><span class="sxs-lookup"><span data-stu-id="75aa3-125">\# Reads/inst</span></span> | <span data-ttu-id="75aa3-126">Dimensión</span><span class="sxs-lookup"><span data-stu-id="75aa3-126">Dimension</span></span> | <span data-ttu-id="75aa3-127">RelAddr</span><span class="sxs-lookup"><span data-stu-id="75aa3-127">RelAddr</span></span> | <span data-ttu-id="75aa3-128">Valores predeterminados</span><span class="sxs-lookup"><span data-stu-id="75aa3-128">Defaults</span></span> | <span data-ttu-id="75aa3-129">Requiere DCL</span><span class="sxs-lookup"><span data-stu-id="75aa3-129">Requires DCL</span></span> |
|---------------|-------|-----|---------------|---------------|-----------|---------|----------|--------------|
| <span data-ttu-id="75aa3-130">Predicado (p)</span><span class="sxs-lookup"><span data-stu-id="75aa3-130">Predicate(p)</span></span>  | <span data-ttu-id="75aa3-131">1</span><span class="sxs-lookup"><span data-stu-id="75aa3-131">1</span></span>     | <span data-ttu-id="75aa3-132">L/E</span><span class="sxs-lookup"><span data-stu-id="75aa3-132">R/W</span></span> | <span data-ttu-id="75aa3-133">1</span><span class="sxs-lookup"><span data-stu-id="75aa3-133">1</span></span>             | <span data-ttu-id="75aa3-134">1</span><span class="sxs-lookup"><span data-stu-id="75aa3-134">1</span></span>             | <span data-ttu-id="75aa3-135">4</span><span class="sxs-lookup"><span data-stu-id="75aa3-135">4</span></span>         | <span data-ttu-id="75aa3-136">N/D</span><span class="sxs-lookup"><span data-stu-id="75aa3-136">N/A</span></span>     | <span data-ttu-id="75aa3-137">None</span><span class="sxs-lookup"><span data-stu-id="75aa3-137">None</span></span>     | <span data-ttu-id="75aa3-138">N</span><span class="sxs-lookup"><span data-stu-id="75aa3-138">N</span></span>            |



 

<span data-ttu-id="75aa3-139">El registro de predicado se puede modificar con [SETP \_ COMP-PS](setp-comp---ps.md).</span><span class="sxs-lookup"><span data-stu-id="75aa3-139">The predicate register can be modified with [setp\_comp - ps](setp-comp---ps.md).</span></span> <span data-ttu-id="75aa3-140">No hay valores predeterminados para este registro; una aplicación debe establecer el registro antes de que se use.</span><span class="sxs-lookup"><span data-stu-id="75aa3-140">There are no default values for this register; an application needs to set the register before it is used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="75aa3-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="75aa3-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75aa3-142">Registra</span><span class="sxs-lookup"><span data-stu-id="75aa3-142">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




