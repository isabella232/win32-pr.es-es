---
title: CRS-PS
description: Calcula un producto cruzado mediante la regla de la derecha. | CRS-PS
ms.assetid: 602fa7cc-4e2b-4d90-90d8-df00d5812c81
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b6098c8bf01bf0d8cce886276c1d1081720ea667
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362112"
---
# <a name="crs---ps"></a><span data-ttu-id="cbd19-104">CRS-PS</span><span class="sxs-lookup"><span data-stu-id="cbd19-104">crs - ps</span></span>

<span data-ttu-id="cbd19-105">Calcula un producto cruzado mediante la regla de la derecha.</span><span class="sxs-lookup"><span data-stu-id="cbd19-105">Computes a cross product using the right-hand rule.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbd19-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cbd19-106">Syntax</span></span>



| <span data-ttu-id="cbd19-107">CRS DST, src0, SRC1</span><span class="sxs-lookup"><span data-stu-id="cbd19-107">crs dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="cbd19-108">, donde</span><span class="sxs-lookup"><span data-stu-id="cbd19-108">where</span></span>

-   <span data-ttu-id="cbd19-109">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="cbd19-109">dst is the destination register.</span></span>
-   <span data-ttu-id="cbd19-110">src0 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="cbd19-110">src0 is a source register.</span></span>
-   <span data-ttu-id="cbd19-111">SRC1 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="cbd19-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbd19-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cbd19-112">Remarks</span></span>



| <span data-ttu-id="cbd19-113">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="cbd19-113">Pixel shader versions</span></span> | <span data-ttu-id="cbd19-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="cbd19-114">1\_1</span></span> | <span data-ttu-id="cbd19-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="cbd19-115">1\_2</span></span> | <span data-ttu-id="cbd19-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="cbd19-116">1\_3</span></span> | <span data-ttu-id="cbd19-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="cbd19-117">1\_4</span></span> | <span data-ttu-id="cbd19-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cbd19-118">2\_0</span></span> | <span data-ttu-id="cbd19-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="cbd19-119">2\_x</span></span> | <span data-ttu-id="cbd19-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="cbd19-120">2\_sw</span></span> | <span data-ttu-id="cbd19-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cbd19-121">3\_0</span></span> | <span data-ttu-id="cbd19-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="cbd19-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="cbd19-123">CRS</span><span class="sxs-lookup"><span data-stu-id="cbd19-123">crs</span></span>                   |      |      |      |      | <span data-ttu-id="cbd19-124">x</span><span class="sxs-lookup"><span data-stu-id="cbd19-124">x</span></span>    | <span data-ttu-id="cbd19-125">x</span><span class="sxs-lookup"><span data-stu-id="cbd19-125">x</span></span>    | <span data-ttu-id="cbd19-126">x</span><span class="sxs-lookup"><span data-stu-id="cbd19-126">x</span></span>     | <span data-ttu-id="cbd19-127">x</span><span class="sxs-lookup"><span data-stu-id="cbd19-127">x</span></span>    | <span data-ttu-id="cbd19-128">x</span><span class="sxs-lookup"><span data-stu-id="cbd19-128">x</span></span>     |



 

<span data-ttu-id="cbd19-129">Esta instrucción funciona como se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="cbd19-129">This instruction works as shown here.</span></span>


```
dest.x = src0.y * src1.z - src0.z * src1.y;
dest.y = src0.z * src1.x - src0.x * src1.z;
dest.z = src0.x * src1.y - src0.y * src1.x;
```



<span data-ttu-id="cbd19-130">Algunas restricciones en el uso:</span><span class="sxs-lookup"><span data-stu-id="cbd19-130">Some restrictions on use:</span></span>

-   <span data-ttu-id="cbd19-131">src0 no puede ser el mismo registro que dest.</span><span class="sxs-lookup"><span data-stu-id="cbd19-131">src0 cannot be the same register as dest.</span></span>
-   <span data-ttu-id="cbd19-132">SRC1 no puede ser el mismo registro que dest.</span><span class="sxs-lookup"><span data-stu-id="cbd19-132">src1 cannot be the same register as dest.</span></span>
-   <span data-ttu-id="cbd19-133">src0 no puede tener ningún swizzle que no sea el swizzle predeterminado (. xyzw).</span><span class="sxs-lookup"><span data-stu-id="cbd19-133">src0 cannot have any swizzle other than the default swizzle (.xyzw).</span></span>
-   <span data-ttu-id="cbd19-134">SRC1 no puede tener ningún swizzle que no sea el swizzle predeterminado (. xyzw).</span><span class="sxs-lookup"><span data-stu-id="cbd19-134">src1 cannot have any swizzle other than the default swizzle (.xyzw).</span></span>
-   <span data-ttu-id="cbd19-135">dest debe tener exactamente una de las siete máscaras siguientes:. x \| . y \| . z \| . XY \| . XZ. \| YZ. \| XYZ.</span><span class="sxs-lookup"><span data-stu-id="cbd19-135">dest has to have exactly one of the following seven masks: .x \| .y \| .z \| .xy \| .xz \| .yz \| .xyz.</span></span>
-   <span data-ttu-id="cbd19-136">dest debe ser un registro temporal.</span><span class="sxs-lookup"><span data-stu-id="cbd19-136">dest must be a temporary register.</span></span>
-   <span data-ttu-id="cbd19-137">dest no debe ser el mismo registro que src0 o SRC1</span><span class="sxs-lookup"><span data-stu-id="cbd19-137">dest must not be the same register as src0 or src1</span></span>

## <a name="related-topics"></a><span data-ttu-id="cbd19-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cbd19-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbd19-139">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="cbd19-139">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




