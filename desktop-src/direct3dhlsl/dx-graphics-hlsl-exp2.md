---
title: exp2 (Corecrt, \_ Math. h)
description: Devuelve el valor exponencial de base 2 o 2x del valor especificado.
ms.assetid: 68b0057c-864d-440b-84f6-781d5fa3b019
keywords:
- HLSL de exp2
topic_type:
- apiref
api_name:
- exp2
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63aaf5ee7c29da49ca2e7b21d80af6967721058d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986862"
---
# <a name="exp2"></a><span data-ttu-id="8ec63-104">exp2</span><span class="sxs-lookup"><span data-stu-id="8ec63-104">exp2</span></span>

<span data-ttu-id="8ec63-105">Devuelve el valor exponencial de base 2 o 2<sup>x</sup>del valor especificado.</span><span class="sxs-lookup"><span data-stu-id="8ec63-105">Returns the base 2 exponential, or 2<sup>x</sup>, of the specified value.</span></span>



| <span data-ttu-id="8ec63-106">*RET* exp2 (*x*)</span><span class="sxs-lookup"><span data-stu-id="8ec63-106">*ret* exp2(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="8ec63-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8ec63-107">Parameters</span></span>



| <span data-ttu-id="8ec63-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="8ec63-108">Item</span></span>                                                   | <span data-ttu-id="8ec63-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="8ec63-109">Description</span></span>                                           |
|--------------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="8ec63-110"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="8ec63-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="8ec63-111">\[en \] el valor de punto flotante especificado.</span><span class="sxs-lookup"><span data-stu-id="8ec63-111">\[in\] The specified floating-point value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="8ec63-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8ec63-112">Return Value</span></span>

<span data-ttu-id="8ec63-113">Valor exponencial de base 2 del parámetro *x* .</span><span class="sxs-lookup"><span data-stu-id="8ec63-113">The base 2 exponential of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="8ec63-114">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="8ec63-114">Type Description</span></span>



| <span data-ttu-id="8ec63-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="8ec63-115">Name</span></span>  | [<span data-ttu-id="8ec63-116">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="8ec63-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="8ec63-117">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="8ec63-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="8ec63-118">Tamaño</span><span class="sxs-lookup"><span data-stu-id="8ec63-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="8ec63-119">*x*</span><span class="sxs-lookup"><span data-stu-id="8ec63-119">*x*</span></span>   | <span data-ttu-id="8ec63-120">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz**</span><span class="sxs-lookup"><span data-stu-id="8ec63-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="8ec63-121">**flot**</span><span class="sxs-lookup"><span data-stu-id="8ec63-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="8ec63-122">cualquiera</span><span class="sxs-lookup"><span data-stu-id="8ec63-122">any</span></span>                            |
| <span data-ttu-id="8ec63-123">*direcc*</span><span class="sxs-lookup"><span data-stu-id="8ec63-123">*ret*</span></span> | <span data-ttu-id="8ec63-124">igual que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="8ec63-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="8ec63-125">**flot**</span><span class="sxs-lookup"><span data-stu-id="8ec63-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="8ec63-126">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="8ec63-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8ec63-127">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="8ec63-127">Minimum Shader Model</span></span>

<span data-ttu-id="8ec63-128">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="8ec63-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="8ec63-129">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="8ec63-129">Shader Model</span></span>                                                                       | <span data-ttu-id="8ec63-130">Compatible</span><span class="sxs-lookup"><span data-stu-id="8ec63-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="8ec63-131">Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="8ec63-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="8ec63-132">sí</span><span class="sxs-lookup"><span data-stu-id="8ec63-132">yes</span></span>       |
| [<span data-ttu-id="8ec63-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8ec63-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="8ec63-134">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="8ec63-134">vs\_1\_1</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="8ec63-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ec63-135">Requirements</span></span>



| <span data-ttu-id="8ec63-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ec63-136">Requirement</span></span> | <span data-ttu-id="8ec63-137">Value</span><span class="sxs-lookup"><span data-stu-id="8ec63-137">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ec63-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8ec63-138">Header</span></span><br/> | <dl> <span data-ttu-id="8ec63-139"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ec63-139"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ec63-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="8ec63-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ec63-141">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="8ec63-141">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

