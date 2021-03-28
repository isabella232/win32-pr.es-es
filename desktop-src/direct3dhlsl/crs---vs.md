---
title: CRS-vs
description: Calcula un producto cruzado mediante la regla de la derecha. | CRS-vs
ms.assetid: 102108f5-acc8-49ce-a84b-b8060decbaa7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fee30fab91b4f491efd4311919245ec2cb98b555
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362111"
---
# <a name="crs---vs"></a><span data-ttu-id="a22df-104">CRS-vs</span><span class="sxs-lookup"><span data-stu-id="a22df-104">crs - vs</span></span>

<span data-ttu-id="a22df-105">Calcula un producto cruzado mediante la regla de la derecha.</span><span class="sxs-lookup"><span data-stu-id="a22df-105">Computes a cross product using the right-hand rule.</span></span>

## <a name="syntax"></a><span data-ttu-id="a22df-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a22df-106">Syntax</span></span>



| <span data-ttu-id="a22df-107">CRS DST, src0, SRC1</span><span class="sxs-lookup"><span data-stu-id="a22df-107">crs dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="a22df-108">, donde</span><span class="sxs-lookup"><span data-stu-id="a22df-108">where</span></span>

-   <span data-ttu-id="a22df-109">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="a22df-109">dst is the destination register.</span></span>
-   <span data-ttu-id="a22df-110">src0 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="a22df-110">src0 is a source register.</span></span>
-   <span data-ttu-id="a22df-111">SRC1 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="a22df-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="a22df-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a22df-112">Remarks</span></span>



| <span data-ttu-id="a22df-113">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="a22df-113">Vertex shader versions</span></span> | <span data-ttu-id="a22df-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="a22df-114">1\_1</span></span> | <span data-ttu-id="a22df-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a22df-115">2\_0</span></span> | <span data-ttu-id="a22df-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="a22df-116">2\_x</span></span> | <span data-ttu-id="a22df-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a22df-117">2\_sw</span></span> | <span data-ttu-id="a22df-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a22df-118">3\_0</span></span> | <span data-ttu-id="a22df-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a22df-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="a22df-120">CRS</span><span class="sxs-lookup"><span data-stu-id="a22df-120">crs</span></span>                    |      | <span data-ttu-id="a22df-121">x</span><span class="sxs-lookup"><span data-stu-id="a22df-121">x</span></span>    | <span data-ttu-id="a22df-122">x</span><span class="sxs-lookup"><span data-stu-id="a22df-122">x</span></span>    | <span data-ttu-id="a22df-123">x</span><span class="sxs-lookup"><span data-stu-id="a22df-123">x</span></span>     | <span data-ttu-id="a22df-124">x</span><span class="sxs-lookup"><span data-stu-id="a22df-124">x</span></span>    | <span data-ttu-id="a22df-125">x</span><span class="sxs-lookup"><span data-stu-id="a22df-125">x</span></span>     |



 

<span data-ttu-id="a22df-126">Esta instrucción funciona como se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="a22df-126">This instruction works as shown here.</span></span>


```
dest.x = src0.y * src1.z - src0.z * src1.y;
dest.y = src0.z * src1.x - src0.x * src1.z;
dest.z = src0.x * src1.y - src0.y * src1.x;
```



<span data-ttu-id="a22df-127">Algunas restricciones en el uso:</span><span class="sxs-lookup"><span data-stu-id="a22df-127">Some restrictions on use:</span></span>

-   <span data-ttu-id="a22df-128">src0 no puede ser el mismo registro que dest.</span><span class="sxs-lookup"><span data-stu-id="a22df-128">src0 cannot be the same register as dest.</span></span>
-   <span data-ttu-id="a22df-129">SRC1 no puede ser el mismo registro que dest.</span><span class="sxs-lookup"><span data-stu-id="a22df-129">src1 cannot be the same register as dest.</span></span>
-   <span data-ttu-id="a22df-130">src0 no puede tener ningún swizzle que no sea el swizzle predeterminado (. xyzw).</span><span class="sxs-lookup"><span data-stu-id="a22df-130">src0 cannot have any swizzle other than the default swizzle (.xyzw).</span></span>
-   <span data-ttu-id="a22df-131">SRC1 no puede tener ningún swizzle que no sea el swizzle predeterminado (. xyzw).</span><span class="sxs-lookup"><span data-stu-id="a22df-131">src1 cannot have any swizzle other than the default swizzle (.xyzw).</span></span>
-   <span data-ttu-id="a22df-132">dest debe tener exactamente una de las siete máscaras siguientes:. x \| . y \| . z \| . XY \| . XZ. \| YZ. \| XYZ.</span><span class="sxs-lookup"><span data-stu-id="a22df-132">dest has to have exactly one of the following seven masks: .x \| .y \| .z \| .xy \| .xz \| .yz \| .xyz.</span></span>
-   <span data-ttu-id="a22df-133">dest debe ser un registro temporal.</span><span class="sxs-lookup"><span data-stu-id="a22df-133">dest must be a temporary register.</span></span>
-   <span data-ttu-id="a22df-134">dest no debe ser el mismo registro que src0 o SRC1</span><span class="sxs-lookup"><span data-stu-id="a22df-134">dest must not be the same register as src0 or src1</span></span>

## <a name="related-topics"></a><span data-ttu-id="a22df-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a22df-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a22df-136">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="a22df-136">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




