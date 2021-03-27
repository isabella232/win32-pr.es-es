---
title: exp
description: Devuelve el valor exponencial de base e, o ex, del valor especificado.
ms.assetid: 7a713251-af47-4f8d-b708-40309b80ba18
keywords:
- HLSL de exp
topic_type:
- apiref
api_name:
- exp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 699eb97ae0fd6bbdeba0da47693178d1e4c48e36
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792045"
---
# <a name="exp"></a><span data-ttu-id="c6260-104">exp</span><span class="sxs-lookup"><span data-stu-id="c6260-104">exp</span></span>

<span data-ttu-id="c6260-105">Devuelve el valor exponencial de base e, o e<sup>x</sup>, del valor especificado.</span><span class="sxs-lookup"><span data-stu-id="c6260-105">Returns the base-e exponential, or e<sup>x</sup>, of the specified value.</span></span>



| <span data-ttu-id="c6260-106">*RET* exp (*x*)</span><span class="sxs-lookup"><span data-stu-id="c6260-106">*ret* exp(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="c6260-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c6260-107">Parameters</span></span>



| <span data-ttu-id="c6260-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="c6260-108">Item</span></span>                                                   | <span data-ttu-id="c6260-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="c6260-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="c6260-110"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="c6260-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="c6260-111">\[en \] el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="c6260-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="c6260-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c6260-112">Return Value</span></span>

<span data-ttu-id="c6260-113">El valor exponencial de base e del parámetro *x* .</span><span class="sxs-lookup"><span data-stu-id="c6260-113">The base-e exponential of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="c6260-114">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="c6260-114">Type Description</span></span>



| <span data-ttu-id="c6260-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="c6260-115">Name</span></span>  | [<span data-ttu-id="c6260-116">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="c6260-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="c6260-117">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="c6260-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="c6260-118">Tamaño</span><span class="sxs-lookup"><span data-stu-id="c6260-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="c6260-119">*x*</span><span class="sxs-lookup"><span data-stu-id="c6260-119">*x*</span></span>   | <span data-ttu-id="c6260-120">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz**</span><span class="sxs-lookup"><span data-stu-id="c6260-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="c6260-121">**flot**</span><span class="sxs-lookup"><span data-stu-id="c6260-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="c6260-122">cualquiera</span><span class="sxs-lookup"><span data-stu-id="c6260-122">any</span></span>                            |
| <span data-ttu-id="c6260-123">*direcc*</span><span class="sxs-lookup"><span data-stu-id="c6260-123">*ret*</span></span> | <span data-ttu-id="c6260-124">igual que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="c6260-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="c6260-125">**flot**</span><span class="sxs-lookup"><span data-stu-id="c6260-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="c6260-126">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="c6260-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c6260-127">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="c6260-127">Minimum Shader Model</span></span>

<span data-ttu-id="c6260-128">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="c6260-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c6260-129">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="c6260-129">Shader Model</span></span>                                                                       | <span data-ttu-id="c6260-130">Compatible</span><span class="sxs-lookup"><span data-stu-id="c6260-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="c6260-131">Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="c6260-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="c6260-132">sí</span><span class="sxs-lookup"><span data-stu-id="c6260-132">yes</span></span>       |
| [<span data-ttu-id="c6260-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c6260-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="c6260-134">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="c6260-134">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="c6260-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="c6260-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6260-136">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="c6260-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

