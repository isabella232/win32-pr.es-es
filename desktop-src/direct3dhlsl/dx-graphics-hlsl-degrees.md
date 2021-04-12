---
title: grados
description: Convierte el valor especificado de radianes en grados.
ms.assetid: e60a3ec4-9177-457a-8314-a5788f353633
keywords:
- HLSL de grados
topic_type:
- apiref
api_name:
- degrees
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 47d8bba0ee43da81a18baaeaffca0e3c917e460d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420904"
---
# <a name="degrees"></a><span data-ttu-id="2ec04-104">grados</span><span class="sxs-lookup"><span data-stu-id="2ec04-104">degrees</span></span>

<span data-ttu-id="2ec04-105">Convierte el valor especificado de radianes en grados.</span><span class="sxs-lookup"><span data-stu-id="2ec04-105">Converts the specified value from radians to degrees.</span></span>



| <span data-ttu-id="2ec04-106">grados *RET* (*x*)</span><span class="sxs-lookup"><span data-stu-id="2ec04-106">*ret* degrees(*x*)</span></span> |
|--------------------|



 

## <a name="parameters"></a><span data-ttu-id="2ec04-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2ec04-107">Parameters</span></span>



| <span data-ttu-id="2ec04-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="2ec04-108">Item</span></span>                                                   | <span data-ttu-id="2ec04-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="2ec04-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="2ec04-110"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="2ec04-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="2ec04-111">\[en \] el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="2ec04-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="2ec04-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2ec04-112">Return Value</span></span>

<span data-ttu-id="2ec04-113">Resultado de convertir el parámetro *x* de radianes en grados.</span><span class="sxs-lookup"><span data-stu-id="2ec04-113">The result of converting the *x* parameter from radians to degrees.</span></span>

## <a name="type-description"></a><span data-ttu-id="2ec04-114">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="2ec04-114">Type Description</span></span>



| <span data-ttu-id="2ec04-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="2ec04-115">Name</span></span>  | [<span data-ttu-id="2ec04-116">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="2ec04-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="2ec04-117">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="2ec04-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="2ec04-118">Tamaño</span><span class="sxs-lookup"><span data-stu-id="2ec04-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="2ec04-119">*x*</span><span class="sxs-lookup"><span data-stu-id="2ec04-119">*x*</span></span>   | <span data-ttu-id="2ec04-120">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz**</span><span class="sxs-lookup"><span data-stu-id="2ec04-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="2ec04-121">**flot**</span><span class="sxs-lookup"><span data-stu-id="2ec04-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="2ec04-122">cualquiera</span><span class="sxs-lookup"><span data-stu-id="2ec04-122">any</span></span>                            |
| <span data-ttu-id="2ec04-123">*direcc*</span><span class="sxs-lookup"><span data-stu-id="2ec04-123">*ret*</span></span> | <span data-ttu-id="2ec04-124">igual que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="2ec04-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="2ec04-125">**flot**</span><span class="sxs-lookup"><span data-stu-id="2ec04-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="2ec04-126">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="2ec04-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2ec04-127">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="2ec04-127">Minimum Shader Model</span></span>

<span data-ttu-id="2ec04-128">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="2ec04-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2ec04-129">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="2ec04-129">Shader Model</span></span>                                                                       | <span data-ttu-id="2ec04-130">Compatible</span><span class="sxs-lookup"><span data-stu-id="2ec04-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="2ec04-131">Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="2ec04-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="2ec04-132">sí</span><span class="sxs-lookup"><span data-stu-id="2ec04-132">yes</span></span>       |
| [<span data-ttu-id="2ec04-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2ec04-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="2ec04-134">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="2ec04-134">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="2ec04-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="2ec04-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ec04-136">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="2ec04-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

