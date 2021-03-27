---
title: Registro de posición
description: Este registro de salida del sombreador de vértices contiene datos de posición por vértice.
ms.assetid: 98f71027-d94b-4dd0-a6b6-4b263954eff9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 89470bb920db7c612b21cefb2c44c2c89d48ce28
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776621"
---
# <a name="position-register"></a><span data-ttu-id="0a187-103">Registro de posición</span><span class="sxs-lookup"><span data-stu-id="0a187-103">Position Register</span></span>

<span data-ttu-id="0a187-104">Este registro de salida del sombreador de vértices contiene datos de posición por vértice.</span><span class="sxs-lookup"><span data-stu-id="0a187-104">This vertex shader output register contains per-vertex position data.</span></span>



| <span data-ttu-id="0a187-105">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="0a187-105">Vertex shader versions</span></span> | <span data-ttu-id="0a187-106">1\_1</span><span class="sxs-lookup"><span data-stu-id="0a187-106">1\_1</span></span> | <span data-ttu-id="0a187-107">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0a187-107">2\_0</span></span> | <span data-ttu-id="0a187-108">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0a187-108">2\_sw</span></span> | <span data-ttu-id="0a187-109">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="0a187-109">2\_x</span></span> | <span data-ttu-id="0a187-110">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0a187-110">3\_0</span></span> | <span data-ttu-id="0a187-111">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0a187-111">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="0a187-112">Registro de posición</span><span class="sxs-lookup"><span data-stu-id="0a187-112">Position Register</span></span>      | <span data-ttu-id="0a187-113">x</span><span class="sxs-lookup"><span data-stu-id="0a187-113">x</span></span>    | <span data-ttu-id="0a187-114">x</span><span class="sxs-lookup"><span data-stu-id="0a187-114">x</span></span>    | <span data-ttu-id="0a187-115">x</span><span class="sxs-lookup"><span data-stu-id="0a187-115">x</span></span>     | <span data-ttu-id="0a187-116">x</span><span class="sxs-lookup"><span data-stu-id="0a187-116">x</span></span>    | <span data-ttu-id="0a187-117">x</span><span class="sxs-lookup"><span data-stu-id="0a187-117">x</span></span>    | <span data-ttu-id="0a187-118">x</span><span class="sxs-lookup"><span data-stu-id="0a187-118">x</span></span>     |



 

<span data-ttu-id="0a187-119">Un registro consta de propiedades que determinan el comportamiento de cada registro.</span><span class="sxs-lookup"><span data-stu-id="0a187-119">A register consists of properties that determine how each register behaves.</span></span>



| <span data-ttu-id="0a187-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0a187-120">Property</span></span>        | <span data-ttu-id="0a187-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="0a187-121">Description</span></span> |
|-----------------|-------------|
| <span data-ttu-id="0a187-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="0a187-122">Name</span></span>            | <span data-ttu-id="0a187-123">oPos</span><span class="sxs-lookup"><span data-stu-id="0a187-123">oPos</span></span>        |
| <span data-ttu-id="0a187-124">Count</span><span class="sxs-lookup"><span data-stu-id="0a187-124">Count</span></span>           | <span data-ttu-id="0a187-125">1 Vector</span><span class="sxs-lookup"><span data-stu-id="0a187-125">1 vector</span></span>    |
| <span data-ttu-id="0a187-126">Permisos de e/s</span><span class="sxs-lookup"><span data-stu-id="0a187-126">I/O permissions</span></span> | <span data-ttu-id="0a187-127">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="0a187-127">Write-only.</span></span> |



 

<span data-ttu-id="0a187-128">El valor es la posición en el espacio de recorte homogéneo.</span><span class="sxs-lookup"><span data-stu-id="0a187-128">The value is the position in homogeneous clipping space.</span></span> <span data-ttu-id="0a187-129">Este valor debe escribirse en el sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="0a187-129">This value must be written by the vertex shader.</span></span>

<span data-ttu-id="0a187-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0a187-130">Example</span></span>


```
    dcl_position v0
    
    def c40, 0.0f,0.0f,0.0f,0.0f;
    // transform into projection space
    m4x4 r0,v0,c8
    max r0.z,c40.z,r0.z //clamp to 0
    max r0.w,c12.x,r0.w //clamp to near clip plane
    mov oPos,r0   
```



## <a name="related-topics"></a><span data-ttu-id="0a187-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0a187-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a187-132">Registros del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="0a187-132">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




