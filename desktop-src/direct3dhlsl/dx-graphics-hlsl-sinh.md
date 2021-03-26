---
title: sinh
description: Devuelve el seno hiperbólico del valor especificado.
ms.assetid: 8a9e11a3-582f-4680-a5bd-ecde90560db3
keywords:
- HLSL de SENOH
topic_type:
- apiref
api_name:
- sinh
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cbf6c5e04eb248c81782ba236010298ebb9564db
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078227"
---
# <a name="sinh"></a><span data-ttu-id="0974c-104">sinh</span><span class="sxs-lookup"><span data-stu-id="0974c-104">sinh</span></span>

<span data-ttu-id="0974c-105">Devuelve el seno hiperbólico del valor especificado.</span><span class="sxs-lookup"><span data-stu-id="0974c-105">Returns the hyperbolic sine of the specified value.</span></span>



| <span data-ttu-id="0974c-106">*RET* SENOH (*x*)</span><span class="sxs-lookup"><span data-stu-id="0974c-106">*ret* sinh(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="0974c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0974c-107">Parameters</span></span>



| <span data-ttu-id="0974c-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="0974c-108">Item</span></span>                                                   | <span data-ttu-id="0974c-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="0974c-109">Description</span></span>                                        |
|--------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="0974c-110"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="0974c-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="0974c-111">\[en \] el valor especificado, en radianes.</span><span class="sxs-lookup"><span data-stu-id="0974c-111">\[in\] The specified value, in radians.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="0974c-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0974c-112">Return Value</span></span>

<span data-ttu-id="0974c-113">Seno hiperbólico del parámetro *x* .</span><span class="sxs-lookup"><span data-stu-id="0974c-113">The hyperbolic sine of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="0974c-114">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="0974c-114">Type Description</span></span>



| <span data-ttu-id="0974c-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="0974c-115">Name</span></span>  | [<span data-ttu-id="0974c-116">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="0974c-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="0974c-117">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="0974c-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="0974c-118">Tamaño</span><span class="sxs-lookup"><span data-stu-id="0974c-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="0974c-119">*x*</span><span class="sxs-lookup"><span data-stu-id="0974c-119">*x*</span></span>   | <span data-ttu-id="0974c-120">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz**</span><span class="sxs-lookup"><span data-stu-id="0974c-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="0974c-121">**flot**</span><span class="sxs-lookup"><span data-stu-id="0974c-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="0974c-122">cualquiera</span><span class="sxs-lookup"><span data-stu-id="0974c-122">any</span></span>                            |
| <span data-ttu-id="0974c-123">*direcc*</span><span class="sxs-lookup"><span data-stu-id="0974c-123">*ret*</span></span> | <span data-ttu-id="0974c-124">igual que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="0974c-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="0974c-125">**flot**</span><span class="sxs-lookup"><span data-stu-id="0974c-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="0974c-126">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="0974c-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0974c-127">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="0974c-127">Minimum Shader Model</span></span>

<span data-ttu-id="0974c-128">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="0974c-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="0974c-129">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="0974c-129">Shader Model</span></span>                                                                       | <span data-ttu-id="0974c-130">Compatible</span><span class="sxs-lookup"><span data-stu-id="0974c-130">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="0974c-131">Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="0974c-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="0974c-132">sí</span><span class="sxs-lookup"><span data-stu-id="0974c-132">yes</span></span>                 |
| [<span data-ttu-id="0974c-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0974c-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="0974c-134">sí ( \_ solo vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="0974c-134">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="0974c-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="0974c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0974c-136">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="0974c-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

