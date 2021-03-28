---
title: dcl_resource RAW (SM5-ASM)
description: Declare una entrada de recurso de sombreador y asígnela a un registro de marcador de posición t \-a para el recurso. | dcl_resource RAW (SM5-ASM)
ms.assetid: ECBA9DAB-F217-47FB-9588-F35866004E72
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dd6ccc5990e34990772a072086d9e080cde67b4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104280050"
---
# <a name="dcl_resource-raw-sm5---asm"></a><span data-ttu-id="3b221-104">\_recurso de DCL sin formato (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="3b221-104">dcl\_resource raw (sm5 - asm)</span></span>

<span data-ttu-id="3b221-105">Declare una entrada de recurso de sombreador y asígnela a un \# registro de marcador de posición t-a para el recurso.</span><span class="sxs-lookup"><span data-stu-id="3b221-105">Declare a shader resource input and assign it to a t\# - a placeholder register for the resource.</span></span>



| <span data-ttu-id="3b221-106">\_ \_ dstSRV sin formato de recursos de DCL</span><span class="sxs-lookup"><span data-stu-id="3b221-106">dcl\_resource\_raw dstSRV</span></span> |
|---------------------------|



 



| <span data-ttu-id="3b221-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="3b221-107">Item</span></span>                                                                                           | <span data-ttu-id="3b221-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="3b221-108">Description</span></span>                                                                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b221-109"><span id="dstSRV"></span><span id="dstsrv"></span><span id="DSTSRV"></span>*dstSRV*</span><span class="sxs-lookup"><span data-stu-id="3b221-109"><span id="dstSRV"></span><span id="dstsrv"></span><span id="DSTSRV"></span>*dstSRV*</span></span><br/> | <span data-ttu-id="3b221-110">\[en \] un \# registro t declarado como una referencia a un ShaderResourceView de un búfer sin formato.</span><span class="sxs-lookup"><span data-stu-id="3b221-110">\[in\] A t\# register declared as a reference to a ShaderResourceView of a raw buffer.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3b221-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3b221-111">Remarks</span></span>

<span data-ttu-id="3b221-112">El contenido de la estructura no tiene ningún tipo; las operaciones realizadas en la memoria pueden interpretar implícitamente los datos como si tuvieran un tipo.</span><span class="sxs-lookup"><span data-stu-id="3b221-112">The contents of the structure have no type; operations performed on the memory may implicitly interpret the data as having a type.</span></span>

<span data-ttu-id="3b221-113">Las instrucciones que hacen referencia a una t sin formato \# toman una dirección 1D, un valor de bit 32 sin signo que especifica el desplazamiento de bytes a una ubicación alineada de 32 bits en el búfer.</span><span class="sxs-lookup"><span data-stu-id="3b221-113">Instructions that reference a raw t\# take a 1D address, an unsigned 32-bit value specifying the byte offset to a 32-bit aligned location in the Buffer.</span></span> <span data-ttu-id="3b221-114">La dirección debe ser un múltiplo de 4 (bytes).</span><span class="sxs-lookup"><span data-stu-id="3b221-114">The address must be a multiple of 4 (bytes).</span></span>

<span data-ttu-id="3b221-115">Las vistas enlazadas a t \# declaradas como RAW deben tener los sin procesar especificados en su creación; de lo contrario, el comportamiento cuando se tiene acceso desde un sombreador no está definido.</span><span class="sxs-lookup"><span data-stu-id="3b221-115">Views bound to t\# declared as raw must have RAW specified on their creation; otherwise behavior when accessed from a shader is undefined.</span></span>

<span data-ttu-id="3b221-116">CS \_ 4 \_ 0 y CS \_ 4 \_ 1 admiten esta instrucción.</span><span class="sxs-lookup"><span data-stu-id="3b221-116">cs\_4\_0 and cs\_4\_1 support this instruction.</span></span>

<span data-ttu-id="3b221-117">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="3b221-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="3b221-118">Vértice</span><span class="sxs-lookup"><span data-stu-id="3b221-118">Vertex</span></span> | <span data-ttu-id="3b221-119">Casco</span><span class="sxs-lookup"><span data-stu-id="3b221-119">Hull</span></span> | <span data-ttu-id="3b221-120">Dominio</span><span class="sxs-lookup"><span data-stu-id="3b221-120">Domain</span></span> | <span data-ttu-id="3b221-121">Geometría</span><span class="sxs-lookup"><span data-stu-id="3b221-121">Geometry</span></span> | <span data-ttu-id="3b221-122">Píxel</span><span class="sxs-lookup"><span data-stu-id="3b221-122">Pixel</span></span> | <span data-ttu-id="3b221-123">Compute</span><span class="sxs-lookup"><span data-stu-id="3b221-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="3b221-124">X</span><span class="sxs-lookup"><span data-stu-id="3b221-124">X</span></span>      | <span data-ttu-id="3b221-125">X</span><span class="sxs-lookup"><span data-stu-id="3b221-125">X</span></span>    | <span data-ttu-id="3b221-126">X</span><span class="sxs-lookup"><span data-stu-id="3b221-126">X</span></span>      | <span data-ttu-id="3b221-127">X</span><span class="sxs-lookup"><span data-stu-id="3b221-127">X</span></span>        | <span data-ttu-id="3b221-128">X</span><span class="sxs-lookup"><span data-stu-id="3b221-128">X</span></span>     | <span data-ttu-id="3b221-129">X</span><span class="sxs-lookup"><span data-stu-id="3b221-129">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="3b221-130">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="3b221-130">Minimum Shader Model</span></span>

<span data-ttu-id="3b221-131">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="3b221-131">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="3b221-132">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="3b221-132">Shader Model</span></span>                                              | <span data-ttu-id="3b221-133">Compatible</span><span class="sxs-lookup"><span data-stu-id="3b221-133">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="3b221-134">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="3b221-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="3b221-135">sí</span><span class="sxs-lookup"><span data-stu-id="3b221-135">yes</span></span>       |
| [<span data-ttu-id="3b221-136">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="3b221-136">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="3b221-137">no</span><span class="sxs-lookup"><span data-stu-id="3b221-137">no</span></span>        |
| [<span data-ttu-id="3b221-138">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="3b221-138">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="3b221-139">no</span><span class="sxs-lookup"><span data-stu-id="3b221-139">no</span></span>        |
| [<span data-ttu-id="3b221-140">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3b221-140">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="3b221-141">no</span><span class="sxs-lookup"><span data-stu-id="3b221-141">no</span></span>        |
| [<span data-ttu-id="3b221-142">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3b221-142">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="3b221-143">no</span><span class="sxs-lookup"><span data-stu-id="3b221-143">no</span></span>        |
| [<span data-ttu-id="3b221-144">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3b221-144">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="3b221-145">no</span><span class="sxs-lookup"><span data-stu-id="3b221-145">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="3b221-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3b221-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b221-147">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3b221-147">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





