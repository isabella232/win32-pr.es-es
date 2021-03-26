---
title: acos
description: Devuelve el arcocoseno del valor especificado.
ms.assetid: c9bc33b8-d586-4c64-9453-5ab97396f2cf
keywords:
- HLSL de ACOS
topic_type:
- apiref
api_name:
- acos
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2cd909c4a4c1300374bba723f1edabb48d51b2e0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149578"
---
# <a name="acos"></a><span data-ttu-id="0b9bf-104">acos</span><span class="sxs-lookup"><span data-stu-id="0b9bf-104">acos</span></span>

<span data-ttu-id="0b9bf-105">Devuelve el arcocoseno del valor especificado.</span><span class="sxs-lookup"><span data-stu-id="0b9bf-105">Returns the arccosine of the specified value.</span></span>



| <span data-ttu-id="0b9bf-106">*RET* ACOS (*x*)</span><span class="sxs-lookup"><span data-stu-id="0b9bf-106">*ret* acos(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="0b9bf-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0b9bf-107">Parameters</span></span>



| <span data-ttu-id="0b9bf-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="0b9bf-108">Item</span></span>                                                   | <span data-ttu-id="0b9bf-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="0b9bf-109">Description</span></span>                                                                                                         |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b9bf-110"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="0b9bf-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="0b9bf-111">\[en \] el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="0b9bf-111">\[in\] The specified value.</span></span> <span data-ttu-id="0b9bf-112">Cada componente debe ser un valor de punto flotante en el intervalo de-1 a 1.</span><span class="sxs-lookup"><span data-stu-id="0b9bf-112">Each component should be a floating-point value within the range of -1 to 1.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="0b9bf-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0b9bf-113">Return Value</span></span>

<span data-ttu-id="0b9bf-114">Arcocoseno del parámetro *x* .</span><span class="sxs-lookup"><span data-stu-id="0b9bf-114">The arccosine of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="0b9bf-115">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="0b9bf-115">Type Description</span></span>



| <span data-ttu-id="0b9bf-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="0b9bf-116">Name</span></span>  | [<span data-ttu-id="0b9bf-117">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="0b9bf-117">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="0b9bf-118">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="0b9bf-118">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="0b9bf-119">Tamaño</span><span class="sxs-lookup"><span data-stu-id="0b9bf-119">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="0b9bf-120">*x*</span><span class="sxs-lookup"><span data-stu-id="0b9bf-120">*x*</span></span>   | <span data-ttu-id="0b9bf-121">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz**</span><span class="sxs-lookup"><span data-stu-id="0b9bf-121">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="0b9bf-122">**flot**</span><span class="sxs-lookup"><span data-stu-id="0b9bf-122">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="0b9bf-123">cualquiera</span><span class="sxs-lookup"><span data-stu-id="0b9bf-123">any</span></span>                            |
| <span data-ttu-id="0b9bf-124">*direcc*</span><span class="sxs-lookup"><span data-stu-id="0b9bf-124">*ret*</span></span> | <span data-ttu-id="0b9bf-125">igual que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="0b9bf-125">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="0b9bf-126">**flot**</span><span class="sxs-lookup"><span data-stu-id="0b9bf-126">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="0b9bf-127">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="0b9bf-127">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0b9bf-128">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="0b9bf-128">Minimum Shader Model</span></span>

<span data-ttu-id="0b9bf-129">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="0b9bf-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="0b9bf-130">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="0b9bf-130">Shader Model</span></span>                                                                       | <span data-ttu-id="0b9bf-131">Compatible</span><span class="sxs-lookup"><span data-stu-id="0b9bf-131">Supported</span></span>     |
|------------------------------------------------------------------------------------|---------------|
| <span data-ttu-id="0b9bf-132">Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="0b9bf-132">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="0b9bf-133">sí</span><span class="sxs-lookup"><span data-stu-id="0b9bf-133">yes</span></span>           |
| [<span data-ttu-id="0b9bf-134">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0b9bf-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="0b9bf-135">\_solo vs 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="0b9bf-135">vs\_1\_1 only</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="0b9bf-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b9bf-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b9bf-137">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="0b9bf-137">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

