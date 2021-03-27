---
title: normalizar
description: Normaliza el vector de punto flotante especificado según x/length (x).
ms.assetid: 7fd6f8ff-f3ff-4d14-b3fc-b44fdddf6c75
keywords:
- normalizar HLSL
topic_type:
- apiref
api_name:
- normalize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f48c78f80f5f92f950795018f05a46c7883d9736
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995597"
---
# <a name="normalize"></a><span data-ttu-id="aab55-104">normalizar</span><span class="sxs-lookup"><span data-stu-id="aab55-104">normalize</span></span>

<span data-ttu-id="aab55-105">Normaliza el vector de punto flotante especificado según x/length (x).</span><span class="sxs-lookup"><span data-stu-id="aab55-105">Normalizes the specified floating-point vector according to x / length(x).</span></span>



| <span data-ttu-id="aab55-106">*Normalize (* *x*)</span><span class="sxs-lookup"><span data-stu-id="aab55-106">*ret* normalize(*x*)</span></span> |
|----------------------|



 

## <a name="parameters"></a><span data-ttu-id="aab55-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aab55-107">Parameters</span></span>



| <span data-ttu-id="aab55-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="aab55-108">Item</span></span>                                                   | <span data-ttu-id="aab55-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="aab55-109">Description</span></span>                                            |
|--------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="aab55-110"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="aab55-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="aab55-111">\[en \] el vector de punto flotante especificado.</span><span class="sxs-lookup"><span data-stu-id="aab55-111">\[in\] The specified floating-point vector.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="aab55-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aab55-112">Return Value</span></span>

<span data-ttu-id="aab55-113">Parámetro *x* normalizado.</span><span class="sxs-lookup"><span data-stu-id="aab55-113">The normalized *x* parameter.</span></span> <span data-ttu-id="aab55-114">Si la longitud del parámetro *x* es 0, el resultado es indefinido.</span><span class="sxs-lookup"><span data-stu-id="aab55-114">If the length of the *x* parameter is 0, the result is indefinite.</span></span>

## <a name="remarks"></a><span data-ttu-id="aab55-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aab55-115">Remarks</span></span>

<span data-ttu-id="aab55-116">La función **normalizar** intrínseca de HLSL usa la siguiente fórmula: *x*  /  [**longitud**](dx-graphics-hlsl-length.md)(*x*).</span><span class="sxs-lookup"><span data-stu-id="aab55-116">The **normalize** HLSL intrinsic function uses the following formula: *x* / [**length**](dx-graphics-hlsl-length.md)(*x*).</span></span>

## <a name="type-description"></a><span data-ttu-id="aab55-117">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="aab55-117">Type Description</span></span>



| <span data-ttu-id="aab55-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="aab55-118">Name</span></span>  | [<span data-ttu-id="aab55-119">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="aab55-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="aab55-120">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="aab55-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="aab55-121">Tamaño</span><span class="sxs-lookup"><span data-stu-id="aab55-121">Size</span></span>                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="aab55-122">*x*</span><span class="sxs-lookup"><span data-stu-id="aab55-122">*x*</span></span>   | [<span data-ttu-id="aab55-123">**medios**</span><span class="sxs-lookup"><span data-stu-id="aab55-123">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="aab55-124">**flot**</span><span class="sxs-lookup"><span data-stu-id="aab55-124">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="aab55-125">cualquiera</span><span class="sxs-lookup"><span data-stu-id="aab55-125">any</span></span>                            |
| <span data-ttu-id="aab55-126">*direcc*</span><span class="sxs-lookup"><span data-stu-id="aab55-126">*ret*</span></span> | <span data-ttu-id="aab55-127">igual que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="aab55-127">same as input *x*</span></span>                                                                   | [<span data-ttu-id="aab55-128">**flot**</span><span class="sxs-lookup"><span data-stu-id="aab55-128">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="aab55-129">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="aab55-129">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="aab55-130">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="aab55-130">Minimum Shader Model</span></span>

<span data-ttu-id="aab55-131">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="aab55-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="aab55-132">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="aab55-132">Shader Model</span></span>                                                                       | <span data-ttu-id="aab55-133">Compatible</span><span class="sxs-lookup"><span data-stu-id="aab55-133">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="aab55-134">Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="aab55-134">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="aab55-135">sí</span><span class="sxs-lookup"><span data-stu-id="aab55-135">yes</span></span>                 |
| [<span data-ttu-id="aab55-136">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="aab55-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="aab55-137">sí ( \_ solo vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="aab55-137">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="aab55-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="aab55-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aab55-139">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="aab55-139">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

