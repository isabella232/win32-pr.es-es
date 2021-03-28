---
title: dcl_samplerType (SM3-vs ASM)
description: Declare una muestra de sombreador de vértices.
ms.assetid: 733307ac-24ab-4db7-bf70-58a83b4c39b1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 556655d793e94b9290fcd1a4a40fdf7f797e80ae
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996969"
---
# <a name="dcl_samplertype-sm3---vs-asm"></a><span data-ttu-id="7e8cc-103">DCL \_ samplerType (SM3-vs ASM)</span><span class="sxs-lookup"><span data-stu-id="7e8cc-103">dcl\_samplerType (sm3 - vs asm)</span></span>

<span data-ttu-id="7e8cc-104">Declare una muestra de sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="7e8cc-104">Declare a vertex shader sampler.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e8cc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7e8cc-105">Syntax</span></span>



|                      |
|----------------------|
| <span data-ttu-id="7e8cc-106">DCL \_ samplerType s\#</span><span class="sxs-lookup"><span data-stu-id="7e8cc-106">dcl\_samplerType s\#</span></span> |



 

<span data-ttu-id="7e8cc-107">donde:</span><span class="sxs-lookup"><span data-stu-id="7e8cc-107">where:</span></span>

-   <span data-ttu-id="7e8cc-108">\_samplerType define el tipo de datos de muestra.</span><span class="sxs-lookup"><span data-stu-id="7e8cc-108">\_samplerType defines the sampler data type.</span></span> <span data-ttu-id="7e8cc-109">Esto determina el número de coordenadas que requiere cada coordenada de textura al realizar el muestreo.</span><span class="sxs-lookup"><span data-stu-id="7e8cc-109">This determines how many coordinates are required by each texture coordinate when sampling.</span></span> <span data-ttu-id="7e8cc-110">Se definen las siguientes dimensiones de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="7e8cc-110">The following texture coordinate dimensions are defined.</span></span>
    -   <span data-ttu-id="7e8cc-111">\_2D</span><span class="sxs-lookup"><span data-stu-id="7e8cc-111">\_2d</span></span>
    -   <span data-ttu-id="7e8cc-112">\_BD</span><span class="sxs-lookup"><span data-stu-id="7e8cc-112">\_cube</span></span>
    -   <span data-ttu-id="7e8cc-113">\_cantidad</span><span class="sxs-lookup"><span data-stu-id="7e8cc-113">\_volume</span></span>
-   <span data-ttu-id="7e8cc-114">s \# identifica una muestra donde s es una abreviatura de la muestra y \# es el número de muestra.</span><span class="sxs-lookup"><span data-stu-id="7e8cc-114">s\# identifies a sampler where s is an abbreviation for the sampler, and \# is the sampler number.</span></span> <span data-ttu-id="7e8cc-115">El [muestreador (Direct3D 9 ASM-vs) es un](dx9-graphics-reference-asm-vs-registers-sampler.md)pseudo registro porque no se puede leer ni escribir directamente en ellos.</span><span class="sxs-lookup"><span data-stu-id="7e8cc-115">[Sampler (Direct3D 9 asm-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md)s are pseudo registers because you cannot directly read or write to them.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e8cc-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7e8cc-116">Remarks</span></span>



| <span data-ttu-id="7e8cc-117">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="7e8cc-117">Vertex shader versions</span></span> | <span data-ttu-id="7e8cc-118">1\_1</span><span class="sxs-lookup"><span data-stu-id="7e8cc-118">1\_1</span></span> | <span data-ttu-id="7e8cc-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7e8cc-119">2\_0</span></span> | <span data-ttu-id="7e8cc-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="7e8cc-120">2\_x</span></span> | <span data-ttu-id="7e8cc-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7e8cc-121">2\_sw</span></span> | <span data-ttu-id="7e8cc-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7e8cc-122">3\_0</span></span> | <span data-ttu-id="7e8cc-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7e8cc-123">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="7e8cc-124">samplerType de DCL \_</span><span class="sxs-lookup"><span data-stu-id="7e8cc-124">dcl\_samplerType</span></span>       |      |      |      |       | <span data-ttu-id="7e8cc-125">x</span><span class="sxs-lookup"><span data-stu-id="7e8cc-125">x</span></span>    | <span data-ttu-id="7e8cc-126">x</span><span class="sxs-lookup"><span data-stu-id="7e8cc-126">x</span></span>     |



 

<span data-ttu-id="7e8cc-127">Todas \_ las instrucciones samplerType de DCL deben aparecer antes de la primera instrucción ejecutable.</span><span class="sxs-lookup"><span data-stu-id="7e8cc-127">All dcl\_samplerType instructions must appear before the first executable instruction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7e8cc-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7e8cc-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e8cc-129">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="7e8cc-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




