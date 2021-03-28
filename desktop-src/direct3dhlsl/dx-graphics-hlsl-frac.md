---
title: frac
description: Devuelve la parte fraccionaria (o decimal) de x; que es mayor o igual que 0 y menor que 1.
ms.assetid: 4e85390f-2b1a-402b-b932-09b80097f7e6
keywords:
- HLSL de frac
topic_type:
- apiref
api_name:
- frac
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 468bddc34f22f9bb5f34871102678e1765148b11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488218"
---
# <a name="frac"></a><span data-ttu-id="f9156-104">frac</span><span class="sxs-lookup"><span data-stu-id="f9156-104">frac</span></span>

<span data-ttu-id="f9156-105">Devuelve la parte fraccionaria (o decimal) de x; que es mayor o igual que 0 y menor que 1.</span><span class="sxs-lookup"><span data-stu-id="f9156-105">Returns the fractional (or decimal) part of x; which is greater than or equal to 0 and less than 1.</span></span>

<span data-ttu-id="f9156-106">Vea también [trunc](./dx-graphics-hlsl-trunc.md).</span><span class="sxs-lookup"><span data-stu-id="f9156-106">Also see [trunc](./dx-graphics-hlsl-trunc.md).</span></span>

| <span data-ttu-id="f9156-107">*RET* frac (*x*)</span><span class="sxs-lookup"><span data-stu-id="f9156-107">*ret* frac(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="f9156-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f9156-108">Parameters</span></span>



| <span data-ttu-id="f9156-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="f9156-109">Item</span></span>                                                   | <span data-ttu-id="f9156-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="f9156-110">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="f9156-111"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="f9156-111"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="f9156-112">\[en \] el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="f9156-112">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="f9156-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f9156-113">Return Value</span></span>

<span data-ttu-id="f9156-114">Parte fraccionaria del parámetro *x* .</span><span class="sxs-lookup"><span data-stu-id="f9156-114">The fractional part of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="f9156-115">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="f9156-115">Type Description</span></span>



| <span data-ttu-id="f9156-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="f9156-116">Name</span></span>  | [<span data-ttu-id="f9156-117">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="f9156-117">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="f9156-118">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="f9156-118">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="f9156-119">Tamaño</span><span class="sxs-lookup"><span data-stu-id="f9156-119">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="f9156-120">*x*</span><span class="sxs-lookup"><span data-stu-id="f9156-120">*x*</span></span>   | <span data-ttu-id="f9156-121">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz**</span><span class="sxs-lookup"><span data-stu-id="f9156-121">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="f9156-122">**flot**</span><span class="sxs-lookup"><span data-stu-id="f9156-122">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="f9156-123">cualquiera</span><span class="sxs-lookup"><span data-stu-id="f9156-123">any</span></span>                            |
| <span data-ttu-id="f9156-124">*direcc*</span><span class="sxs-lookup"><span data-stu-id="f9156-124">*ret*</span></span> | <span data-ttu-id="f9156-125">igual que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="f9156-125">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="f9156-126">**flot**</span><span class="sxs-lookup"><span data-stu-id="f9156-126">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="f9156-127">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="f9156-127">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f9156-128">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="f9156-128">Minimum Shader Model</span></span>

<span data-ttu-id="f9156-129">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="f9156-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f9156-130">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="f9156-130">Shader Model</span></span>                                                                       | <span data-ttu-id="f9156-131">Compatible</span><span class="sxs-lookup"><span data-stu-id="f9156-131">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="f9156-132">Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="f9156-132">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="f9156-133">sí</span><span class="sxs-lookup"><span data-stu-id="f9156-133">yes</span></span>       |
| [<span data-ttu-id="f9156-134">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f9156-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="f9156-135">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="f9156-135">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="f9156-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="f9156-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9156-137">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="f9156-137">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

