---
title: atan
description: Devuelve el arcotangente del valor especificado.
ms.assetid: e3ce3ac3-1012-414f-a193-102208083e39
keywords:
- HLSL de atan
topic_type:
- apiref
api_name:
- atan
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 290ced1e5100e3bbc780fab6ab984deaca38528f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792051"
---
# <a name="atan"></a><span data-ttu-id="2bb8d-104">atan</span><span class="sxs-lookup"><span data-stu-id="2bb8d-104">atan</span></span>

<span data-ttu-id="2bb8d-105">Devuelve el arcotangente del valor especificado.</span><span class="sxs-lookup"><span data-stu-id="2bb8d-105">Returns the arctangent of the specified value.</span></span>



| <span data-ttu-id="2bb8d-106">*RET* atan (*x*)</span><span class="sxs-lookup"><span data-stu-id="2bb8d-106">*ret* atan(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="2bb8d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2bb8d-107">Parameters</span></span>



| <span data-ttu-id="2bb8d-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="2bb8d-108">Item</span></span>                                                   | <span data-ttu-id="2bb8d-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="2bb8d-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="2bb8d-110"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="2bb8d-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="2bb8d-111">\[en \] el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="2bb8d-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="2bb8d-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2bb8d-112">Return Value</span></span>

<span data-ttu-id="2bb8d-113">Arco tangente del parámetro *x* .</span><span class="sxs-lookup"><span data-stu-id="2bb8d-113">The arctangent of the *x* parameter.</span></span> <span data-ttu-id="2bb8d-114">Este valor está dentro del intervalo de-π/2 a π/2.</span><span class="sxs-lookup"><span data-stu-id="2bb8d-114">This value is within the range of -π/2 to π/2.</span></span>

## <a name="type-description"></a><span data-ttu-id="2bb8d-115">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="2bb8d-115">Type Description</span></span>



| <span data-ttu-id="2bb8d-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="2bb8d-116">Name</span></span>  | [<span data-ttu-id="2bb8d-117">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="2bb8d-117">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="2bb8d-118">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="2bb8d-118">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="2bb8d-119">Tamaño</span><span class="sxs-lookup"><span data-stu-id="2bb8d-119">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="2bb8d-120">*x*</span><span class="sxs-lookup"><span data-stu-id="2bb8d-120">*x*</span></span>   | <span data-ttu-id="2bb8d-121">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz**</span><span class="sxs-lookup"><span data-stu-id="2bb8d-121">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="2bb8d-122">**flot**</span><span class="sxs-lookup"><span data-stu-id="2bb8d-122">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="2bb8d-123">cualquiera</span><span class="sxs-lookup"><span data-stu-id="2bb8d-123">any</span></span>                            |
| <span data-ttu-id="2bb8d-124">*direcc*</span><span class="sxs-lookup"><span data-stu-id="2bb8d-124">*ret*</span></span> | <span data-ttu-id="2bb8d-125">igual que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="2bb8d-125">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="2bb8d-126">**flot**</span><span class="sxs-lookup"><span data-stu-id="2bb8d-126">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="2bb8d-127">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="2bb8d-127">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2bb8d-128">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="2bb8d-128">Minimum Shader Model</span></span>

<span data-ttu-id="2bb8d-129">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="2bb8d-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2bb8d-130">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="2bb8d-130">Shader Model</span></span>                                                                       | <span data-ttu-id="2bb8d-131">Compatible</span><span class="sxs-lookup"><span data-stu-id="2bb8d-131">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="2bb8d-132">Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="2bb8d-132">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="2bb8d-133">sí</span><span class="sxs-lookup"><span data-stu-id="2bb8d-133">yes</span></span>       |
| [<span data-ttu-id="2bb8d-134">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2bb8d-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="2bb8d-135">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="2bb8d-135">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="2bb8d-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="2bb8d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bb8d-137">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="2bb8d-137">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

