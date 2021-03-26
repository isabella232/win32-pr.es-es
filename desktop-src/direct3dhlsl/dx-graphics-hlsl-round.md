---
title: Round (Corecrt \_ Math. h)
description: Redondea el valor especificado al entero más próximo.
ms.assetid: 258ce717-dca1-4ed2-ad98-1ecfdb58f939
keywords:
- Round-HLSL
topic_type:
- apiref
api_name:
- round
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f00bf845dfe16a92729b523fba62f6fd6dcde2b5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003858"
---
# <a name="round"></a><span data-ttu-id="93f85-104">round</span><span class="sxs-lookup"><span data-stu-id="93f85-104">round</span></span>

<span data-ttu-id="93f85-105">Redondea el valor especificado al entero más próximo.</span><span class="sxs-lookup"><span data-stu-id="93f85-105">Rounds the specified value to the nearest integer.</span></span> <span data-ttu-id="93f85-106">Los casos de medio ciclo se redondean a los pares más cercanos.</span><span class="sxs-lookup"><span data-stu-id="93f85-106">Halfway cases are rounded to the nearest even.</span></span>



| <span data-ttu-id="93f85-107">*RET* Round (*x*)</span><span class="sxs-lookup"><span data-stu-id="93f85-107">*ret* round(*x*)</span></span> |
|------------------|



 

## <a name="parameters"></a><span data-ttu-id="93f85-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="93f85-108">Parameters</span></span>



| <span data-ttu-id="93f85-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="93f85-109">Item</span></span>                                                   | <span data-ttu-id="93f85-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="93f85-110">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="93f85-111"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="93f85-111"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="93f85-112">\[en \] el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="93f85-112">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="93f85-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="93f85-113">Return Value</span></span>

<span data-ttu-id="93f85-114">Parámetro *x* , redondeado al entero más próximo dentro de un tipo de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="93f85-114">The *x* parameter, rounded to the nearest integer within a floating-point type.</span></span>

## <a name="type-description"></a><span data-ttu-id="93f85-115">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="93f85-115">Type Description</span></span>



| <span data-ttu-id="93f85-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="93f85-116">Name</span></span>  | [<span data-ttu-id="93f85-117">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="93f85-117">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="93f85-118">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="93f85-118">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="93f85-119">Tamaño</span><span class="sxs-lookup"><span data-stu-id="93f85-119">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="93f85-120">*x*</span><span class="sxs-lookup"><span data-stu-id="93f85-120">*x*</span></span>   | <span data-ttu-id="93f85-121">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz**</span><span class="sxs-lookup"><span data-stu-id="93f85-121">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="93f85-122">**flot**</span><span class="sxs-lookup"><span data-stu-id="93f85-122">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="93f85-123">cualquiera</span><span class="sxs-lookup"><span data-stu-id="93f85-123">any</span></span>                            |
| <span data-ttu-id="93f85-124">*direcc*</span><span class="sxs-lookup"><span data-stu-id="93f85-124">*ret*</span></span> | <span data-ttu-id="93f85-125">igual que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="93f85-125">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="93f85-126">**flot**</span><span class="sxs-lookup"><span data-stu-id="93f85-126">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="93f85-127">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="93f85-127">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="93f85-128">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="93f85-128">Minimum Shader Model</span></span>

<span data-ttu-id="93f85-129">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="93f85-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="93f85-130">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="93f85-130">Shader Model</span></span>                                                                       | <span data-ttu-id="93f85-131">Compatible</span><span class="sxs-lookup"><span data-stu-id="93f85-131">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="93f85-132">Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="93f85-132">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="93f85-133">sí</span><span class="sxs-lookup"><span data-stu-id="93f85-133">yes</span></span>                 |
| [<span data-ttu-id="93f85-134">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="93f85-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="93f85-135">sí ( \_ solo vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="93f85-135">yes (vs\_1\_1 only)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="93f85-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93f85-136">Requirements</span></span>



| <span data-ttu-id="93f85-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="93f85-137">Requirement</span></span> | <span data-ttu-id="93f85-138">Value</span><span class="sxs-lookup"><span data-stu-id="93f85-138">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="93f85-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="93f85-139">Header</span></span><br/> | <dl> <span data-ttu-id="93f85-140"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="93f85-140"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93f85-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="93f85-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93f85-142">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="93f85-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

