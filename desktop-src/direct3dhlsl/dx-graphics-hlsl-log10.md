---
title: log10
description: Devuelve el logaritmo en base 10 del valor especificado.
ms.assetid: a94f8438-8153-4a31-bde3-98831edf99e5
keywords:
- HLSL de log10
topic_type:
- apiref
api_name:
- log10
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2d226dcc33da1aee6d55e21c6d97febc23577503
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359255"
---
# <a name="log10"></a><span data-ttu-id="e28ae-104">log10</span><span class="sxs-lookup"><span data-stu-id="e28ae-104">log10</span></span>

<span data-ttu-id="e28ae-105">Devuelve el logaritmo en base 10 del valor especificado.</span><span class="sxs-lookup"><span data-stu-id="e28ae-105">Returns the base-10 logarithm of the specified value.</span></span>



| <span data-ttu-id="e28ae-106">*RET* log10 (*x*)</span><span class="sxs-lookup"><span data-stu-id="e28ae-106">*ret* log10(*x*)</span></span> |
|------------------|



 

## <a name="parameters"></a><span data-ttu-id="e28ae-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e28ae-107">Parameters</span></span>



| <span data-ttu-id="e28ae-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="e28ae-108">Item</span></span>                                                   | <span data-ttu-id="e28ae-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="e28ae-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="e28ae-110"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="e28ae-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="e28ae-111">\[en \] el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="e28ae-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="e28ae-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e28ae-112">Return Value</span></span>

<span data-ttu-id="e28ae-113">Logaritmo en base 10 del parámetro *x* .</span><span class="sxs-lookup"><span data-stu-id="e28ae-113">The base-10 logarithm of the *x* parameter.</span></span> <span data-ttu-id="e28ae-114">Si el parámetro *x* es negativo, esta función devuelve un valor indefinido.</span><span class="sxs-lookup"><span data-stu-id="e28ae-114">If the *x* parameter is negative, this function returns indefinite.</span></span> <span data-ttu-id="e28ae-115">Si *x* es 0, esta función devuelve-INF.</span><span class="sxs-lookup"><span data-stu-id="e28ae-115">If the *x* is 0, this function returns -INF.</span></span>

## <a name="type-description"></a><span data-ttu-id="e28ae-116">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="e28ae-116">Type Description</span></span>



| <span data-ttu-id="e28ae-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="e28ae-117">Name</span></span>  | [<span data-ttu-id="e28ae-118">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="e28ae-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="e28ae-119">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="e28ae-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="e28ae-120">Tamaño</span><span class="sxs-lookup"><span data-stu-id="e28ae-120">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="e28ae-121">*x*</span><span class="sxs-lookup"><span data-stu-id="e28ae-121">*x*</span></span>   | <span data-ttu-id="e28ae-122">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz**</span><span class="sxs-lookup"><span data-stu-id="e28ae-122">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="e28ae-123">**flot**</span><span class="sxs-lookup"><span data-stu-id="e28ae-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="e28ae-124">cualquiera</span><span class="sxs-lookup"><span data-stu-id="e28ae-124">any</span></span>                            |
| <span data-ttu-id="e28ae-125">*direcc*</span><span class="sxs-lookup"><span data-stu-id="e28ae-125">*ret*</span></span> | <span data-ttu-id="e28ae-126">igual que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="e28ae-126">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="e28ae-127">**flot**</span><span class="sxs-lookup"><span data-stu-id="e28ae-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="e28ae-128">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="e28ae-128">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e28ae-129">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="e28ae-129">Minimum Shader Model</span></span>

<span data-ttu-id="e28ae-130">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="e28ae-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="e28ae-131">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="e28ae-131">Shader Model</span></span>                                                                       | <span data-ttu-id="e28ae-132">Compatible</span><span class="sxs-lookup"><span data-stu-id="e28ae-132">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="e28ae-133">Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="e28ae-133">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="e28ae-134">sí</span><span class="sxs-lookup"><span data-stu-id="e28ae-134">yes</span></span>                 |
| [<span data-ttu-id="e28ae-135">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e28ae-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="e28ae-136">sí ( \_ solo vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="e28ae-136">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="e28ae-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="e28ae-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e28ae-138">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="e28ae-138">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

