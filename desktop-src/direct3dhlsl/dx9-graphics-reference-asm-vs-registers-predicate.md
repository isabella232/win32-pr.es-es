---
title: Predicado Register (HLSL VS Reference)
description: Este registro de salida del sombreador de vértices contiene un valor booleano por canal.
ms.assetid: 4b06e19a-78c7-4886-a0e2-225d419282e7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f558a5fee10d0403eeaacab9dc29ff3ea52b427c
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2019
ms.locfileid: "104077144"
---
# <a name="predicate-register-hlsl-vs-reference"></a><span data-ttu-id="c72e5-103">Predicado Register (HLSL VS Reference)</span><span class="sxs-lookup"><span data-stu-id="c72e5-103">Predicate Register (HLSL VS reference)</span></span>

<span data-ttu-id="c72e5-104">Este registro de salida del sombreador de vértices contiene un valor booleano por canal.</span><span class="sxs-lookup"><span data-stu-id="c72e5-104">This vertex shader output register contains a per-channel Boolean value.</span></span>

<span data-ttu-id="c72e5-105">Un registro de predicado es compatible con las siguientes versiones.</span><span class="sxs-lookup"><span data-stu-id="c72e5-105">A predicate register is supported by the following versions.</span></span>



| <span data-ttu-id="c72e5-106">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="c72e5-106">Vertex shader versions</span></span> | <span data-ttu-id="c72e5-107">1\_1</span><span class="sxs-lookup"><span data-stu-id="c72e5-107">1\_1</span></span> | <span data-ttu-id="c72e5-108">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c72e5-108">2\_0</span></span> | <span data-ttu-id="c72e5-109">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c72e5-109">2\_sw</span></span> | <span data-ttu-id="c72e5-110">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c72e5-110">2\_x</span></span> | <span data-ttu-id="c72e5-111">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c72e5-111">3\_0</span></span> | <span data-ttu-id="c72e5-112">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c72e5-112">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="c72e5-113">registro de predicado</span><span class="sxs-lookup"><span data-stu-id="c72e5-113">predicate register</span></span>     |      |      |       | <span data-ttu-id="c72e5-114">x</span><span class="sxs-lookup"><span data-stu-id="c72e5-114">x</span></span>    | <span data-ttu-id="c72e5-115">x</span><span class="sxs-lookup"><span data-stu-id="c72e5-115">x</span></span>    | <span data-ttu-id="c72e5-116">x</span><span class="sxs-lookup"><span data-stu-id="c72e5-116">x</span></span>     |



 

<span data-ttu-id="c72e5-117">Estas son las propiedades de registro.</span><span class="sxs-lookup"><span data-stu-id="c72e5-117">Here are the register properties.</span></span>



| <span data-ttu-id="c72e5-118">Tipo de registro</span><span class="sxs-lookup"><span data-stu-id="c72e5-118">Register type</span></span> | <span data-ttu-id="c72e5-119">Count</span><span class="sxs-lookup"><span data-stu-id="c72e5-119">Count</span></span> | <span data-ttu-id="c72e5-120">L/E</span><span class="sxs-lookup"><span data-stu-id="c72e5-120">R/W</span></span> | <span data-ttu-id="c72e5-121">\# Leer puertos</span><span class="sxs-lookup"><span data-stu-id="c72e5-121">\# Read ports</span></span> | <span data-ttu-id="c72e5-122">\# Lecturas/inst.</span><span class="sxs-lookup"><span data-stu-id="c72e5-122">\# Reads/inst</span></span> | <span data-ttu-id="c72e5-123">Dimensión</span><span class="sxs-lookup"><span data-stu-id="c72e5-123">Dimension</span></span> | <span data-ttu-id="c72e5-124">RelAddr</span><span class="sxs-lookup"><span data-stu-id="c72e5-124">RelAddr</span></span> | <span data-ttu-id="c72e5-125">Valores predeterminados</span><span class="sxs-lookup"><span data-stu-id="c72e5-125">Defaults</span></span> | <span data-ttu-id="c72e5-126">Requiere DCL</span><span class="sxs-lookup"><span data-stu-id="c72e5-126">Requires DCL</span></span> |
|---------------|-------|-----|---------------|---------------|-----------|---------|----------|--------------|
| <span data-ttu-id="c72e5-127">Predicado (p)</span><span class="sxs-lookup"><span data-stu-id="c72e5-127">Predicate(p)</span></span>  | <span data-ttu-id="c72e5-128">1</span><span class="sxs-lookup"><span data-stu-id="c72e5-128">1</span></span>     | <span data-ttu-id="c72e5-129">L/E</span><span class="sxs-lookup"><span data-stu-id="c72e5-129">R/W</span></span> | <span data-ttu-id="c72e5-130">1</span><span class="sxs-lookup"><span data-stu-id="c72e5-130">1</span></span>             | <span data-ttu-id="c72e5-131">1</span><span class="sxs-lookup"><span data-stu-id="c72e5-131">1</span></span>             | <span data-ttu-id="c72e5-132">4</span><span class="sxs-lookup"><span data-stu-id="c72e5-132">4</span></span>         | <span data-ttu-id="c72e5-133">N/D</span><span class="sxs-lookup"><span data-stu-id="c72e5-133">N/A</span></span>     | <span data-ttu-id="c72e5-134">None</span><span class="sxs-lookup"><span data-stu-id="c72e5-134">None</span></span>     | <span data-ttu-id="c72e5-135">N</span><span class="sxs-lookup"><span data-stu-id="c72e5-135">N</span></span>            |



 

<span data-ttu-id="c72e5-136">El registro de predicado se puede modificar con [SETP \_ COMP-vs](setp-comp---vs.md). No hay valores predeterminados para este registro, una aplicación debe establecer el registro antes de que se use.</span><span class="sxs-lookup"><span data-stu-id="c72e5-136">The predicate register can be modified with [setp\_comp - vs](setp-comp---vs.md). There are no default values for this register, an application needs to set the register before it is used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c72e5-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c72e5-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c72e5-138">Registros del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="c72e5-138">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




