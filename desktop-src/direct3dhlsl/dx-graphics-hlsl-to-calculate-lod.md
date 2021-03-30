---
title: CalculateLevelOfDetail (objeto de textura de HLSL de DirectX)
description: Calcula el nivel de detalle.
ms.assetid: 7c7c3754-45a9-49c6-8420-aac22f776b15
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c59b8da97ff1cbe0bd88d6a49120a0a040cf3c30
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "104984091"
---
# <a name="calculatelevelofdetail-directx-hlsl-texture-object"></a><span data-ttu-id="7156d-103">CalculateLevelOfDetail (objeto de textura de HLSL de DirectX)</span><span class="sxs-lookup"><span data-stu-id="7156d-103">CalculateLevelOfDetail (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="7156d-104">Calcula el nivel de detalle.</span><span class="sxs-lookup"><span data-stu-id="7156d-104">Calculates the level of detail.</span></span>



|                                                                 |
|-----------------------------------------------------------------|
| <span data-ttu-id="7156d-105">RET Object. CalculateLevelOfDetail ( \_ Estado de muestra S, Float x);</span><span class="sxs-lookup"><span data-stu-id="7156d-105">ret Object.CalculateLevelOfDetail( sampler\_state S, float x );</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="7156d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7156d-106">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7156d-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="7156d-107">Item</span></span></th>
<th><span data-ttu-id="7156d-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="7156d-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7156d-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Objeto</em></span><span class="sxs-lookup"><span data-stu-id="7156d-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="7156d-110">Cualquier tipo <a href="dx-graphics-hlsl-to-type.md">de objeto de textura</a> (excepto Texture2DMS y Texture2DMSArray).</span><span class="sxs-lookup"><span data-stu-id="7156d-110">Any <a href="dx-graphics-hlsl-to-type.md">texture-object</a> type (except Texture2DMS and Texture2DMSArray).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7156d-111"><span id="S"></span><span id="s"></span><em>Seg</em></span><span class="sxs-lookup"><span data-stu-id="7156d-111"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="7156d-112">de Un <a href="/windows/desktop/direct3d10/d3d10-effect-sampler-syntax">Estado de muestra</a>.</span><span class="sxs-lookup"><span data-stu-id="7156d-112">[in] A <a href="/windows/desktop/direct3d10/d3d10-effect-sampler-syntax">Sampler state</a>.</span></span> <span data-ttu-id="7156d-113">Se trata de un objeto declarado en un archivo de efectos que contiene las asignaciones de estado.</span><span class="sxs-lookup"><span data-stu-id="7156d-113">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7156d-114"><span id="x"></span><span id="X"></span><em>x1</em></span><span class="sxs-lookup"><span data-stu-id="7156d-114"><span id="x"></span><span id="X"></span><em>x</em></span></span><br/></td>
<td><span data-ttu-id="7156d-115">de Valor o valores de interpolación lineal, que es un número de punto flotante entre 0,0 y 1,0, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="7156d-115">[in] The linear interpolation value or values, which is a floating-point number between 0.0 and 1.0 inclusive.</span></span> <span data-ttu-id="7156d-116">El número de componentes depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="7156d-116">The number of components is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="7156d-117">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="7156d-117">Texture-Object Type</span></span></th>
<th><span data-ttu-id="7156d-118">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="7156d-118">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7156d-119">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="7156d-119">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="7156d-120">float1</span><span class="sxs-lookup"><span data-stu-id="7156d-120">float1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7156d-121">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="7156d-121">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="7156d-122">float2</span><span class="sxs-lookup"><span data-stu-id="7156d-122">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7156d-123">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="7156d-123">Texture3D, TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="7156d-124">float3</span><span class="sxs-lookup"><span data-stu-id="7156d-124">float3</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a><span data-ttu-id="7156d-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7156d-125">Return Value</span></span>

<span data-ttu-id="7156d-126">Devuelve el LOD calculado, un solo valor de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="7156d-126">Returns the calculated LOD, a single floating-point value.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="7156d-127">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="7156d-127">Minimum Shader Model</span></span>

<span data-ttu-id="7156d-128">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="7156d-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="7156d-129">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7156d-129">vs\_4\_0</span></span> | <span data-ttu-id="7156d-130">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="7156d-130">vs\_4\_1</span></span>  | <span data-ttu-id="7156d-131">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7156d-131">ps\_4\_0</span></span> | <span data-ttu-id="7156d-132">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="7156d-132">ps\_4\_1</span></span>  | <span data-ttu-id="7156d-133">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7156d-133">gs\_4\_0</span></span> | <span data-ttu-id="7156d-134">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="7156d-134">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
|          |           |          | <span data-ttu-id="7156d-135">x</span><span class="sxs-lookup"><span data-stu-id="7156d-135">x</span></span>         |          |           |



 

1.  <span data-ttu-id="7156d-136">TextureCubeArray está disponible en el modelo de sombreador 4,1 o superior.</span><span class="sxs-lookup"><span data-stu-id="7156d-136">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="7156d-137">El modelo de sombreador 4,1 está disponible en Direct3D 10,1 o superior.</span><span class="sxs-lookup"><span data-stu-id="7156d-137">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7156d-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7156d-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7156d-139">Texture-objeto</span><span class="sxs-lookup"><span data-stu-id="7156d-139">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

