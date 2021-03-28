---
title: InputPatch
description: Representa una matriz de puntos de control que están disponibles para el sombreador de casco como entradas.
ms.assetid: a2eeb45a-85b2-4ed0-b071-fcbb8abf4f2d
keywords:
- HLSL de InputPatch
topic_type:
- apiref
api_name:
- InputPatch
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a882d032133ccb7bc98a34b3ef99551aa18fa51b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104996812"
---
# <a name="inputpatch"></a><span data-ttu-id="7860c-104">InputPatch</span><span class="sxs-lookup"><span data-stu-id="7860c-104">InputPatch</span></span>

<span data-ttu-id="7860c-105">Representa una matriz de puntos de control que están disponibles para el sombreador de casco como entradas.</span><span class="sxs-lookup"><span data-stu-id="7860c-105">Represents an array of control points that are available to the hull shader as inputs.</span></span>



| <span data-ttu-id="7860c-106">Método</span><span class="sxs-lookup"><span data-stu-id="7860c-106">Method</span></span>                                                      | <span data-ttu-id="7860c-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="7860c-107">Description</span></span>                         |
|-------------------------------------------------------------|-------------------------------------|
| <span data-ttu-id="7860c-108">[**Operador\[\]**](sm5-object-inputpatch-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="7860c-108">[**Operator\[\]**](sm5-object-inputpatch-operatorindex.md)</span></span> | <span data-ttu-id="7860c-109">Obtiene una variable de recurso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7860c-109">Gets a read-only resource variable.</span></span> |



 

<span data-ttu-id="7860c-110">La clase InputPatch también admite las siguientes propiedades:</span><span class="sxs-lookup"><span data-stu-id="7860c-110">The InputPatch class also supports the following properties:</span></span>



| <span data-ttu-id="7860c-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7860c-111">Properties</span></span> | <span data-ttu-id="7860c-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="7860c-112">Type</span></span> | <span data-ttu-id="7860c-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="7860c-113">Description</span></span>                   |
|------------|------|-------------------------------|
| <span data-ttu-id="7860c-114">Length</span><span class="sxs-lookup"><span data-stu-id="7860c-114">Length</span></span>     | <span data-ttu-id="7860c-115">uint</span><span class="sxs-lookup"><span data-stu-id="7860c-115">uint</span></span> | <span data-ttu-id="7860c-116">Número de puntos de control.</span><span class="sxs-lookup"><span data-stu-id="7860c-116">The number of control points.</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="7860c-117">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="7860c-117">Minimum Shader Model</span></span>

<span data-ttu-id="7860c-118">Este objeto es compatible con los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="7860c-118">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="7860c-119">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="7860c-119">Shader Model</span></span>                                                                | <span data-ttu-id="7860c-120">Compatible</span><span class="sxs-lookup"><span data-stu-id="7860c-120">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="7860c-121">Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="7860c-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="7860c-122">sí</span><span class="sxs-lookup"><span data-stu-id="7860c-122">yes</span></span>       |



 

<span data-ttu-id="7860c-123">Este objeto es compatible con los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="7860c-123">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="7860c-124">Vértice</span><span class="sxs-lookup"><span data-stu-id="7860c-124">Vertex</span></span> | <span data-ttu-id="7860c-125">Casco</span><span class="sxs-lookup"><span data-stu-id="7860c-125">Hull</span></span> | <span data-ttu-id="7860c-126">Dominio</span><span class="sxs-lookup"><span data-stu-id="7860c-126">Domain</span></span> | <span data-ttu-id="7860c-127">Geometría</span><span class="sxs-lookup"><span data-stu-id="7860c-127">Geometry</span></span> | <span data-ttu-id="7860c-128">Píxel</span><span class="sxs-lookup"><span data-stu-id="7860c-128">Pixel</span></span> | <span data-ttu-id="7860c-129">Compute</span><span class="sxs-lookup"><span data-stu-id="7860c-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="7860c-130">x</span><span class="sxs-lookup"><span data-stu-id="7860c-130">x</span></span>    |        | <span data-ttu-id="7860c-131">x</span><span class="sxs-lookup"><span data-stu-id="7860c-131">x</span></span>        |       |         |



 

## <a name="see-also"></a><span data-ttu-id="7860c-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="7860c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7860c-133">Objetos del modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="7860c-133">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




