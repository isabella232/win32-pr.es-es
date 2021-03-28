---
title: Ceil ((Corecrt, \_ Math. h)
description: Devuelve el valor entero más pequeño que es mayor o igual que el valor especificado.
ms.assetid: 9823f321-14c3-4b27-9a4b-7a885cece39b
keywords:
- HLSL de Ceil (
topic_type:
- apiref
api_name:
- ceil
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec86db320119b7f162ed48a748c1d1ff4335b6f3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998359"
---
# <a name="ceil"></a><span data-ttu-id="32706-104">ceil</span><span class="sxs-lookup"><span data-stu-id="32706-104">ceil</span></span>

<span data-ttu-id="32706-105">Devuelve el valor entero más pequeño que es mayor o igual que el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="32706-105">Returns the smallest integer value that is greater than or equal to the specified value.</span></span>



| <span data-ttu-id="32706-106">*RET* Ceil ((*x*)</span><span class="sxs-lookup"><span data-stu-id="32706-106">*ret* ceil(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="32706-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="32706-107">Parameters</span></span>



| <span data-ttu-id="32706-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="32706-108">Item</span></span>                                                   | <span data-ttu-id="32706-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="32706-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="32706-110"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="32706-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="32706-111">\[en \] el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="32706-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="32706-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="32706-112">Return Value</span></span>

<span data-ttu-id="32706-113">Valor entero más pequeño (devuelto como tipo de punto flotante) que es mayor o igual que el parámetro *x* .</span><span class="sxs-lookup"><span data-stu-id="32706-113">The smallest integer value (returned as a floating-point type) that is greater than or equal to the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="32706-114">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="32706-114">Type Description</span></span>



| <span data-ttu-id="32706-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="32706-115">Name</span></span>  | [<span data-ttu-id="32706-116">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="32706-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="32706-117">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="32706-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="32706-118">Tamaño</span><span class="sxs-lookup"><span data-stu-id="32706-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="32706-119">*x*</span><span class="sxs-lookup"><span data-stu-id="32706-119">*x*</span></span>   | <span data-ttu-id="32706-120">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz**</span><span class="sxs-lookup"><span data-stu-id="32706-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="32706-121">**flot**</span><span class="sxs-lookup"><span data-stu-id="32706-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="32706-122">cualquiera</span><span class="sxs-lookup"><span data-stu-id="32706-122">any</span></span>                            |
| <span data-ttu-id="32706-123">*direcc*</span><span class="sxs-lookup"><span data-stu-id="32706-123">*ret*</span></span> | <span data-ttu-id="32706-124">igual que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="32706-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="32706-125">**flot**</span><span class="sxs-lookup"><span data-stu-id="32706-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="32706-126">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="32706-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="32706-127">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="32706-127">Minimum Shader Model</span></span>

<span data-ttu-id="32706-128">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="32706-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="32706-129">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="32706-129">Shader Model</span></span>                                                                       | <span data-ttu-id="32706-130">Compatible</span><span class="sxs-lookup"><span data-stu-id="32706-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="32706-131">Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="32706-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="32706-132">sí</span><span class="sxs-lookup"><span data-stu-id="32706-132">yes</span></span>       |
| [<span data-ttu-id="32706-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="32706-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="32706-134">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="32706-134">vs\_1\_1</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="32706-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32706-135">Requirements</span></span>



| <span data-ttu-id="32706-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="32706-136">Requirement</span></span> | <span data-ttu-id="32706-137">Value</span><span class="sxs-lookup"><span data-stu-id="32706-137">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="32706-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="32706-138">Header</span></span><br/> | <dl> <span data-ttu-id="32706-139"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="32706-139"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32706-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="32706-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32706-141">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="32706-141">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

