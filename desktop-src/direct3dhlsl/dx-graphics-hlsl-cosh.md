---
title: cosh
description: Devuelve el coseno hiperbólico del valor especificado.
ms.assetid: ed68c461-de91-4ce4-a424-8ab28ee43f23
keywords:
- un HLSL de cosh
topic_type:
- apiref
api_name:
- cosh
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3bd6cad2b79e849d8f20bbaf5baa6cfc7db0b702
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997160"
---
# <a name="cosh"></a><span data-ttu-id="53f79-104">cosh</span><span class="sxs-lookup"><span data-stu-id="53f79-104">cosh</span></span>

<span data-ttu-id="53f79-105">Devuelve el coseno hiperbólico del valor especificado.</span><span class="sxs-lookup"><span data-stu-id="53f79-105">Returns the hyperbolic cosine of the specified value.</span></span>



| <span data-ttu-id="53f79-106">*RET* cosh (*x*)</span><span class="sxs-lookup"><span data-stu-id="53f79-106">*ret* cosh(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="53f79-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="53f79-107">Parameters</span></span>



| <span data-ttu-id="53f79-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="53f79-108">Item</span></span>                                                   | <span data-ttu-id="53f79-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="53f79-109">Description</span></span>                                        |
|--------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="53f79-110"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="53f79-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="53f79-111">\[en \] el valor especificado, en radianes.</span><span class="sxs-lookup"><span data-stu-id="53f79-111">\[in\] The specified value, in radians.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="53f79-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="53f79-112">Return Value</span></span>

<span data-ttu-id="53f79-113">Coseno hiperbólico del parámetro *x* .</span><span class="sxs-lookup"><span data-stu-id="53f79-113">The hyperbolic cosine of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="53f79-114">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="53f79-114">Type Description</span></span>



| <span data-ttu-id="53f79-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="53f79-115">Name</span></span>  | [<span data-ttu-id="53f79-116">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="53f79-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="53f79-117">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="53f79-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="53f79-118">Tamaño</span><span class="sxs-lookup"><span data-stu-id="53f79-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="53f79-119">*x*</span><span class="sxs-lookup"><span data-stu-id="53f79-119">*x*</span></span>   | <span data-ttu-id="53f79-120">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz**</span><span class="sxs-lookup"><span data-stu-id="53f79-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="53f79-121">**flot**</span><span class="sxs-lookup"><span data-stu-id="53f79-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="53f79-122">cualquiera</span><span class="sxs-lookup"><span data-stu-id="53f79-122">any</span></span>                            |
| <span data-ttu-id="53f79-123">*direcc*</span><span class="sxs-lookup"><span data-stu-id="53f79-123">*ret*</span></span> | <span data-ttu-id="53f79-124">igual que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="53f79-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="53f79-125">**flot**</span><span class="sxs-lookup"><span data-stu-id="53f79-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="53f79-126">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="53f79-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="53f79-127">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="53f79-127">Minimum Shader Model</span></span>

<span data-ttu-id="53f79-128">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="53f79-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="53f79-129">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="53f79-129">Shader Model</span></span>                                                                       | <span data-ttu-id="53f79-130">Compatible</span><span class="sxs-lookup"><span data-stu-id="53f79-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="53f79-131">Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="53f79-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="53f79-132">sí</span><span class="sxs-lookup"><span data-stu-id="53f79-132">yes</span></span>       |
| [<span data-ttu-id="53f79-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="53f79-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="53f79-134">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="53f79-134">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="53f79-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="53f79-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53f79-136">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="53f79-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

