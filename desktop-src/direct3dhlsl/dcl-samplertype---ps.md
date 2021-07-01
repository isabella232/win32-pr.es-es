---
title: dcl_samplerType (sm2, sm3 - ps asm)
description: Declare un muestreador de sombreador de píxeles.
ms.assetid: c90ff5b6-f89a-4993-8a5d-dbbc4a7896b0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7a6da220e50b43ce990c090c61d1caf84afec653
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129672"
---
# <a name="dcl_samplertype-sm2-sm3---ps-asm"></a><span data-ttu-id="367b9-103">dcl \_ samplerType (sm2, sm3 - ps asm)</span><span class="sxs-lookup"><span data-stu-id="367b9-103">dcl\_samplerType (sm2, sm3 - ps asm)</span></span>

<span data-ttu-id="367b9-104">Declare un muestreador de sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="367b9-104">Declare a pixel shader sampler.</span></span>

## <a name="syntax"></a><span data-ttu-id="367b9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="367b9-105">Syntax</span></span>

<span data-ttu-id="367b9-106">dcl \_ samplerType s\#</span><span class="sxs-lookup"><span data-stu-id="367b9-106">dcl\_samplerType s\#</span></span>



 

<span data-ttu-id="367b9-107">donde:</span><span class="sxs-lookup"><span data-stu-id="367b9-107">where:</span></span>

-   <span data-ttu-id="367b9-108">\_samplerType define el tipo de datos sampler.</span><span class="sxs-lookup"><span data-stu-id="367b9-108">\_samplerType defines the sampler data type.</span></span> <span data-ttu-id="367b9-109">Esto determina cuántas coordenadas son necesarias para cada coordenada de textura al realizar el muestreo.</span><span class="sxs-lookup"><span data-stu-id="367b9-109">This determines how many coordinates are required by each texture coordinate when sampling.</span></span> <span data-ttu-id="367b9-110">Se definen las siguientes dimensiones de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="367b9-110">The following texture coordinate dimensions are defined.</span></span>
    -   <span data-ttu-id="367b9-111">\_2d</span><span class="sxs-lookup"><span data-stu-id="367b9-111">\_2d</span></span>
    -   <span data-ttu-id="367b9-112">\_Cubo</span><span class="sxs-lookup"><span data-stu-id="367b9-112">\_cube</span></span>
    -   <span data-ttu-id="367b9-113">\_volumen</span><span class="sxs-lookup"><span data-stu-id="367b9-113">\_volume</span></span>
-   <span data-ttu-id="367b9-114">s identifica un sampler donde s es una abreviatura del muestreador \# y es el número del \# muestreador.</span><span class="sxs-lookup"><span data-stu-id="367b9-114">s\# identifies a sampler where s is an abbreviation for the sampler, and \# is the sampler number.</span></span> <span data-ttu-id="367b9-115">Los muestreadores son pseudo registros porque no se pueden leer ni escribir directamente en ellos.</span><span class="sxs-lookup"><span data-stu-id="367b9-115">Samplers are pseudo registers because you cannot directly read or write to them.</span></span>

## <a name="remarks"></a><span data-ttu-id="367b9-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="367b9-116">Remarks</span></span>



| <span data-ttu-id="367b9-117">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="367b9-117">Pixel shader versions</span></span> | <span data-ttu-id="367b9-118">1\_1</span><span class="sxs-lookup"><span data-stu-id="367b9-118">1\_1</span></span> | <span data-ttu-id="367b9-119">1\_2</span><span class="sxs-lookup"><span data-stu-id="367b9-119">1\_2</span></span> | <span data-ttu-id="367b9-120">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="367b9-120">1\_3</span></span> | <span data-ttu-id="367b9-121">1\_4</span><span class="sxs-lookup"><span data-stu-id="367b9-121">1\_4</span></span> | <span data-ttu-id="367b9-122">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="367b9-122">2\_0</span></span> | <span data-ttu-id="367b9-123">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="367b9-123">2\_x</span></span> | <span data-ttu-id="367b9-124">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="367b9-124">2\_sw</span></span> | <span data-ttu-id="367b9-125">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="367b9-125">3\_0</span></span> | <span data-ttu-id="367b9-126">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="367b9-126">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="367b9-127">dcl \_ samplerType</span><span class="sxs-lookup"><span data-stu-id="367b9-127">dcl\_samplerType</span></span>      |      |      |      |      | <span data-ttu-id="367b9-128">x</span><span class="sxs-lookup"><span data-stu-id="367b9-128">x</span></span>    | <span data-ttu-id="367b9-129">x</span><span class="sxs-lookup"><span data-stu-id="367b9-129">x</span></span>    | <span data-ttu-id="367b9-130">x</span><span class="sxs-lookup"><span data-stu-id="367b9-130">x</span></span>     | <span data-ttu-id="367b9-131">x</span><span class="sxs-lookup"><span data-stu-id="367b9-131">x</span></span>    | <span data-ttu-id="367b9-132">x</span><span class="sxs-lookup"><span data-stu-id="367b9-132">x</span></span>     |



 

<span data-ttu-id="367b9-133">Todas las instrucciones \_ dcl samplerType deben aparecer antes de la primera instrucción ejecutable.</span><span class="sxs-lookup"><span data-stu-id="367b9-133">All dcl\_samplerType instructions must appear before the first executable instruction.</span></span>

## <a name="example"></a><span data-ttu-id="367b9-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="367b9-134">Example</span></span>


```
dcl_cube t0.rgb;  // Define a 3D texture map.

add r0, r0, t0;   // Perturb texture coordinates. 
texld r0, s0, r0; // Load r0 with a color sampled from stage0
                  //   at perturbed texture coordinates r0.
                  // This is a dependent texture read.
```



## <a name="related-topics"></a><span data-ttu-id="367b9-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="367b9-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="367b9-136">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="367b9-136">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




