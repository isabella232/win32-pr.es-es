---
title: sqrt
description: Devuelve la raíz cuadrada del valor de punto flotante especificado por componente.
ms.assetid: e8debc60-1441-4974-9ab3-6d1c2217caaf
keywords:
- HLSL de raiz
topic_type:
- apiref
api_name:
- sqrt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ff3c872dac6da28a1ec92993e387bd23daec7f86
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420745"
---
# <a name="sqrt"></a><span data-ttu-id="0e645-104">sqrt</span><span class="sxs-lookup"><span data-stu-id="0e645-104">sqrt</span></span>

<span data-ttu-id="0e645-105">Devuelve la raíz cuadrada del valor de punto flotante especificado por componente.</span><span class="sxs-lookup"><span data-stu-id="0e645-105">Returns the square root of the specified floating-point value, per component.</span></span>



| <span data-ttu-id="0e645-106">*RET* sqrt (*x*)</span><span class="sxs-lookup"><span data-stu-id="0e645-106">*ret* sqrt(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="0e645-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0e645-107">Parameters</span></span>



| <span data-ttu-id="0e645-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="0e645-108">Item</span></span>                                                   | <span data-ttu-id="0e645-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="0e645-109">Description</span></span>                                           |
|--------------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="0e645-110"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="0e645-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="0e645-111">\[en \] el valor de punto flotante especificado.</span><span class="sxs-lookup"><span data-stu-id="0e645-111">\[in\] The specified floating-point value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="0e645-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0e645-112">Return Value</span></span>

<span data-ttu-id="0e645-113">Raíz cuadrada del parámetro *x* , por componente.</span><span class="sxs-lookup"><span data-stu-id="0e645-113">The square root of the *x* parameter, per component.</span></span>

## <a name="type-description"></a><span data-ttu-id="0e645-114">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="0e645-114">Type Description</span></span>



| <span data-ttu-id="0e645-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="0e645-115">Name</span></span>  | [<span data-ttu-id="0e645-116">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="0e645-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="0e645-117">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="0e645-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="0e645-118">Tamaño</span><span class="sxs-lookup"><span data-stu-id="0e645-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="0e645-119">*x*</span><span class="sxs-lookup"><span data-stu-id="0e645-119">*x*</span></span>   | <span data-ttu-id="0e645-120">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz**</span><span class="sxs-lookup"><span data-stu-id="0e645-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="0e645-121">**flot**</span><span class="sxs-lookup"><span data-stu-id="0e645-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="0e645-122">cualquiera</span><span class="sxs-lookup"><span data-stu-id="0e645-122">any</span></span>                            |
| <span data-ttu-id="0e645-123">*direcc*</span><span class="sxs-lookup"><span data-stu-id="0e645-123">*ret*</span></span> | <span data-ttu-id="0e645-124">igual que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="0e645-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="0e645-125">**flot**</span><span class="sxs-lookup"><span data-stu-id="0e645-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="0e645-126">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="0e645-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0e645-127">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="0e645-127">Minimum Shader Model</span></span>

<span data-ttu-id="0e645-128">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="0e645-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="0e645-129">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="0e645-129">Shader Model</span></span>                                                                       | <span data-ttu-id="0e645-130">Compatible</span><span class="sxs-lookup"><span data-stu-id="0e645-130">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="0e645-131">Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="0e645-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="0e645-132">sí</span><span class="sxs-lookup"><span data-stu-id="0e645-132">yes</span></span>                 |
| [<span data-ttu-id="0e645-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0e645-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="0e645-134">sí ( \_ solo vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="0e645-134">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="0e645-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="0e645-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e645-136">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="0e645-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

