---
title: cos
description: Devuelve el coseno del valor especificado.
ms.assetid: 96c15702-98be-45bc-9abc-60ccc3c217b6
keywords:
- HLSL de cos
topic_type:
- apiref
api_name:
- cos
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4f5c0f4f071d47102c673301a397bfe3ecf178e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421359"
---
# <a name="cos"></a><span data-ttu-id="d786c-104">cos</span><span class="sxs-lookup"><span data-stu-id="d786c-104">cos</span></span>

<span data-ttu-id="d786c-105">Devuelve el coseno del valor especificado.</span><span class="sxs-lookup"><span data-stu-id="d786c-105">Returns the cosine of the specified value.</span></span>



| <span data-ttu-id="d786c-106">*rec* (*x*)</span><span class="sxs-lookup"><span data-stu-id="d786c-106">*ret* cos(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="d786c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d786c-107">Parameters</span></span>



| <span data-ttu-id="d786c-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="d786c-108">Item</span></span>                                                   | <span data-ttu-id="d786c-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="d786c-109">Description</span></span>                                        |
|--------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="d786c-110"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="d786c-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="d786c-111">\[en \] el valor especificado, en radianes.</span><span class="sxs-lookup"><span data-stu-id="d786c-111">\[in\] The specified value, in radians.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="d786c-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d786c-112">Return Value</span></span>

<span data-ttu-id="d786c-113">Coseno del parámetro *x* .</span><span class="sxs-lookup"><span data-stu-id="d786c-113">The cosine of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="d786c-114">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="d786c-114">Type Description</span></span>



| <span data-ttu-id="d786c-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="d786c-115">Name</span></span>  | [<span data-ttu-id="d786c-116">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="d786c-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="d786c-117">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="d786c-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="d786c-118">Tamaño</span><span class="sxs-lookup"><span data-stu-id="d786c-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="d786c-119">*x*</span><span class="sxs-lookup"><span data-stu-id="d786c-119">*x*</span></span>   | <span data-ttu-id="d786c-120">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz**</span><span class="sxs-lookup"><span data-stu-id="d786c-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="d786c-121">**flot**</span><span class="sxs-lookup"><span data-stu-id="d786c-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d786c-122">cualquiera</span><span class="sxs-lookup"><span data-stu-id="d786c-122">any</span></span>                            |
| <span data-ttu-id="d786c-123">*direcc*</span><span class="sxs-lookup"><span data-stu-id="d786c-123">*ret*</span></span> | <span data-ttu-id="d786c-124">igual que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="d786c-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="d786c-125">**flot**</span><span class="sxs-lookup"><span data-stu-id="d786c-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d786c-126">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="d786c-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d786c-127">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="d786c-127">Minimum Shader Model</span></span>

<span data-ttu-id="d786c-128">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="d786c-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d786c-129">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="d786c-129">Shader Model</span></span>                                                                       | <span data-ttu-id="d786c-130">Compatible</span><span class="sxs-lookup"><span data-stu-id="d786c-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="d786c-131">Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="d786c-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="d786c-132">sí</span><span class="sxs-lookup"><span data-stu-id="d786c-132">yes</span></span>       |
| [<span data-ttu-id="d786c-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d786c-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="d786c-134">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="d786c-134">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="d786c-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="d786c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d786c-136">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="d786c-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

