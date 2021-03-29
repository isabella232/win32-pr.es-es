---
title: Floor (Corecrt \_ Math. h)
description: Devuelve el entero más grande que es menor o igual que el valor especificado.
ms.assetid: f7193425-2448-4ae6-99d5-bb5e1aa74111
keywords:
- HLSL en planta
topic_type:
- apiref
api_name:
- floor
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ecb46719d5361ec9f7c36b21d94793bc9a67ffe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986857"
---
# <a name="floor"></a><span data-ttu-id="8b667-104">floor</span><span class="sxs-lookup"><span data-stu-id="8b667-104">floor</span></span>

<span data-ttu-id="8b667-105">Devuelve el entero más grande que es menor o igual que el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="8b667-105">Returns the largest integer that is less than or equal to the specified value.</span></span>



| <span data-ttu-id="8b667-106">*RET* Floor (*x*)</span><span class="sxs-lookup"><span data-stu-id="8b667-106">*ret* floor(*x*)</span></span> |
|------------------|



 

## <a name="parameters"></a><span data-ttu-id="8b667-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8b667-107">Parameters</span></span>



| <span data-ttu-id="8b667-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="8b667-108">Item</span></span>                                                   | <span data-ttu-id="8b667-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="8b667-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="8b667-110"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="8b667-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="8b667-111">\[en \] el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="8b667-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="8b667-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8b667-112">Return Value</span></span>

<span data-ttu-id="8b667-113">El valor entero más grande (devuelto como un tipo de punto flotante) que es menor o igual que el parámetro *x* .</span><span class="sxs-lookup"><span data-stu-id="8b667-113">The largest integer value (returned as a floating-point type) that is less than or equal to the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="8b667-114">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="8b667-114">Type Description</span></span>



| <span data-ttu-id="8b667-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="8b667-115">Name</span></span>  | [<span data-ttu-id="8b667-116">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="8b667-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="8b667-117">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="8b667-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="8b667-118">Tamaño</span><span class="sxs-lookup"><span data-stu-id="8b667-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="8b667-119">*x*</span><span class="sxs-lookup"><span data-stu-id="8b667-119">*x*</span></span>   | <span data-ttu-id="8b667-120">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz**</span><span class="sxs-lookup"><span data-stu-id="8b667-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="8b667-121">**flot**</span><span class="sxs-lookup"><span data-stu-id="8b667-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="8b667-122">cualquiera</span><span class="sxs-lookup"><span data-stu-id="8b667-122">any</span></span>                            |
| <span data-ttu-id="8b667-123">*direcc*</span><span class="sxs-lookup"><span data-stu-id="8b667-123">*ret*</span></span> | <span data-ttu-id="8b667-124">igual que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="8b667-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="8b667-125">**flot**</span><span class="sxs-lookup"><span data-stu-id="8b667-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="8b667-126">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="8b667-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8b667-127">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="8b667-127">Minimum Shader Model</span></span>

<span data-ttu-id="8b667-128">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="8b667-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="8b667-129">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="8b667-129">Shader Model</span></span>                                                                       | <span data-ttu-id="8b667-130">Compatible</span><span class="sxs-lookup"><span data-stu-id="8b667-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="8b667-131">Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="8b667-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="8b667-132">sí</span><span class="sxs-lookup"><span data-stu-id="8b667-132">yes</span></span>       |
| [<span data-ttu-id="8b667-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8b667-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="8b667-134">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="8b667-134">vs\_1\_1</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="8b667-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b667-135">Requirements</span></span>



| <span data-ttu-id="8b667-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b667-136">Requirement</span></span> | <span data-ttu-id="8b667-137">Value</span><span class="sxs-lookup"><span data-stu-id="8b667-137">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b667-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8b667-138">Header</span></span><br/> | <dl> <span data-ttu-id="8b667-139"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b667-139"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b667-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="8b667-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b667-141">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="8b667-141">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

