---
title: OutputPatch
description: OutputPatch
ms.assetid: 24841938-6c84-4e1f-ba8a-a81b589bdd51
keywords:
- HLSL de OutputPatch
topic_type:
- apiref
api_name:
- OutputPatch
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4c77a30a2ff23bdc292d45df6514ef00fab53463
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076592"
---
# <a name="outputpatch"></a><span data-ttu-id="f1327-104">OutputPatch</span><span class="sxs-lookup"><span data-stu-id="f1327-104">OutputPatch</span></span>

<span data-ttu-id="f1327-105">Representa una matriz de puntos de control de salida que están disponibles para la función patch-Constant del sombreador de casco, así como para el sombreador de dominios.</span><span class="sxs-lookup"><span data-stu-id="f1327-105">Represents an array of output control points that are available to the hull shader's patch-constant function as well as the domain shader.</span></span>



| <span data-ttu-id="f1327-106">Método</span><span class="sxs-lookup"><span data-stu-id="f1327-106">Method</span></span>                                                       | <span data-ttu-id="f1327-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="f1327-107">Description</span></span>                         |
|--------------------------------------------------------------|-------------------------------------|
| <span data-ttu-id="f1327-108">[**Operador\[\]**](sm5-object-outputpatch-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="f1327-108">[**Operator\[\]**](sm5-object-outputpatch-operatorindex.md)</span></span> | <span data-ttu-id="f1327-109">Obtiene una variable de recurso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="f1327-109">Gets a read-only resource variable.</span></span> |



 

<span data-ttu-id="f1327-110">Además, la clase InputPatch admite las siguientes propiedades:</span><span class="sxs-lookup"><span data-stu-id="f1327-110">In addition, the InputPatch class supports the following properties:</span></span>



| <span data-ttu-id="f1327-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f1327-111">Properties</span></span> | <span data-ttu-id="f1327-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="f1327-112">Type</span></span> | <span data-ttu-id="f1327-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="f1327-113">Description</span></span>                   |
|------------|------|-------------------------------|
| <span data-ttu-id="f1327-114">Length</span><span class="sxs-lookup"><span data-stu-id="f1327-114">Length</span></span>     | <span data-ttu-id="f1327-115">uint</span><span class="sxs-lookup"><span data-stu-id="f1327-115">uint</span></span> | <span data-ttu-id="f1327-116">Número de puntos de control.</span><span class="sxs-lookup"><span data-stu-id="f1327-116">The number of control points.</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f1327-117">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="f1327-117">Minimum Shader Model</span></span>

<span data-ttu-id="f1327-118">Este objeto es compatible con los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="f1327-118">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="f1327-119">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="f1327-119">Shader Model</span></span>                                                                | <span data-ttu-id="f1327-120">Compatible</span><span class="sxs-lookup"><span data-stu-id="f1327-120">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="f1327-121">Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="f1327-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="f1327-122">sí</span><span class="sxs-lookup"><span data-stu-id="f1327-122">yes</span></span>       |



 

<span data-ttu-id="f1327-123">Este objeto es compatible con los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="f1327-123">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="f1327-124">Vértice</span><span class="sxs-lookup"><span data-stu-id="f1327-124">Vertex</span></span> | <span data-ttu-id="f1327-125">Casco</span><span class="sxs-lookup"><span data-stu-id="f1327-125">Hull</span></span> | <span data-ttu-id="f1327-126">Dominio</span><span class="sxs-lookup"><span data-stu-id="f1327-126">Domain</span></span> | <span data-ttu-id="f1327-127">Geometría</span><span class="sxs-lookup"><span data-stu-id="f1327-127">Geometry</span></span> | <span data-ttu-id="f1327-128">Píxel</span><span class="sxs-lookup"><span data-stu-id="f1327-128">Pixel</span></span> | <span data-ttu-id="f1327-129">Compute</span><span class="sxs-lookup"><span data-stu-id="f1327-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="f1327-130">x</span><span class="sxs-lookup"><span data-stu-id="f1327-130">x</span></span>    | <span data-ttu-id="f1327-131">x</span><span class="sxs-lookup"><span data-stu-id="f1327-131">x</span></span>      |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="f1327-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="f1327-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1327-133">Objetos del modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="f1327-133">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




