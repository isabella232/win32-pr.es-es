---
title: isNaN (Corecrt \_ Math. h)
description: Determina si el valor especificado es NAN o QNAN.
ms.assetid: 09085634-e610-4793-848e-abda8241f1cc
keywords:
- desisnan HLSL
topic_type:
- apiref
api_name:
- isnan
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef9f4549b6a142f5bf6011cdfb144de92efde64c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083798"
---
# <a name="isnan"></a><span data-ttu-id="a8f44-104">isnan</span><span class="sxs-lookup"><span data-stu-id="a8f44-104">isnan</span></span>

<span data-ttu-id="a8f44-105">Determina si el valor especificado es NAN o QNAN.</span><span class="sxs-lookup"><span data-stu-id="a8f44-105">Determines if the specified value is NAN or QNAN.</span></span>



| <span data-ttu-id="a8f44-106">el isNaN de *RET* (*x*)</span><span class="sxs-lookup"><span data-stu-id="a8f44-106">*ret* isnan(*x*)</span></span> |
|------------------|



 

## <a name="parameters"></a><span data-ttu-id="a8f44-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a8f44-107">Parameters</span></span>



| <span data-ttu-id="a8f44-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="a8f44-108">Item</span></span>                                                   | <span data-ttu-id="a8f44-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="a8f44-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="a8f44-110"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="a8f44-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="a8f44-111">\[en \] el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="a8f44-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="a8f44-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a8f44-112">Return Value</span></span>

<span data-ttu-id="a8f44-113">Devuelve un valor del mismo tamaño que la entrada, con un valor establecido en **true** si el parámetro *x* es Nan o QNAN.</span><span class="sxs-lookup"><span data-stu-id="a8f44-113">Returns a value of the same size as the input, with a value set to **True** if the *x* parameter is NAN or QNAN.</span></span> <span data-ttu-id="a8f44-114">En caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="a8f44-114">Otherwise, **False**.</span></span>

## <a name="type-description"></a><span data-ttu-id="a8f44-115">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="a8f44-115">Type Description</span></span>



| <span data-ttu-id="a8f44-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="a8f44-116">Name</span></span>  | [<span data-ttu-id="a8f44-117">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="a8f44-117">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="a8f44-118">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="a8f44-118">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="a8f44-119">Tamaño</span><span class="sxs-lookup"><span data-stu-id="a8f44-119">Size</span></span>     |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|----------|
| <span data-ttu-id="a8f44-120">*x*</span><span class="sxs-lookup"><span data-stu-id="a8f44-120">*x*</span></span>   | <span data-ttu-id="a8f44-121">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz**</span><span class="sxs-lookup"><span data-stu-id="a8f44-121">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="a8f44-122">**flot**</span><span class="sxs-lookup"><span data-stu-id="a8f44-122">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="a8f44-123">cualquiera</span><span class="sxs-lookup"><span data-stu-id="a8f44-123">any</span></span>      |
| <span data-ttu-id="a8f44-124">*direcc*</span><span class="sxs-lookup"><span data-stu-id="a8f44-124">*ret*</span></span> | <span data-ttu-id="a8f44-125">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz**</span><span class="sxs-lookup"><span data-stu-id="a8f44-125">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="a8f44-126">**bool**</span><span class="sxs-lookup"><span data-stu-id="a8f44-126">**bool**</span></span>](/windows/desktop/WinProg/windows-data-types)                         | <span data-ttu-id="a8f44-127">como entrada</span><span class="sxs-lookup"><span data-stu-id="a8f44-127">as input</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a8f44-128">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="a8f44-128">Minimum Shader Model</span></span>

<span data-ttu-id="a8f44-129">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="a8f44-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a8f44-130">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="a8f44-130">Shader Model</span></span>                                                                       | <span data-ttu-id="a8f44-131">Compatible</span><span class="sxs-lookup"><span data-stu-id="a8f44-131">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="a8f44-132">Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="a8f44-132">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="a8f44-133">sí</span><span class="sxs-lookup"><span data-stu-id="a8f44-133">yes</span></span>                 |
| [<span data-ttu-id="a8f44-134">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a8f44-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="a8f44-135">sí ( \_ solo vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="a8f44-135">yes (vs\_1\_1 only)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="a8f44-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8f44-136">Requirements</span></span>



| <span data-ttu-id="a8f44-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8f44-137">Requirement</span></span> | <span data-ttu-id="a8f44-138">Value</span><span class="sxs-lookup"><span data-stu-id="a8f44-138">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8f44-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a8f44-139">Header</span></span><br/> | <dl> <span data-ttu-id="a8f44-140"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8f44-140"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8f44-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="a8f44-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8f44-142">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="a8f44-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

