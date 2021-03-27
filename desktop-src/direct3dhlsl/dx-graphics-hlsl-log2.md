---
title: LOG2 (Corecrt, \_ Math. h)
description: Devuelve el logaritmo en base 2 del valor especificado.
ms.assetid: 0bc75697-92c0-4de5-89bd-2ce824baa03e
keywords:
- HLSL de LOG2
topic_type:
- apiref
api_name:
- log2
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81692071b7886fa3e3096d785bccf80c7eff937a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003962"
---
# <a name="log2"></a><span data-ttu-id="16b84-104">LOG2</span><span class="sxs-lookup"><span data-stu-id="16b84-104">log2</span></span>

<span data-ttu-id="16b84-105">Devuelve el logaritmo en base 2 del valor especificado.</span><span class="sxs-lookup"><span data-stu-id="16b84-105">Returns the base-2 logarithm of the specified value.</span></span>



| <span data-ttu-id="16b84-106">*RET* LOG2 (*x*)</span><span class="sxs-lookup"><span data-stu-id="16b84-106">*ret* log2(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="16b84-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="16b84-107">Parameters</span></span>



| <span data-ttu-id="16b84-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="16b84-108">Item</span></span>                                                   | <span data-ttu-id="16b84-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="16b84-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="16b84-110"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="16b84-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="16b84-111">\[en \] el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="16b84-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="16b84-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="16b84-112">Return Value</span></span>

<span data-ttu-id="16b84-113">Logaritmo en base 2 del parámetro *x* .</span><span class="sxs-lookup"><span data-stu-id="16b84-113">The base-2 logarithm of the *x* parameter.</span></span> <span data-ttu-id="16b84-114">Si el parámetro *x* es negativo, esta función devuelve un valor indefinido.</span><span class="sxs-lookup"><span data-stu-id="16b84-114">If the *x* parameter is negative, this function returns indefinite.</span></span> <span data-ttu-id="16b84-115">Si el parámetro *x* es 0, esta función devuelve + INF.</span><span class="sxs-lookup"><span data-stu-id="16b84-115">If the *x* parameter is 0, this function returns +INF.</span></span>

## <a name="type-description"></a><span data-ttu-id="16b84-116">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="16b84-116">Type Description</span></span>



| <span data-ttu-id="16b84-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="16b84-117">Name</span></span>  | [<span data-ttu-id="16b84-118">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="16b84-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="16b84-119">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="16b84-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="16b84-120">Tamaño</span><span class="sxs-lookup"><span data-stu-id="16b84-120">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="16b84-121">*x*</span><span class="sxs-lookup"><span data-stu-id="16b84-121">*x*</span></span>   | <span data-ttu-id="16b84-122">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz**</span><span class="sxs-lookup"><span data-stu-id="16b84-122">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="16b84-123">**flot**</span><span class="sxs-lookup"><span data-stu-id="16b84-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="16b84-124">cualquiera</span><span class="sxs-lookup"><span data-stu-id="16b84-124">any</span></span>                            |
| <span data-ttu-id="16b84-125">*direcc*</span><span class="sxs-lookup"><span data-stu-id="16b84-125">*ret*</span></span> | <span data-ttu-id="16b84-126">igual que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="16b84-126">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="16b84-127">**flot**</span><span class="sxs-lookup"><span data-stu-id="16b84-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="16b84-128">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="16b84-128">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="16b84-129">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="16b84-129">Minimum Shader Model</span></span>

<span data-ttu-id="16b84-130">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="16b84-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="16b84-131">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="16b84-131">Shader Model</span></span>                                                                       | <span data-ttu-id="16b84-132">Compatible</span><span class="sxs-lookup"><span data-stu-id="16b84-132">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="16b84-133">Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="16b84-133">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="16b84-134">sí</span><span class="sxs-lookup"><span data-stu-id="16b84-134">yes</span></span>                 |
| [<span data-ttu-id="16b84-135">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="16b84-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="16b84-136">sí ( \_ solo vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="16b84-136">yes (vs\_1\_1 only)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="16b84-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16b84-137">Requirements</span></span>



| <span data-ttu-id="16b84-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="16b84-138">Requirement</span></span> | <span data-ttu-id="16b84-139">Value</span><span class="sxs-lookup"><span data-stu-id="16b84-139">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="16b84-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="16b84-140">Header</span></span><br/> | <dl> <span data-ttu-id="16b84-141"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="16b84-141"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16b84-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="16b84-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16b84-143">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="16b84-143">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

