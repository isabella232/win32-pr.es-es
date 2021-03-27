---
title: cruzadas
description: Devuelve el producto cruzado de dos vectores 3D de punto flotante.
ms.assetid: 5f1832af-6bc5-49a7-956a-fd762f674f5f
keywords:
- HLSL cruzado
topic_type:
- apiref
api_name:
- cross
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 91959bf415c3e56edf370942de268523bf998743
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997157"
---
# <a name="cross"></a><span data-ttu-id="db8fa-104">cruzadas</span><span class="sxs-lookup"><span data-stu-id="db8fa-104">cross</span></span>

<span data-ttu-id="db8fa-105">Devuelve el producto cruzado de dos vectores 3D de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="db8fa-105">Returns the cross product of two floating-point, 3D vectors.</span></span>



| <span data-ttu-id="db8fa-106">*RET* cruzada (*x*, *y*)</span><span class="sxs-lookup"><span data-stu-id="db8fa-106">*ret* cross(*x*, *y*)</span></span> |
|-----------------------|



 

## <a name="parameters"></a><span data-ttu-id="db8fa-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="db8fa-107">Parameters</span></span>



| <span data-ttu-id="db8fa-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="db8fa-108">Item</span></span>                                                   | <span data-ttu-id="db8fa-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="db8fa-109">Description</span></span>                                             |
|--------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="db8fa-110"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="db8fa-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="db8fa-111">\[en \] el primer punto flotante, Vector 3D.</span><span class="sxs-lookup"><span data-stu-id="db8fa-111">\[in\] The first floating-point, 3D vector.</span></span><br/>  |
| <span data-ttu-id="db8fa-112"><span id="y"></span><span id="Y"></span>*sí*</span><span class="sxs-lookup"><span data-stu-id="db8fa-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="db8fa-113">\[en \] el segundo punto flotante, Vector 3D.</span><span class="sxs-lookup"><span data-stu-id="db8fa-113">\[in\] The second floating-point, 3D vector.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="db8fa-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="db8fa-114">Return Value</span></span>

<span data-ttu-id="db8fa-115">El producto cruzado del parámetro *x* y el parámetro *y* .</span><span class="sxs-lookup"><span data-stu-id="db8fa-115">The cross product of the *x* parameter and the *y* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="db8fa-116">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="db8fa-116">Type Description</span></span>



| <span data-ttu-id="db8fa-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="db8fa-117">Name</span></span>  | [<span data-ttu-id="db8fa-118">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="db8fa-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="db8fa-119">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="db8fa-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="db8fa-120">Tamaño</span><span class="sxs-lookup"><span data-stu-id="db8fa-120">Size</span></span> |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="db8fa-121">*x*</span><span class="sxs-lookup"><span data-stu-id="db8fa-121">*x*</span></span>   | [<span data-ttu-id="db8fa-122">**medios**</span><span class="sxs-lookup"><span data-stu-id="db8fa-122">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="db8fa-123">**flot**</span><span class="sxs-lookup"><span data-stu-id="db8fa-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="db8fa-124">3</span><span class="sxs-lookup"><span data-stu-id="db8fa-124">3</span></span>    |
| <span data-ttu-id="db8fa-125">*y*</span><span class="sxs-lookup"><span data-stu-id="db8fa-125">*y*</span></span>   | [<span data-ttu-id="db8fa-126">**medios**</span><span class="sxs-lookup"><span data-stu-id="db8fa-126">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="db8fa-127">**flot**</span><span class="sxs-lookup"><span data-stu-id="db8fa-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="db8fa-128">3</span><span class="sxs-lookup"><span data-stu-id="db8fa-128">3</span></span>    |
| <span data-ttu-id="db8fa-129">*direcc*</span><span class="sxs-lookup"><span data-stu-id="db8fa-129">*ret*</span></span> | [<span data-ttu-id="db8fa-130">**medios**</span><span class="sxs-lookup"><span data-stu-id="db8fa-130">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="db8fa-131">**flot**</span><span class="sxs-lookup"><span data-stu-id="db8fa-131">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="db8fa-132">3</span><span class="sxs-lookup"><span data-stu-id="db8fa-132">3</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="db8fa-133">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="db8fa-133">Minimum Shader Model</span></span>

<span data-ttu-id="db8fa-134">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="db8fa-134">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="db8fa-135">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="db8fa-135">Shader Model</span></span>                                                                       | <span data-ttu-id="db8fa-136">Compatible</span><span class="sxs-lookup"><span data-stu-id="db8fa-136">Supported</span></span>             |
|------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="db8fa-137">Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="db8fa-137">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="db8fa-138">sí</span><span class="sxs-lookup"><span data-stu-id="db8fa-138">yes</span></span>                   |
| [<span data-ttu-id="db8fa-139">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="db8fa-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="db8fa-140">vs \_ 1 \_ 1 y PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="db8fa-140">vs\_1\_1 and ps\_1\_4</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="db8fa-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="db8fa-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db8fa-142">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="db8fa-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

