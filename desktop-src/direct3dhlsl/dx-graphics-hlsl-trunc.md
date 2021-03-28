---
title: trunc (Corecrt \_ Math. h)
description: Trunca un valor de punto flotante al componente entero.
ms.assetid: a0978fa2-71f8-4257-8c90-96224c2ec953
keywords:
- truncar HLSL
topic_type:
- apiref
api_name:
- trunc
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34493f60e60bc0dce35f5f9db50360265191c742
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998460"
---
# <a name="trunc"></a><span data-ttu-id="2ab19-104">trunc</span><span class="sxs-lookup"><span data-stu-id="2ab19-104">trunc</span></span>

<span data-ttu-id="2ab19-105">Trunca un valor de punto flotante al componente entero.</span><span class="sxs-lookup"><span data-stu-id="2ab19-105">Truncates a floating-point value to the integer component.</span></span>



| <span data-ttu-id="2ab19-106">RET trunc (*x*)</span><span class="sxs-lookup"><span data-stu-id="2ab19-106">ret trunc(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="2ab19-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2ab19-107">Parameters</span></span>



| <span data-ttu-id="2ab19-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="2ab19-108">Item</span></span>                                                   | <span data-ttu-id="2ab19-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="2ab19-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="2ab19-110"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="2ab19-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="2ab19-111">\[en \] la entrada especificada.</span><span class="sxs-lookup"><span data-stu-id="2ab19-111">\[in\] The specified input.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="2ab19-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2ab19-112">Return Value</span></span>

<span data-ttu-id="2ab19-113">El valor de entrada se trunca a un componente entero.</span><span class="sxs-lookup"><span data-stu-id="2ab19-113">The input value truncated to an integer component.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ab19-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2ab19-114">Remarks</span></span>

<span data-ttu-id="2ab19-115">Esta función trunca un valor de punto flotante al componente entero.</span><span class="sxs-lookup"><span data-stu-id="2ab19-115">This function truncates a floating-point value to the integer component.</span></span> <span data-ttu-id="2ab19-116">Dado un valor de punto flotante de 1,6, la función trunc devolvería 1,0, donde la función [**Round (DirectX HLSL)**](dx-graphics-hlsl-round.md) devolvería 2,0.</span><span class="sxs-lookup"><span data-stu-id="2ab19-116">Given a floating-point value of 1.6, the trunc function would return 1.0, where as the [**round (DirectX HLSL)**](dx-graphics-hlsl-round.md) function would return 2.0.</span></span>

## <a name="type-description"></a><span data-ttu-id="2ab19-117">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="2ab19-117">Type Description</span></span>



| <span data-ttu-id="2ab19-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="2ab19-118">Name</span></span> | [<span data-ttu-id="2ab19-119">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="2ab19-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="2ab19-120">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="2ab19-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="2ab19-121">Tamaño</span><span class="sxs-lookup"><span data-stu-id="2ab19-121">Size</span></span>                         |
|------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|------------------------------|
| <span data-ttu-id="2ab19-122">*x*</span><span class="sxs-lookup"><span data-stu-id="2ab19-122">*x*</span></span>  | <span data-ttu-id="2ab19-123">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz**</span><span class="sxs-lookup"><span data-stu-id="2ab19-123">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="2ab19-124">**flot**</span><span class="sxs-lookup"><span data-stu-id="2ab19-124">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="2ab19-125">cualquiera</span><span class="sxs-lookup"><span data-stu-id="2ab19-125">any</span></span>                          |
| <span data-ttu-id="2ab19-126">direcc</span><span class="sxs-lookup"><span data-stu-id="2ab19-126">ret</span></span>  | <span data-ttu-id="2ab19-127">El mismo tipo que la entrada x</span><span class="sxs-lookup"><span data-stu-id="2ab19-127">Same type as input x</span></span>                                                                                           | [<span data-ttu-id="2ab19-128">**flot**</span><span class="sxs-lookup"><span data-stu-id="2ab19-128">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="2ab19-129">Mismas dimensiones que la entrada x</span><span class="sxs-lookup"><span data-stu-id="2ab19-129">Same dimension(s) as input x</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2ab19-130">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="2ab19-130">Minimum Shader Model</span></span>

<span data-ttu-id="2ab19-131">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="2ab19-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2ab19-132">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="2ab19-132">Shader Model</span></span>                                                                       | <span data-ttu-id="2ab19-133">Compatible</span><span class="sxs-lookup"><span data-stu-id="2ab19-133">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="2ab19-134">Modelador [modelo 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="2ab19-134">[Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) and higher shader models</span></span> | <span data-ttu-id="2ab19-135">sí</span><span class="sxs-lookup"><span data-stu-id="2ab19-135">yes</span></span>       |



 

## <a name="requirements"></a><span data-ttu-id="2ab19-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ab19-136">Requirements</span></span>



| <span data-ttu-id="2ab19-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ab19-137">Requirement</span></span> | <span data-ttu-id="2ab19-138">Value</span><span class="sxs-lookup"><span data-stu-id="2ab19-138">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ab19-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2ab19-139">Header</span></span><br/> | <dl> <span data-ttu-id="2ab19-140"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ab19-140"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ab19-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="2ab19-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ab19-142">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="2ab19-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

