---
title: isinf ((Corecrt, \_ Math. h)
description: Determina si el valor especificado es infinito.
ms.assetid: 2028dc5a-e48b-4081-a0ec-35901113aab6
keywords:
- HLSL de isinf (
topic_type:
- apiref
api_name:
- isinf
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4df738438d62d5a66dd3b08ad769d475df562d5f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280388"
---
# <a name="isinf"></a><span data-ttu-id="26388-104">isinf</span><span class="sxs-lookup"><span data-stu-id="26388-104">isinf</span></span>

<span data-ttu-id="26388-105">Determina si el valor especificado es infinito.</span><span class="sxs-lookup"><span data-stu-id="26388-105">Determines if the specified value is infinite.</span></span>



| <span data-ttu-id="26388-106">*RET* isinf ((*x*)</span><span class="sxs-lookup"><span data-stu-id="26388-106">*ret* isinf(*x*)</span></span> |
|------------------|



 

## <a name="parameters"></a><span data-ttu-id="26388-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="26388-107">Parameters</span></span>



| <span data-ttu-id="26388-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="26388-108">Item</span></span>                                                   | <span data-ttu-id="26388-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="26388-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="26388-110"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="26388-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="26388-111">\[en \] el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="26388-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="26388-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="26388-112">Return Value</span></span>

<span data-ttu-id="26388-113">Devuelve un valor del mismo tamaño que la entrada, con un valor establecido en **true** si el parámetro *x* es + inf o-INF.</span><span class="sxs-lookup"><span data-stu-id="26388-113">Returns a value of the same size as the input, with a value set to **True** if the *x* parameter is +INF or -INF.</span></span> <span data-ttu-id="26388-114">En caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="26388-114">Otherwise, **False**.</span></span>

## <a name="type-description"></a><span data-ttu-id="26388-115">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="26388-115">Type Description</span></span>



| <span data-ttu-id="26388-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="26388-116">Name</span></span>  | [<span data-ttu-id="26388-117">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="26388-117">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="26388-118">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="26388-118">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="26388-119">Tamaño</span><span class="sxs-lookup"><span data-stu-id="26388-119">Size</span></span>     |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|----------|
| <span data-ttu-id="26388-120">*x*</span><span class="sxs-lookup"><span data-stu-id="26388-120">*x*</span></span>   | <span data-ttu-id="26388-121">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz**</span><span class="sxs-lookup"><span data-stu-id="26388-121">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="26388-122">**flot**</span><span class="sxs-lookup"><span data-stu-id="26388-122">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="26388-123">cualquiera</span><span class="sxs-lookup"><span data-stu-id="26388-123">any</span></span>      |
| <span data-ttu-id="26388-124">*direcc*</span><span class="sxs-lookup"><span data-stu-id="26388-124">*ret*</span></span> | <span data-ttu-id="26388-125">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz**</span><span class="sxs-lookup"><span data-stu-id="26388-125">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="26388-126">**bool**</span><span class="sxs-lookup"><span data-stu-id="26388-126">**bool**</span></span>](/windows/desktop/WinProg/windows-data-types)                         | <span data-ttu-id="26388-127">como entrada</span><span class="sxs-lookup"><span data-stu-id="26388-127">as input</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="26388-128">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="26388-128">Minimum Shader Model</span></span>

<span data-ttu-id="26388-129">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="26388-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="26388-130">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="26388-130">Shader Model</span></span>                                                                       | <span data-ttu-id="26388-131">Compatible</span><span class="sxs-lookup"><span data-stu-id="26388-131">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="26388-132">Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="26388-132">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="26388-133">sí</span><span class="sxs-lookup"><span data-stu-id="26388-133">yes</span></span>                 |
| [<span data-ttu-id="26388-134">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="26388-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="26388-135">sí ( \_ solo vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="26388-135">yes (vs\_1\_1 only)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="26388-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26388-136">Requirements</span></span>



| <span data-ttu-id="26388-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="26388-137">Requirement</span></span> | <span data-ttu-id="26388-138">Value</span><span class="sxs-lookup"><span data-stu-id="26388-138">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="26388-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="26388-139">Header</span></span><br/> | <dl> <span data-ttu-id="26388-140"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="26388-140"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26388-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="26388-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26388-142">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="26388-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

