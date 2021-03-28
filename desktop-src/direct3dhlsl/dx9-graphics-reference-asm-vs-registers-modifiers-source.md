---
title: Modificadores de registro de origen del sombreador de vértices
description: Los modificadores de origen se pueden aplicar para modificar los datos leídos de un registro de origen antes de que la instrucción use los datos.
ms.assetid: 516ff7ca-0071-44ac-a246-612a9faa7e7b
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 49c663741da50620e03cfde9f13d67a0c0063453
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418912"
---
# <a name="vertex-shader-source-register-modifiers"></a><span data-ttu-id="5320c-103">Modificadores de registro de origen del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="5320c-103">Vertex Shader Source Register Modifiers</span></span>

<span data-ttu-id="5320c-104">Los modificadores de origen se pueden aplicar para modificar los datos leídos de un registro de origen antes de que la instrucción use los datos.</span><span class="sxs-lookup"><span data-stu-id="5320c-104">Source modifiers can be applied to modify the data read from a source register before the data is used by the instruction.</span></span>

## <a name="negate"></a><span data-ttu-id="5320c-105">Negate</span><span class="sxs-lookup"><span data-stu-id="5320c-105">Negate</span></span>

<span data-ttu-id="5320c-106">Niega el contenido del registro de origen.</span><span class="sxs-lookup"><span data-stu-id="5320c-106">Negate the contents of the source register.</span></span>



| <span data-ttu-id="5320c-107">Modificador de componente</span><span class="sxs-lookup"><span data-stu-id="5320c-107">Component modifier</span></span> | <span data-ttu-id="5320c-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="5320c-108">Description</span></span>     |
|--------------------|-----------------|
| <span data-ttu-id="5320c-109">\- c</span><span class="sxs-lookup"><span data-stu-id="5320c-109">\- r</span></span>               | <span data-ttu-id="5320c-110">Negación de origen</span><span class="sxs-lookup"><span data-stu-id="5320c-110">Source negation</span></span> |



 

<span data-ttu-id="5320c-111">No se puede usar el modificador Negate en el segundo registro de código fuente de estas instrucciones: [m3x2-vs](m3x2---vs.md), [M3x3-vs](m3x3---vs.md), [M3x4-vs](m3x4---vs.md), [m4x3-vs](m4x3---vs.md), [M4x4-vs](m4x4---vs.md).</span><span class="sxs-lookup"><span data-stu-id="5320c-111">The negate modifier cannot be used on second source register of these instructions: [m3x2 - vs](m3x2---vs.md), [m3x3 - vs](m3x3---vs.md), [m3x4 - vs](m3x4---vs.md), [m4x3 - vs](m4x3---vs.md), [m4x4 - vs](m4x4---vs.md).</span></span>



| <span data-ttu-id="5320c-112">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="5320c-112">Vertex shader versions</span></span> | <span data-ttu-id="5320c-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="5320c-113">1\_1</span></span> | <span data-ttu-id="5320c-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5320c-114">2\_0</span></span> | <span data-ttu-id="5320c-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5320c-115">2\_x</span></span> | <span data-ttu-id="5320c-116">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5320c-116">2\_sw</span></span> | <span data-ttu-id="5320c-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5320c-117">3\_0</span></span> | <span data-ttu-id="5320c-118">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5320c-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| \-                     | <span data-ttu-id="5320c-119">x</span><span class="sxs-lookup"><span data-stu-id="5320c-119">x</span></span>    | <span data-ttu-id="5320c-120">x</span><span class="sxs-lookup"><span data-stu-id="5320c-120">x</span></span>    | <span data-ttu-id="5320c-121">x</span><span class="sxs-lookup"><span data-stu-id="5320c-121">x</span></span>    | <span data-ttu-id="5320c-122">x</span><span class="sxs-lookup"><span data-stu-id="5320c-122">x</span></span>     | <span data-ttu-id="5320c-123">x</span><span class="sxs-lookup"><span data-stu-id="5320c-123">x</span></span>    | <span data-ttu-id="5320c-124">x</span><span class="sxs-lookup"><span data-stu-id="5320c-124">x</span></span>     |



 

## <a name="absolute-value"></a><span data-ttu-id="5320c-125">Valor absoluto</span><span class="sxs-lookup"><span data-stu-id="5320c-125">Absolute Value</span></span>

<span data-ttu-id="5320c-126">Tome el valor absoluto del registro.</span><span class="sxs-lookup"><span data-stu-id="5320c-126">Take the absolute value of the register.</span></span>



| <span data-ttu-id="5320c-127">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="5320c-127">Vertex shader versions</span></span> | <span data-ttu-id="5320c-128">1\_1</span><span class="sxs-lookup"><span data-stu-id="5320c-128">1\_1</span></span> | <span data-ttu-id="5320c-129">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5320c-129">2\_0</span></span> | <span data-ttu-id="5320c-130">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5320c-130">2\_x</span></span> | <span data-ttu-id="5320c-131">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5320c-131">2\_sw</span></span> | <span data-ttu-id="5320c-132">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5320c-132">3\_0</span></span> | <span data-ttu-id="5320c-133">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5320c-133">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="5320c-134">abs</span><span class="sxs-lookup"><span data-stu-id="5320c-134">abs</span></span>                    |      |      |      |       | <span data-ttu-id="5320c-135">x</span><span class="sxs-lookup"><span data-stu-id="5320c-135">x</span></span>    | <span data-ttu-id="5320c-136">x</span><span class="sxs-lookup"><span data-stu-id="5320c-136">x</span></span>     |



 

<span data-ttu-id="5320c-137">Si cualquier sombreador de la versión 3 Lee de uno o más registros Float constantes (c \# ), debe cumplirse una de las siguientes condiciones.</span><span class="sxs-lookup"><span data-stu-id="5320c-137">If any version 3 shader reads from one or more constant float registers (c\#), one of the following must be true.</span></span>

-   <span data-ttu-id="5320c-138">Todos los registros de punto flotante constantes deben usar el modificador ABS.</span><span class="sxs-lookup"><span data-stu-id="5320c-138">All of the constant floating-point registers must use the abs modifier.</span></span>
-   <span data-ttu-id="5320c-139">Ninguno de los registros de punto flotante constantes puede usar el modificador ABS.</span><span class="sxs-lookup"><span data-stu-id="5320c-139">None of the constant floating-point registers can use the abs modifier.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5320c-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5320c-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5320c-141">Modificadores de registro del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="5320c-141">Vertex Shader Register Modifiers</span></span>](dx9-graphics-reference-asm-vs-registers-modifiers.md)
</dt> </dl>

 

 




