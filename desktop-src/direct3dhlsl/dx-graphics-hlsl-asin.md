---
title: asin
description: Devuelve el arcoseno del valor especificado.
ms.assetid: 49559cb2-3305-4c97-8071-1589bcca3a75
keywords:
- Asin HLSL
topic_type:
- apiref
api_name:
- asin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a2f64865cb3172037f6630dc422a69aa4d135b1d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078308"
---
# <a name="asin"></a><span data-ttu-id="935a0-104">asin</span><span class="sxs-lookup"><span data-stu-id="935a0-104">asin</span></span>

<span data-ttu-id="935a0-105">Devuelve el arcoseno del valor especificado.</span><span class="sxs-lookup"><span data-stu-id="935a0-105">Returns the arcsine of the specified value.</span></span>



| <span data-ttu-id="935a0-106">*RET* Asin (*x*)</span><span class="sxs-lookup"><span data-stu-id="935a0-106">*ret* asin(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="935a0-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="935a0-107">Parameters</span></span>



| <span data-ttu-id="935a0-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="935a0-108">Item</span></span>                                                   | <span data-ttu-id="935a0-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="935a0-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="935a0-110"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="935a0-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="935a0-111">\[en \] el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="935a0-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="935a0-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="935a0-112">Return Value</span></span>

<span data-ttu-id="935a0-113">Arcoseno del parámetro *x* .</span><span class="sxs-lookup"><span data-stu-id="935a0-113">The arcsine of the *x* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="935a0-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="935a0-114">Remarks</span></span>

<span data-ttu-id="935a0-115">Cada componente del parámetro *x* debe estar en el intervalo de-π/2 a π/2.</span><span class="sxs-lookup"><span data-stu-id="935a0-115">Each component of the *x* parameter should be within the range of -π/2 to π/2.</span></span>

## <a name="type-description"></a><span data-ttu-id="935a0-116">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="935a0-116">Type Description</span></span>



| <span data-ttu-id="935a0-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="935a0-117">Name</span></span>  | [<span data-ttu-id="935a0-118">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="935a0-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="935a0-119">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="935a0-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="935a0-120">Tamaño</span><span class="sxs-lookup"><span data-stu-id="935a0-120">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="935a0-121">*x*</span><span class="sxs-lookup"><span data-stu-id="935a0-121">*x*</span></span>   | <span data-ttu-id="935a0-122">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz**</span><span class="sxs-lookup"><span data-stu-id="935a0-122">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="935a0-123">**flot**</span><span class="sxs-lookup"><span data-stu-id="935a0-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="935a0-124">cualquiera</span><span class="sxs-lookup"><span data-stu-id="935a0-124">any</span></span>                            |
| <span data-ttu-id="935a0-125">*direcc*</span><span class="sxs-lookup"><span data-stu-id="935a0-125">*ret*</span></span> | <span data-ttu-id="935a0-126">igual que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="935a0-126">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="935a0-127">**flot**</span><span class="sxs-lookup"><span data-stu-id="935a0-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="935a0-128">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="935a0-128">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="935a0-129">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="935a0-129">Minimum Shader Model</span></span>

<span data-ttu-id="935a0-130">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="935a0-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="935a0-131">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="935a0-131">Shader Model</span></span>                                                                       | <span data-ttu-id="935a0-132">Compatible</span><span class="sxs-lookup"><span data-stu-id="935a0-132">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="935a0-133">Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="935a0-133">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="935a0-134">sí</span><span class="sxs-lookup"><span data-stu-id="935a0-134">yes</span></span>       |
| [<span data-ttu-id="935a0-135">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="935a0-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="935a0-136">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="935a0-136">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="935a0-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="935a0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="935a0-138">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="935a0-138">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

