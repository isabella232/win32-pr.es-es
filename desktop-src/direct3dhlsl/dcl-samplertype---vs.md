---
title: dcl_samplerType (sm3 - vs asm)
description: Declare un muestreador de sombreador de vértices.
ms.assetid: 733307ac-24ab-4db7-bf70-58a83b4c39b1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2fbcb934ad591274d743f09c810de2db42278261
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129873"
---
# <a name="dcl_samplertype-sm3---vs-asm"></a><span data-ttu-id="5e7e1-103">dcl \_ samplerType (sm3 - vs asm)</span><span class="sxs-lookup"><span data-stu-id="5e7e1-103">dcl\_samplerType (sm3 - vs asm)</span></span>

<span data-ttu-id="5e7e1-104">Declare un muestreador de sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="5e7e1-104">Declare a vertex shader sampler.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e7e1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5e7e1-105">Syntax</span></span>

<span data-ttu-id="5e7e1-106">dcl \_ samplerType s\#</span><span class="sxs-lookup"><span data-stu-id="5e7e1-106">dcl\_samplerType s\#</span></span>



 

<span data-ttu-id="5e7e1-107">donde:</span><span class="sxs-lookup"><span data-stu-id="5e7e1-107">where:</span></span>

-   <span data-ttu-id="5e7e1-108">\_samplerType define el tipo de datos sampler.</span><span class="sxs-lookup"><span data-stu-id="5e7e1-108">\_samplerType defines the sampler data type.</span></span> <span data-ttu-id="5e7e1-109">Esto determina cuántas coordenadas son necesarias para cada coordenada de textura al realizar el muestreo.</span><span class="sxs-lookup"><span data-stu-id="5e7e1-109">This determines how many coordinates are required by each texture coordinate when sampling.</span></span> <span data-ttu-id="5e7e1-110">Se definen las siguientes dimensiones de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="5e7e1-110">The following texture coordinate dimensions are defined.</span></span>
    -   <span data-ttu-id="5e7e1-111">\_2d</span><span class="sxs-lookup"><span data-stu-id="5e7e1-111">\_2d</span></span>
    -   <span data-ttu-id="5e7e1-112">\_Cubo</span><span class="sxs-lookup"><span data-stu-id="5e7e1-112">\_cube</span></span>
    -   <span data-ttu-id="5e7e1-113">\_volumen</span><span class="sxs-lookup"><span data-stu-id="5e7e1-113">\_volume</span></span>
-   <span data-ttu-id="5e7e1-114">s identifica un sampler donde s es una abreviatura del muestreador \# y es el número del \# muestreador.</span><span class="sxs-lookup"><span data-stu-id="5e7e1-114">s\# identifies a sampler where s is an abbreviation for the sampler, and \# is the sampler number.</span></span> <span data-ttu-id="5e7e1-115">[Sampler (Direct3D 9 asm-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md)s son pseudo registros porque no se pueden leer ni escribir directamente en ellos.</span><span class="sxs-lookup"><span data-stu-id="5e7e1-115">[Sampler (Direct3D 9 asm-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md)s are pseudo registers because you cannot directly read or write to them.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e7e1-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5e7e1-116">Remarks</span></span>



| <span data-ttu-id="5e7e1-117">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="5e7e1-117">Vertex shader versions</span></span> | <span data-ttu-id="5e7e1-118">1\_1</span><span class="sxs-lookup"><span data-stu-id="5e7e1-118">1\_1</span></span> | <span data-ttu-id="5e7e1-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5e7e1-119">2\_0</span></span> | <span data-ttu-id="5e7e1-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5e7e1-120">2\_x</span></span> | <span data-ttu-id="5e7e1-121">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="5e7e1-121">2\_sw</span></span> | <span data-ttu-id="5e7e1-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5e7e1-122">3\_0</span></span> | <span data-ttu-id="5e7e1-123">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="5e7e1-123">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="5e7e1-124">dcl \_ samplerType</span><span class="sxs-lookup"><span data-stu-id="5e7e1-124">dcl\_samplerType</span></span>       |      |      |      |       | <span data-ttu-id="5e7e1-125">x</span><span class="sxs-lookup"><span data-stu-id="5e7e1-125">x</span></span>    | <span data-ttu-id="5e7e1-126">x</span><span class="sxs-lookup"><span data-stu-id="5e7e1-126">x</span></span>     |



 

<span data-ttu-id="5e7e1-127">Todas las instrucciones \_ dcl samplerType deben aparecer antes de la primera instrucción ejecutable.</span><span class="sxs-lookup"><span data-stu-id="5e7e1-127">All dcl\_samplerType instructions must appear before the first executable instruction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5e7e1-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5e7e1-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e7e1-129">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="5e7e1-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




