---
title: tanh
description: Devuelve la tangente hiperbólica del valor especificado.
ms.assetid: e2d27aa0-5e03-4f2f-a29c-884711710c8d
keywords:
- HLSL de tanh
topic_type:
- apiref
api_name:
- tanh
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7c5312aaac6d6f164e940f99183e61688b393fbd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077948"
---
# <a name="tanh"></a><span data-ttu-id="edbac-104">tanh</span><span class="sxs-lookup"><span data-stu-id="edbac-104">tanh</span></span>

<span data-ttu-id="edbac-105">Devuelve la tangente hiperbólica del valor especificado.</span><span class="sxs-lookup"><span data-stu-id="edbac-105">Returns the hyperbolic tangent of the specified value.</span></span>



| <span data-ttu-id="edbac-106">*RET* tanh (*x*)</span><span class="sxs-lookup"><span data-stu-id="edbac-106">*ret* tanh(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="edbac-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="edbac-107">Parameters</span></span>



| <span data-ttu-id="edbac-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="edbac-108">Item</span></span>                                                   | <span data-ttu-id="edbac-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="edbac-109">Description</span></span>                                        |
|--------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="edbac-110"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="edbac-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="edbac-111">\[en \] el valor especificado, en radianes.</span><span class="sxs-lookup"><span data-stu-id="edbac-111">\[in\] The specified value, in radians.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="edbac-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="edbac-112">Return Value</span></span>

<span data-ttu-id="edbac-113">Tangente hiperbólica del parámetro *x* .</span><span class="sxs-lookup"><span data-stu-id="edbac-113">The hyperbolic tangent of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="edbac-114">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="edbac-114">Type Description</span></span>



| <span data-ttu-id="edbac-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="edbac-115">Name</span></span>  | [<span data-ttu-id="edbac-116">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="edbac-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="edbac-117">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="edbac-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="edbac-118">Tamaño</span><span class="sxs-lookup"><span data-stu-id="edbac-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="edbac-119">*x*</span><span class="sxs-lookup"><span data-stu-id="edbac-119">*x*</span></span>   | <span data-ttu-id="edbac-120">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz**</span><span class="sxs-lookup"><span data-stu-id="edbac-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="edbac-121">**flot**</span><span class="sxs-lookup"><span data-stu-id="edbac-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="edbac-122">cualquiera</span><span class="sxs-lookup"><span data-stu-id="edbac-122">any</span></span>                            |
| <span data-ttu-id="edbac-123">*direcc*</span><span class="sxs-lookup"><span data-stu-id="edbac-123">*ret*</span></span> | <span data-ttu-id="edbac-124">igual que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="edbac-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="edbac-125">**flot**</span><span class="sxs-lookup"><span data-stu-id="edbac-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="edbac-126">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="edbac-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="edbac-127">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="edbac-127">Minimum Shader Model</span></span>

<span data-ttu-id="edbac-128">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="edbac-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="edbac-129">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="edbac-129">Shader Model</span></span>                                                                       | <span data-ttu-id="edbac-130">Compatible</span><span class="sxs-lookup"><span data-stu-id="edbac-130">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="edbac-131">Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="edbac-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="edbac-132">sí</span><span class="sxs-lookup"><span data-stu-id="edbac-132">yes</span></span>                 |
| [<span data-ttu-id="edbac-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="edbac-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="edbac-134">sí ( \_ solo vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="edbac-134">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="edbac-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="edbac-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edbac-136">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="edbac-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

