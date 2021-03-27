---
title: Texture2DMS
description: Tipo Texture2DMS (tal como existe en el modelo de sombreador 4) más las variables de recurso.
ms.assetid: afda7324-680e-432a-a445-d90bd708e5e0
keywords:
- HLSL de Texture2DMS
topic_type:
- apiref
api_name:
- Texture2DMS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c16c69a4fa0fd35ce7b12d69f880daa4b8345d02
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076632"
---
# <a name="texture2dms"></a><span data-ttu-id="1fef0-104">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="1fef0-104">Texture2DMS</span></span>

<span data-ttu-id="1fef0-105">Tipo Texture2DMS (tal como existe en el modelo de sombreador 4) más las variables de recurso.</span><span class="sxs-lookup"><span data-stu-id="1fef0-105">Texture2DMS type (as it exists in Shader Model 4) plus resource variables.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1fef0-106">En esta sección</span><span class="sxs-lookup"><span data-stu-id="1fef0-106">In this section</span></span>



| <span data-ttu-id="1fef0-107">Tema</span><span class="sxs-lookup"><span data-stu-id="1fef0-107">Topic</span></span>                                                                                    | <span data-ttu-id="1fef0-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="1fef0-108">Description</span></span>                                                                                 |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1fef0-109">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="1fef0-109">**GetDimensions**</span></span>](sm5-object-texture2dms-getdimensions.md)<br/>                 | <span data-ttu-id="1fef0-110">Devuelve las dimensiones del recurso.</span><span class="sxs-lookup"><span data-stu-id="1fef0-110">Returns the dimensions of the resource.</span></span><br/>                                          |
| [<span data-ttu-id="1fef0-111">**GetSamplePosition**</span><span class="sxs-lookup"><span data-stu-id="1fef0-111">**GetSamplePosition**</span></span>](sm5-object-texture2dms-getsampleposition.md)<br/>         | <span data-ttu-id="1fef0-112">Devuelve la posición de ejemplo para el índice de ejemplo proporcionado.</span><span class="sxs-lookup"><span data-stu-id="1fef0-112">Returns the sample position for the sample index provided.</span></span><br/>                       |
| [<span data-ttu-id="1fef0-113">**Cargar métodos**</span><span class="sxs-lookup"><span data-stu-id="1fef0-113">**Load methods**</span></span>](texture2dms-load.md)<br/>                                      | <span data-ttu-id="1fef0-114">Recupera un valor del recurso en la ubicación y el índice de ejemplo proporcionados.</span><span class="sxs-lookup"><span data-stu-id="1fef0-114">Retrieves a value from the resource at the location and sample index provided.</span></span><br/>   |
| <span data-ttu-id="1fef0-115">[**AdventureWorks. Operator\[\]\[\]**](sm5-object-texture2dms-sampleoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="1fef0-115">[**sample.Operator\[\]\[\]**](sm5-object-texture2dms-sampleoperatorindex.md)</span></span><br/> | <span data-ttu-id="1fef0-116">Recupera un valor del recurso en la ubicación y el índice de ejemplo proporcionados.</span><span class="sxs-lookup"><span data-stu-id="1fef0-116">Retrieves a value from the resource at the location and sample index provided.</span></span><br/>   |
| <span data-ttu-id="1fef0-117">[**Operador\[\]**](sm5-object-texture2dms-operator1.md)</span><span class="sxs-lookup"><span data-stu-id="1fef0-117">[**Operator\[\]**](sm5-object-texture2dms-operator1.md)</span></span><br/>                      | <span data-ttu-id="1fef0-118">Recupera un valor del recurso en la ubicación proporcionada en el índice de ejemplo 0.</span><span class="sxs-lookup"><span data-stu-id="1fef0-118">Retrieves a value from the resource at the location provided at sample index 0.</span></span> <br/> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1fef0-119">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="1fef0-119">Minimum Shader Model</span></span>

<span data-ttu-id="1fef0-120">Este objeto es compatible con los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="1fef0-120">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="1fef0-121">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="1fef0-121">Shader Model</span></span>              | <span data-ttu-id="1fef0-122">Compatible</span><span class="sxs-lookup"><span data-stu-id="1fef0-122">Supported</span></span> |
|---------------------------|-----------|
| <span data-ttu-id="1fef0-123">Modelo de sombreador 4 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="1fef0-123">Shader model 4 and higher</span></span> | <span data-ttu-id="1fef0-124">sí</span><span class="sxs-lookup"><span data-stu-id="1fef0-124">yes</span></span>       |



 

<span data-ttu-id="1fef0-125">Este objeto es compatible con los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="1fef0-125">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="1fef0-126">Vértice</span><span class="sxs-lookup"><span data-stu-id="1fef0-126">Vertex</span></span> | <span data-ttu-id="1fef0-127">Casco</span><span class="sxs-lookup"><span data-stu-id="1fef0-127">Hull</span></span> | <span data-ttu-id="1fef0-128">Dominio</span><span class="sxs-lookup"><span data-stu-id="1fef0-128">Domain</span></span> | <span data-ttu-id="1fef0-129">Geometría</span><span class="sxs-lookup"><span data-stu-id="1fef0-129">Geometry</span></span> | <span data-ttu-id="1fef0-130">Píxel</span><span class="sxs-lookup"><span data-stu-id="1fef0-130">Pixel</span></span> | <span data-ttu-id="1fef0-131">Compute</span><span class="sxs-lookup"><span data-stu-id="1fef0-131">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="1fef0-132">x</span><span class="sxs-lookup"><span data-stu-id="1fef0-132">x</span></span>      | <span data-ttu-id="1fef0-133">x</span><span class="sxs-lookup"><span data-stu-id="1fef0-133">x</span></span>    | <span data-ttu-id="1fef0-134">x</span><span class="sxs-lookup"><span data-stu-id="1fef0-134">x</span></span>      | <span data-ttu-id="1fef0-135">x</span><span class="sxs-lookup"><span data-stu-id="1fef0-135">x</span></span>        | <span data-ttu-id="1fef0-136">x</span><span class="sxs-lookup"><span data-stu-id="1fef0-136">x</span></span>     | <span data-ttu-id="1fef0-137">x</span><span class="sxs-lookup"><span data-stu-id="1fef0-137">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="1fef0-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="1fef0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fef0-139">Objetos del modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="1fef0-139">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 





