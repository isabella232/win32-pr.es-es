---
title: rsqrt (
description: Devuelve el recíproco de la raíz cuadrada del valor especificado.
ms.assetid: 4e266e41-cde9-4a59-8937-98bfc63f3b5d
keywords:
- HLSL de rsqrt (
topic_type:
- apiref
api_name:
- rsqrt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 56eb5f1cba8510e57a2c4b5622e10dc91666b6a6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997081"
---
# <a name="rsqrt"></a><span data-ttu-id="b90ba-104">rsqrt (</span><span class="sxs-lookup"><span data-stu-id="b90ba-104">rsqrt</span></span>

<span data-ttu-id="b90ba-105">Devuelve el recíproco de la raíz cuadrada del valor especificado.</span><span class="sxs-lookup"><span data-stu-id="b90ba-105">Returns the reciprocal of the square root of the specified value.</span></span>



| <span data-ttu-id="b90ba-106">*RET* rsqrt ((*x*)</span><span class="sxs-lookup"><span data-stu-id="b90ba-106">*ret* rsqrt(*x*)</span></span> |
|------------------|



 

## <a name="parameters"></a><span data-ttu-id="b90ba-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b90ba-107">Parameters</span></span>



| <span data-ttu-id="b90ba-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="b90ba-108">Item</span></span>                                                   | <span data-ttu-id="b90ba-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="b90ba-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="b90ba-110"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="b90ba-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="b90ba-111">\[en \] el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="b90ba-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="b90ba-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b90ba-112">Return Value</span></span>

<span data-ttu-id="b90ba-113">Recíproco de la raíz cuadrada del parámetro *x* .</span><span class="sxs-lookup"><span data-stu-id="b90ba-113">The reciprocal of the square root of the *x* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="b90ba-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b90ba-114">Remarks</span></span>

<span data-ttu-id="b90ba-115">Esta función usa la siguiente fórmula: 1/ **sqrt**(*x*).</span><span class="sxs-lookup"><span data-stu-id="b90ba-115">This function uses the following formula: 1 / **sqrt**(*x*).</span></span>

## <a name="type-description"></a><span data-ttu-id="b90ba-116">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="b90ba-116">Type Description</span></span>



| <span data-ttu-id="b90ba-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="b90ba-117">Name</span></span>  | [<span data-ttu-id="b90ba-118">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="b90ba-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="b90ba-119">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="b90ba-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="b90ba-120">Tamaño</span><span class="sxs-lookup"><span data-stu-id="b90ba-120">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="b90ba-121">*x*</span><span class="sxs-lookup"><span data-stu-id="b90ba-121">*x*</span></span>   | <span data-ttu-id="b90ba-122">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz**</span><span class="sxs-lookup"><span data-stu-id="b90ba-122">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="b90ba-123">**flot**</span><span class="sxs-lookup"><span data-stu-id="b90ba-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b90ba-124">cualquiera</span><span class="sxs-lookup"><span data-stu-id="b90ba-124">any</span></span>                            |
| <span data-ttu-id="b90ba-125">*direcc*</span><span class="sxs-lookup"><span data-stu-id="b90ba-125">*ret*</span></span> | <span data-ttu-id="b90ba-126">igual que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="b90ba-126">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="b90ba-127">**flot**</span><span class="sxs-lookup"><span data-stu-id="b90ba-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b90ba-128">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="b90ba-128">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b90ba-129">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="b90ba-129">Minimum Shader Model</span></span>

<span data-ttu-id="b90ba-130">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="b90ba-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b90ba-131">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="b90ba-131">Shader Model</span></span>                                                                       | <span data-ttu-id="b90ba-132">Compatible</span><span class="sxs-lookup"><span data-stu-id="b90ba-132">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="b90ba-133">Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="b90ba-133">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="b90ba-134">sí</span><span class="sxs-lookup"><span data-stu-id="b90ba-134">yes</span></span>                 |
| [<span data-ttu-id="b90ba-135">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b90ba-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="b90ba-136">sí ( \_ solo vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="b90ba-136">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="b90ba-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="b90ba-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b90ba-138">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="b90ba-138">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

