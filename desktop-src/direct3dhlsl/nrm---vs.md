---
title: NRM-vs
description: Normalizar un vector 3D. | NRM-vs
ms.assetid: 735e9971-c0c3-4648-8362-58bda6fac46a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0e696277136826294392149c4b7430e4c75f9d9a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104280062"
---
# <a name="nrm---vs"></a><span data-ttu-id="ea332-104">NRM-vs</span><span class="sxs-lookup"><span data-stu-id="ea332-104">nrm - vs</span></span>

<span data-ttu-id="ea332-105">Normalizar un vector 3D.</span><span class="sxs-lookup"><span data-stu-id="ea332-105">Normalize a 3D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea332-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ea332-106">Syntax</span></span>



| <span data-ttu-id="ea332-107">NRM DST, src</span><span class="sxs-lookup"><span data-stu-id="ea332-107">nrm dst, src</span></span> |
|--------------|



 

<span data-ttu-id="ea332-108">, donde</span><span class="sxs-lookup"><span data-stu-id="ea332-108">where</span></span>

-   <span data-ttu-id="ea332-109">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="ea332-109">dst is the destination register.</span></span>
-   <span data-ttu-id="ea332-110">src es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="ea332-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea332-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ea332-111">Remarks</span></span>



| <span data-ttu-id="ea332-112">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="ea332-112">Vertex shader versions</span></span> | <span data-ttu-id="ea332-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="ea332-113">1\_1</span></span> | <span data-ttu-id="ea332-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ea332-114">2\_0</span></span> | <span data-ttu-id="ea332-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="ea332-115">2\_x</span></span> | <span data-ttu-id="ea332-116">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="ea332-116">2\_sw</span></span> | <span data-ttu-id="ea332-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ea332-117">3\_0</span></span> | <span data-ttu-id="ea332-118">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="ea332-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="ea332-119">nrm</span><span class="sxs-lookup"><span data-stu-id="ea332-119">nrm</span></span>                    |      | <span data-ttu-id="ea332-120">x</span><span class="sxs-lookup"><span data-stu-id="ea332-120">x</span></span>    | <span data-ttu-id="ea332-121">x</span><span class="sxs-lookup"><span data-stu-id="ea332-121">x</span></span>    | <span data-ttu-id="ea332-122">x</span><span class="sxs-lookup"><span data-stu-id="ea332-122">x</span></span>     | <span data-ttu-id="ea332-123">x</span><span class="sxs-lookup"><span data-stu-id="ea332-123">x</span></span>    | <span data-ttu-id="ea332-124">x</span><span class="sxs-lookup"><span data-stu-id="ea332-124">x</span></span>     |



 

<span data-ttu-id="ea332-125">Esta instrucción funciona conceptualmente tal y como se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="ea332-125">This instruction works conceptually as shown here.</span></span>

<span data-ttu-id="ea332-126">squareRootOfTheSum = (src0. x \* src0. x + src0. y \* src0. y + src0. z \* src0. z)<sup>1/2</sup>;</span><span class="sxs-lookup"><span data-stu-id="ea332-126">squareRootOfTheSum = (src0.x\*src0.x + src0.y\*src0.y + src0.z\*src0.z)<sup>1/2</sup>;</span></span>


```
dest.x = src0.x * (1 / squareRootOfTheSum);
dest.y = src0.y * (1 / squareRootOfTheSum);
dest.z = src0.z * (1 / squareRootOfTheSum);
dest.w = src0.w * (1 / squareRootOfTheSum);
```



<span data-ttu-id="ea332-127">Los registros dest y src no pueden ser iguales.</span><span class="sxs-lookup"><span data-stu-id="ea332-127">The dest and src registers cannot be the same.</span></span> <span data-ttu-id="ea332-128">El registro de destino debe ser un registro temporal.</span><span class="sxs-lookup"><span data-stu-id="ea332-128">The dest register must be a temporary register.</span></span>

<span data-ttu-id="ea332-129">Esta instrucción realiza la interpolación lineal basada en la fórmula siguiente.</span><span class="sxs-lookup"><span data-stu-id="ea332-129">This instruction performs the linear interpolation based on the following formula.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="ea332-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ea332-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea332-131">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="ea332-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




