---
title: asfloat
description: Interpreta el patrón de bits de x como un número de punto flotante.
ms.assetid: 48e1e0cb-8578-4e6d-8c46-2b8b201906c1
keywords:
- Interfloat HLSL
topic_type:
- apiref
api_name:
- asfloat
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a5701d959fb59519318dd7f2e91b6790f4c0b6e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997133"
---
# <a name="asfloat"></a><span data-ttu-id="a17cc-104">asfloat</span><span class="sxs-lookup"><span data-stu-id="a17cc-104">asfloat</span></span>

<span data-ttu-id="a17cc-105">Interpreta el patrón de bits de *x* como un número de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="a17cc-105">Interprets the bit pattern of *x* as a floating-point number.</span></span>



| <span data-ttu-id="a17cc-106">RET asfloat (*x*)</span><span class="sxs-lookup"><span data-stu-id="a17cc-106">ret asfloat(*x*)</span></span> |
|------------------|



 

## <a name="parameters"></a><span data-ttu-id="a17cc-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a17cc-107">Parameters</span></span>



| <span data-ttu-id="a17cc-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="a17cc-108">Item</span></span>                                                   | <span data-ttu-id="a17cc-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="a17cc-109">Description</span></span>                        |
|--------------------------------------------------------|------------------------------------|
| <span data-ttu-id="a17cc-110"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="a17cc-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="a17cc-111">\[en \] el valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="a17cc-111">\[in\] The input value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="a17cc-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a17cc-112">Return Value</span></span>

<span data-ttu-id="a17cc-113">La entrada se interpreta como un número de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="a17cc-113">The input interpreted as a floating-point number.</span></span>

## <a name="type-description"></a><span data-ttu-id="a17cc-114">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="a17cc-114">Type Description</span></span>



| <span data-ttu-id="a17cc-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="a17cc-115">Name</span></span>  | [<span data-ttu-id="a17cc-116">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="a17cc-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="a17cc-117">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="a17cc-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                         | <span data-ttu-id="a17cc-118">Tamaño</span><span class="sxs-lookup"><span data-stu-id="a17cc-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="a17cc-119">*x*</span><span class="sxs-lookup"><span data-stu-id="a17cc-119">*x*</span></span>   | <span data-ttu-id="a17cc-120">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz**</span><span class="sxs-lookup"><span data-stu-id="a17cc-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="a17cc-121">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**uint**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="a17cc-121">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**uint**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="a17cc-122">cualquiera</span><span class="sxs-lookup"><span data-stu-id="a17cc-122">any</span></span>                            |
| <span data-ttu-id="a17cc-123">*direcc*</span><span class="sxs-lookup"><span data-stu-id="a17cc-123">*ret*</span></span> | <span data-ttu-id="a17cc-124">igual que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="a17cc-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="a17cc-125">**flot**</span><span class="sxs-lookup"><span data-stu-id="a17cc-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                                                                                | <span data-ttu-id="a17cc-126">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="a17cc-126">same dimension(s) as input *x*</span></span> |



 

## <a name="function-overloads"></a><span data-ttu-id="a17cc-127">Sobrecargas de función</span><span class="sxs-lookup"><span data-stu-id="a17cc-127">Function Overloads</span></span>

<dl> <span data-ttu-id="a17cc-128">' Float <x> asfloat ( <x> valor float); `  
` Float <x> asfloat ( <x> valor int); `  
` Float <x> asfloat ( <x> valor uint); '</span><span class="sxs-lookup"><span data-stu-id="a17cc-128">`float<x> asfloat(float<x> value);`  
`float<x> asfloat(int<x> value);`  
`float<x> asfloat(uint<x> value);`</span></span>
</dl>

## <a name="minimum-shader-model"></a><span data-ttu-id="a17cc-129">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="a17cc-129">Minimum Shader Model</span></span>

<span data-ttu-id="a17cc-130">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="a17cc-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a17cc-131">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="a17cc-131">Shader Model</span></span>                                                        | <span data-ttu-id="a17cc-132">Compatible</span><span class="sxs-lookup"><span data-stu-id="a17cc-132">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="a17cc-133">Modelos de sombreador [modelo 4](dx-graphics-hlsl-sm4.md) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="a17cc-133">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="a17cc-134">sí</span><span class="sxs-lookup"><span data-stu-id="a17cc-134">yes</span></span>       |
| [<span data-ttu-id="a17cc-135">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a17cc-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)           | <span data-ttu-id="a17cc-136">no</span><span class="sxs-lookup"><span data-stu-id="a17cc-136">no</span></span>        |
| [<span data-ttu-id="a17cc-137">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a17cc-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)           | <span data-ttu-id="a17cc-138">no</span><span class="sxs-lookup"><span data-stu-id="a17cc-138">no</span></span>        |
| [<span data-ttu-id="a17cc-139">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a17cc-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)           | <span data-ttu-id="a17cc-140">no</span><span class="sxs-lookup"><span data-stu-id="a17cc-140">no</span></span>        |



 

## <a name="remarks"></a><span data-ttu-id="a17cc-141">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a17cc-141">Remarks</span></span>

<span data-ttu-id="a17cc-142">Los compiladores anteriores permitieron incorrectamente `asfloat(bool)` , pero tenga en cuenta que no se admiten las entradas bool.</span><span class="sxs-lookup"><span data-stu-id="a17cc-142">Older compilers incorrectly allowed `asfloat(bool)`, but note that bool inputs are not supported.</span></span>

## <a name="see-also"></a><span data-ttu-id="a17cc-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="a17cc-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a17cc-144">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="a17cc-144">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

