---
title: saturación (referencia de HLSL)
description: Fija el valor especificado en el intervalo de 0 a 1.
ms.assetid: efe4dedd-732a-4643-8a57-61814434f6ff
keywords:
- saturar HLSL
topic_type:
- apiref
api_name:
- saturate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 609443bdc1d0cff6a4c81c8eb26d86a30ea1e721
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104358991"
---
# <a name="saturate-hlsl-reference"></a><span data-ttu-id="0fdc7-104">saturación (referencia de HLSL)</span><span class="sxs-lookup"><span data-stu-id="0fdc7-104">saturate (HLSL reference)</span></span>

<span data-ttu-id="0fdc7-105">Fija el valor especificado en el intervalo de 0 a 1.</span><span class="sxs-lookup"><span data-stu-id="0fdc7-105">Clamps the specified value within the range of 0 to 1.</span></span>



| <span data-ttu-id="0fdc7-106">*RET* saturada (*x*)</span><span class="sxs-lookup"><span data-stu-id="0fdc7-106">*ret* saturate(*x*)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="0fdc7-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0fdc7-107">Parameters</span></span>



| <span data-ttu-id="0fdc7-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="0fdc7-108">Item</span></span>                                                   | <span data-ttu-id="0fdc7-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="0fdc7-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="0fdc7-110"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="0fdc7-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="0fdc7-111">\[en \] el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="0fdc7-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="0fdc7-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0fdc7-112">Return Value</span></span>

<span data-ttu-id="0fdc7-113">Parámetro *x* , fijado en el intervalo de 0 a 1.</span><span class="sxs-lookup"><span data-stu-id="0fdc7-113">The *x* parameter, clamped within the range of 0 to 1.</span></span>

## <a name="type-description"></a><span data-ttu-id="0fdc7-114">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="0fdc7-114">Type Description</span></span>



| <span data-ttu-id="0fdc7-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="0fdc7-115">Name</span></span>  | [<span data-ttu-id="0fdc7-116">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="0fdc7-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="0fdc7-117">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="0fdc7-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="0fdc7-118">Tamaño</span><span class="sxs-lookup"><span data-stu-id="0fdc7-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="0fdc7-119">*x*</span><span class="sxs-lookup"><span data-stu-id="0fdc7-119">*x*</span></span>   | <span data-ttu-id="0fdc7-120">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz**</span><span class="sxs-lookup"><span data-stu-id="0fdc7-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="0fdc7-121">**flot**</span><span class="sxs-lookup"><span data-stu-id="0fdc7-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="0fdc7-122">cualquiera</span><span class="sxs-lookup"><span data-stu-id="0fdc7-122">any</span></span>                            |
| <span data-ttu-id="0fdc7-123">*direcc*</span><span class="sxs-lookup"><span data-stu-id="0fdc7-123">*ret*</span></span> | <span data-ttu-id="0fdc7-124">igual que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="0fdc7-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="0fdc7-125">**flot**</span><span class="sxs-lookup"><span data-stu-id="0fdc7-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="0fdc7-126">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="0fdc7-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0fdc7-127">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="0fdc7-127">Minimum Shader Model</span></span>

<span data-ttu-id="0fdc7-128">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="0fdc7-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="0fdc7-129">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="0fdc7-129">Shader Model</span></span>                                                                       | <span data-ttu-id="0fdc7-130">Compatible</span><span class="sxs-lookup"><span data-stu-id="0fdc7-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="0fdc7-131">Modelador [modelo 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="0fdc7-131">[Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) and higher shader models</span></span> | <span data-ttu-id="0fdc7-132">sí</span><span class="sxs-lookup"><span data-stu-id="0fdc7-132">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="0fdc7-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="0fdc7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fdc7-134">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="0fdc7-134">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

