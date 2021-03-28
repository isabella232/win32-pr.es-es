---
title: Mostrar
description: Devuelve un vector de reflexión mediante un rayo de incidente y una superficie normal.
ms.assetid: e321b399-f382-4585-83a6-a7da1f7b2327
keywords:
- reflejar HLSL
topic_type:
- apiref
api_name:
- reflect
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 46c981f636a797ecc4e0dd341ce44ed886c202cb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793594"
---
# <a name="reflect"></a><span data-ttu-id="10261-104">Mostrar</span><span class="sxs-lookup"><span data-stu-id="10261-104">reflect</span></span>

<span data-ttu-id="10261-105">Devuelve un vector de reflexión mediante un rayo de incidente y una superficie normal.</span><span class="sxs-lookup"><span data-stu-id="10261-105">Returns a reflection vector using an incident ray and a surface normal.</span></span>



| <span data-ttu-id="10261-106">refleje *RET* (*i*, *n*)</span><span class="sxs-lookup"><span data-stu-id="10261-106">*ret* reflect(*i*, *n*)</span></span> |
|-------------------------|



 

## <a name="parameters"></a><span data-ttu-id="10261-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="10261-107">Parameters</span></span>



| <span data-ttu-id="10261-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="10261-108">Item</span></span>                                                   | <span data-ttu-id="10261-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="10261-109">Description</span></span>                                          |
|--------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="10261-110"><span id="i"></span><span id="I"></span>*Configur*</span><span class="sxs-lookup"><span data-stu-id="10261-110"><span id="i"></span><span id="I"></span>*i*</span></span><br/> | <span data-ttu-id="10261-111">\[en \] un vector de incidente de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="10261-111">\[in\] A floating-point, incident vector.</span></span><br/> |
| <span data-ttu-id="10261-112"><span id="n"></span><span id="N"></span>*n*</span><span class="sxs-lookup"><span data-stu-id="10261-112"><span id="n"></span><span id="N"></span>*n*</span></span><br/> | <span data-ttu-id="10261-113">\[en \] un vector normal de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="10261-113">\[in\] A floating-point, normal vector.</span></span><br/>   |



 

## <a name="return-value"></a><span data-ttu-id="10261-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="10261-114">Return Value</span></span>

<span data-ttu-id="10261-115">Un vector de reflexión de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="10261-115">A floating-point, reflection vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="10261-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="10261-116">Remarks</span></span>

<span data-ttu-id="10261-117">Esta función calcula el vector de reflexión mediante la siguiente fórmula: v = i-2 \* n \* punto (i n).</span><span class="sxs-lookup"><span data-stu-id="10261-117">This function calculates the reflection vector using the following formula: v = i - 2 \* n \* dot(i n) .</span></span>

## <a name="type-description"></a><span data-ttu-id="10261-118">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="10261-118">Type Description</span></span>



| <span data-ttu-id="10261-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="10261-119">Name</span></span>  | [<span data-ttu-id="10261-120">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="10261-120">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="10261-121">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="10261-121">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="10261-122">Tamaño</span><span class="sxs-lookup"><span data-stu-id="10261-122">Size</span></span>                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="10261-123">*i*</span><span class="sxs-lookup"><span data-stu-id="10261-123">*i*</span></span>   | [<span data-ttu-id="10261-124">**medios**</span><span class="sxs-lookup"><span data-stu-id="10261-124">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="10261-125">**flot**</span><span class="sxs-lookup"><span data-stu-id="10261-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="10261-126">cualquiera</span><span class="sxs-lookup"><span data-stu-id="10261-126">any</span></span>                            |
| <span data-ttu-id="10261-127">*n*</span><span class="sxs-lookup"><span data-stu-id="10261-127">*n*</span></span>   | [<span data-ttu-id="10261-128">**medios**</span><span class="sxs-lookup"><span data-stu-id="10261-128">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="10261-129">**flot**</span><span class="sxs-lookup"><span data-stu-id="10261-129">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="10261-130">mismas dimensiones que la entrada *i*</span><span class="sxs-lookup"><span data-stu-id="10261-130">same dimension(s) as input *i*</span></span> |
| <span data-ttu-id="10261-131">*direcc*</span><span class="sxs-lookup"><span data-stu-id="10261-131">*ret*</span></span> | [<span data-ttu-id="10261-132">**medios**</span><span class="sxs-lookup"><span data-stu-id="10261-132">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="10261-133">**flot**</span><span class="sxs-lookup"><span data-stu-id="10261-133">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="10261-134">mismas dimensiones que la entrada *i*</span><span class="sxs-lookup"><span data-stu-id="10261-134">same dimension(s) as input *i*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="10261-135">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="10261-135">Minimum Shader Model</span></span>

<span data-ttu-id="10261-136">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="10261-136">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="10261-137">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="10261-137">Shader Model</span></span>                                                                       | <span data-ttu-id="10261-138">Compatible</span><span class="sxs-lookup"><span data-stu-id="10261-138">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="10261-139">Modelador [modelo 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="10261-139">[Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) and higher shader models</span></span> | <span data-ttu-id="10261-140">sí</span><span class="sxs-lookup"><span data-stu-id="10261-140">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="10261-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="10261-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10261-142">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="10261-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

