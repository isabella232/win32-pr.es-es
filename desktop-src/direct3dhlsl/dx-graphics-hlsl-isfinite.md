---
title: isFinite ((Corecrt, \_ Math. h)
description: Determina si el valor de punto flotante especificado es finito.
ms.assetid: 8be10499-2d06-4520-9697-dab2f461bd0d
keywords:
- HLSL de isFinite (
topic_type:
- apiref
api_name:
- isfinite
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f63c943dadccad9f485668948f366698f3bce5e6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998389"
---
# <a name="isfinite"></a><span data-ttu-id="20ff2-104">isFinite (</span><span class="sxs-lookup"><span data-stu-id="20ff2-104">isfinite</span></span>

<span data-ttu-id="20ff2-105">Determina si el valor de punto flotante especificado es finito.</span><span class="sxs-lookup"><span data-stu-id="20ff2-105">Determines if the specified floating-point value is finite.</span></span>



| <span data-ttu-id="20ff2-106">*RET* isFinite ((*x*)</span><span class="sxs-lookup"><span data-stu-id="20ff2-106">*ret* isfinite(*x*)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="20ff2-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="20ff2-107">Parameters</span></span>



| <span data-ttu-id="20ff2-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="20ff2-108">Item</span></span>                                                   | <span data-ttu-id="20ff2-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="20ff2-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="20ff2-110"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="20ff2-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="20ff2-111">\[en \] el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="20ff2-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="20ff2-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="20ff2-112">Return Value</span></span>

<span data-ttu-id="20ff2-113">Devuelve un valor del mismo tamaño que la entrada, con un valor establecido en **true** si el parámetro *x* es finito; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="20ff2-113">Returns a value of the same size as the input, with a value set to **True** if the *x* parameter is finite; otherwise **False**.</span></span>

## <a name="type-description"></a><span data-ttu-id="20ff2-114">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="20ff2-114">Type Description</span></span>



| <span data-ttu-id="20ff2-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="20ff2-115">Name</span></span>  | [<span data-ttu-id="20ff2-116">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="20ff2-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="20ff2-117">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="20ff2-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="20ff2-118">Tamaño</span><span class="sxs-lookup"><span data-stu-id="20ff2-118">Size</span></span>     |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|----------|
| <span data-ttu-id="20ff2-119">*x*</span><span class="sxs-lookup"><span data-stu-id="20ff2-119">*x*</span></span>   | <span data-ttu-id="20ff2-120">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz**</span><span class="sxs-lookup"><span data-stu-id="20ff2-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="20ff2-121">**flot**</span><span class="sxs-lookup"><span data-stu-id="20ff2-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="20ff2-122">cualquiera</span><span class="sxs-lookup"><span data-stu-id="20ff2-122">any</span></span>      |
| <span data-ttu-id="20ff2-123">*direcc*</span><span class="sxs-lookup"><span data-stu-id="20ff2-123">*ret*</span></span> | <span data-ttu-id="20ff2-124">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz**</span><span class="sxs-lookup"><span data-stu-id="20ff2-124">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="20ff2-125">**bool**</span><span class="sxs-lookup"><span data-stu-id="20ff2-125">**bool**</span></span>](/windows/desktop/WinProg/windows-data-types)                         | <span data-ttu-id="20ff2-126">como entrada</span><span class="sxs-lookup"><span data-stu-id="20ff2-126">as input</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="20ff2-127">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="20ff2-127">Minimum Shader Model</span></span>

<span data-ttu-id="20ff2-128">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="20ff2-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="20ff2-129">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="20ff2-129">Shader Model</span></span>                                                                       | <span data-ttu-id="20ff2-130">Compatible</span><span class="sxs-lookup"><span data-stu-id="20ff2-130">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="20ff2-131">Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="20ff2-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="20ff2-132">sí</span><span class="sxs-lookup"><span data-stu-id="20ff2-132">yes</span></span>                 |
| [<span data-ttu-id="20ff2-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="20ff2-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="20ff2-134">sí ( \_ solo vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="20ff2-134">yes (vs\_1\_1 only)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="20ff2-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20ff2-135">Requirements</span></span>



| <span data-ttu-id="20ff2-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="20ff2-136">Requirement</span></span> | <span data-ttu-id="20ff2-137">Value</span><span class="sxs-lookup"><span data-stu-id="20ff2-137">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="20ff2-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="20ff2-138">Header</span></span><br/> | <dl> <span data-ttu-id="20ff2-139"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="20ff2-139"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20ff2-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="20ff2-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20ff2-141">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="20ff2-141">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

