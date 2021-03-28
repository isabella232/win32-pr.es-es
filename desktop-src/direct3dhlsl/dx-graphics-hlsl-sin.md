---
title: sin
description: Devuelve el seno del valor especificado.
ms.assetid: e1c3ead8-73dd-4798-8553-1a42dbaefe8e
keywords:
- sin HLSL
topic_type:
- apiref
api_name:
- sin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d48332d35052a893dcb348a70e4d464a6bbfe0c9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421258"
---
# <a name="sin"></a><span data-ttu-id="94080-104">sin</span><span class="sxs-lookup"><span data-stu-id="94080-104">sin</span></span>

<span data-ttu-id="94080-105">Devuelve el seno del valor especificado.</span><span class="sxs-lookup"><span data-stu-id="94080-105">Returns the sine of the specified value.</span></span>



| <span data-ttu-id="94080-106">*RET* sin (*x*)</span><span class="sxs-lookup"><span data-stu-id="94080-106">*ret* sin(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="94080-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="94080-107">Parameters</span></span>



| <span data-ttu-id="94080-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="94080-108">Item</span></span>                                                   | <span data-ttu-id="94080-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="94080-109">Description</span></span>                                        |
|--------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="94080-110"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="94080-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="94080-111">\[en \] el valor especificado, en radianes.</span><span class="sxs-lookup"><span data-stu-id="94080-111">\[in\] The specified value, in radians.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="94080-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="94080-112">Return Value</span></span>

<span data-ttu-id="94080-113">Seno del parámetro *x* .</span><span class="sxs-lookup"><span data-stu-id="94080-113">The sine of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="94080-114">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="94080-114">Type Description</span></span>



| <span data-ttu-id="94080-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="94080-115">Name</span></span>  | [<span data-ttu-id="94080-116">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="94080-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="94080-117">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="94080-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="94080-118">Tamaño</span><span class="sxs-lookup"><span data-stu-id="94080-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="94080-119">*x*</span><span class="sxs-lookup"><span data-stu-id="94080-119">*x*</span></span>   | <span data-ttu-id="94080-120">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz**</span><span class="sxs-lookup"><span data-stu-id="94080-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="94080-121">**flot**</span><span class="sxs-lookup"><span data-stu-id="94080-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="94080-122">cualquiera</span><span class="sxs-lookup"><span data-stu-id="94080-122">any</span></span>                            |
| <span data-ttu-id="94080-123">*direcc*</span><span class="sxs-lookup"><span data-stu-id="94080-123">*ret*</span></span> | <span data-ttu-id="94080-124">igual que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="94080-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="94080-125">**flot**</span><span class="sxs-lookup"><span data-stu-id="94080-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="94080-126">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="94080-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="94080-127">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="94080-127">Minimum Shader Model</span></span>

<span data-ttu-id="94080-128">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="94080-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="94080-129">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="94080-129">Shader Model</span></span>                                                                       | <span data-ttu-id="94080-130">Compatible</span><span class="sxs-lookup"><span data-stu-id="94080-130">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="94080-131">Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="94080-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="94080-132">sí</span><span class="sxs-lookup"><span data-stu-id="94080-132">yes</span></span>                 |
| [<span data-ttu-id="94080-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="94080-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="94080-134">sí ( \_ solo vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="94080-134">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="94080-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="94080-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94080-136">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="94080-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

