---
title: NRM-PS
description: Normalizar un vector 3D. | NRM-PS
ms.assetid: 4881037d-3ad1-4afb-b4ad-d615c6b8fe34
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 165f1b8fa6adce4ffba079eff025ed1a3d8ce61e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362171"
---
# <a name="nrm---ps"></a><span data-ttu-id="9bf34-104">NRM-PS</span><span class="sxs-lookup"><span data-stu-id="9bf34-104">nrm - ps</span></span>

<span data-ttu-id="9bf34-105">Normalizar un vector 3D.</span><span class="sxs-lookup"><span data-stu-id="9bf34-105">Normalize a 3D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bf34-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9bf34-106">Syntax</span></span>



| <span data-ttu-id="9bf34-107">NRM DST, src</span><span class="sxs-lookup"><span data-stu-id="9bf34-107">nrm dst, src</span></span> |
|--------------|



 

<span data-ttu-id="9bf34-108">, donde</span><span class="sxs-lookup"><span data-stu-id="9bf34-108">where</span></span>

-   <span data-ttu-id="9bf34-109">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="9bf34-109">dst is the destination register.</span></span>
-   <span data-ttu-id="9bf34-110">src es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="9bf34-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="9bf34-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9bf34-111">Remarks</span></span>



| <span data-ttu-id="9bf34-112">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="9bf34-112">Pixel shader versions</span></span> | <span data-ttu-id="9bf34-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="9bf34-113">1\_1</span></span> | <span data-ttu-id="9bf34-114">1\_2</span><span class="sxs-lookup"><span data-stu-id="9bf34-114">1\_2</span></span> | <span data-ttu-id="9bf34-115">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="9bf34-115">1\_3</span></span> | <span data-ttu-id="9bf34-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="9bf34-116">1\_4</span></span> | <span data-ttu-id="9bf34-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9bf34-117">2\_0</span></span> | <span data-ttu-id="9bf34-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="9bf34-118">2\_x</span></span> | <span data-ttu-id="9bf34-119">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="9bf34-119">2\_sw</span></span> | <span data-ttu-id="9bf34-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9bf34-120">3\_0</span></span> | <span data-ttu-id="9bf34-121">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="9bf34-121">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="9bf34-122">nrm</span><span class="sxs-lookup"><span data-stu-id="9bf34-122">nrm</span></span>                   |      |      |      |      | <span data-ttu-id="9bf34-123">x</span><span class="sxs-lookup"><span data-stu-id="9bf34-123">x</span></span>    | <span data-ttu-id="9bf34-124">x</span><span class="sxs-lookup"><span data-stu-id="9bf34-124">x</span></span>    | <span data-ttu-id="9bf34-125">x</span><span class="sxs-lookup"><span data-stu-id="9bf34-125">x</span></span>     | <span data-ttu-id="9bf34-126">x</span><span class="sxs-lookup"><span data-stu-id="9bf34-126">x</span></span>    | <span data-ttu-id="9bf34-127">x</span><span class="sxs-lookup"><span data-stu-id="9bf34-127">x</span></span>     |



 

<span data-ttu-id="9bf34-128">Esta instrucción funciona conceptualmente tal y como se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="9bf34-128">This instruction works conceptually as shown here.</span></span>

<span data-ttu-id="9bf34-129">squareRootOfTheSum = (src0. x \* src0. x + src0. y \* src0. y + src0. z \* src0. z)<sup>1/2</sup>;</span><span class="sxs-lookup"><span data-stu-id="9bf34-129">squareRootOfTheSum = (src0.x\*src0.x + src0.y\*src0.y + src0.z\*src0.z)<sup>1/2</sup>;</span></span>


```
dest.x = src0.x * (1 / squareRootOfTheSum);
dest.y = src0.y * (1 / squareRootOfTheSum);
dest.z = src0.z * (1 / squareRootOfTheSum);
dest.w = src0.w * (1 / squareRootOfTheSum);
```



<span data-ttu-id="9bf34-130">Los registros dest y src no pueden ser iguales.</span><span class="sxs-lookup"><span data-stu-id="9bf34-130">The dest and src registers cannot be the same.</span></span> <span data-ttu-id="9bf34-131">El registro de destino debe ser un registro temporal.</span><span class="sxs-lookup"><span data-stu-id="9bf34-131">The dest register must be a temporary register.</span></span>

<span data-ttu-id="9bf34-132">Esta instrucción realiza la interpolación lineal basada en la fórmula siguiente.</span><span class="sxs-lookup"><span data-stu-id="9bf34-132">This instruction performs the linear interpolation based on the following formula.</span></span>


```
float f = src0.x*src0.x + src0.y*src0.y + src0.z*src0.z;
if (f != 0)
    f = (float)(1/sqrt(f));
else
    f = FLT_MAX;

dest.x = src0.x*f;
dest.y = src0.y*f;
dest.z = src0.z*f;
dest.w = src0.w*f;
```



## <a name="related-topics"></a><span data-ttu-id="9bf34-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9bf34-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9bf34-134">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="9bf34-134">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




