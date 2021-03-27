---
title: tan
description: Devuelve la tangente del valor especificado.
ms.assetid: ca03b184-9e1a-4152-9292-f8af38aa9423
keywords:
- HLSL tan
topic_type:
- apiref
api_name:
- tan
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cf9451a2bf1a5759470e87343f1b4a15583b470a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792304"
---
# <a name="tan"></a><span data-ttu-id="bcec8-104">tan</span><span class="sxs-lookup"><span data-stu-id="bcec8-104">tan</span></span>

<span data-ttu-id="bcec8-105">Devuelve la tangente del valor especificado.</span><span class="sxs-lookup"><span data-stu-id="bcec8-105">Returns the tangent of the specified value.</span></span>



| <span data-ttu-id="bcec8-106">*RET* tan (*x*)</span><span class="sxs-lookup"><span data-stu-id="bcec8-106">*ret* tan(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="bcec8-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bcec8-107">Parameters</span></span>



| <span data-ttu-id="bcec8-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="bcec8-108">Item</span></span>                                                   | <span data-ttu-id="bcec8-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="bcec8-109">Description</span></span>                                        |
|--------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="bcec8-110"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="bcec8-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="bcec8-111">\[en \] el valor especificado, en radianes.</span><span class="sxs-lookup"><span data-stu-id="bcec8-111">\[in\] The specified value, in radians.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="bcec8-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bcec8-112">Return Value</span></span>

<span data-ttu-id="bcec8-113">Tangente del parámetro *x* .</span><span class="sxs-lookup"><span data-stu-id="bcec8-113">The tangent of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="bcec8-114">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="bcec8-114">Type Description</span></span>



| <span data-ttu-id="bcec8-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="bcec8-115">Name</span></span>  | [<span data-ttu-id="bcec8-116">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="bcec8-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="bcec8-117">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="bcec8-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="bcec8-118">Tamaño</span><span class="sxs-lookup"><span data-stu-id="bcec8-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="bcec8-119">*x*</span><span class="sxs-lookup"><span data-stu-id="bcec8-119">*x*</span></span>   | <span data-ttu-id="bcec8-120">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz**</span><span class="sxs-lookup"><span data-stu-id="bcec8-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="bcec8-121">**flot**</span><span class="sxs-lookup"><span data-stu-id="bcec8-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="bcec8-122">cualquiera</span><span class="sxs-lookup"><span data-stu-id="bcec8-122">any</span></span>                            |
| <span data-ttu-id="bcec8-123">*direcc*</span><span class="sxs-lookup"><span data-stu-id="bcec8-123">*ret*</span></span> | <span data-ttu-id="bcec8-124">igual que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="bcec8-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="bcec8-125">**flot**</span><span class="sxs-lookup"><span data-stu-id="bcec8-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="bcec8-126">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="bcec8-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="bcec8-127">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="bcec8-127">Minimum Shader Model</span></span>

<span data-ttu-id="bcec8-128">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="bcec8-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="bcec8-129">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="bcec8-129">Shader Model</span></span>                                                                       | <span data-ttu-id="bcec8-130">Compatible</span><span class="sxs-lookup"><span data-stu-id="bcec8-130">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="bcec8-131">Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="bcec8-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="bcec8-132">sí</span><span class="sxs-lookup"><span data-stu-id="bcec8-132">yes</span></span>                 |
| [<span data-ttu-id="bcec8-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bcec8-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="bcec8-134">sí ( \_ solo vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="bcec8-134">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="bcec8-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="bcec8-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcec8-136">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="bcec8-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

