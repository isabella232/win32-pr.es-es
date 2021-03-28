---
title: Buffer
description: Buffer
ms.assetid: 7f552b9b-c5fb-4bc2-a7ae-61983379db38
keywords:
- HLSL de búfer
topic_type:
- apiref
api_name:
- Buffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce1754272fd90cedc5a806543dd83a99cdcd9455
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104419643"
---
# <a name="buffer"></a><span data-ttu-id="246e5-104">Buffer</span><span class="sxs-lookup"><span data-stu-id="246e5-104">Buffer</span></span>

<span data-ttu-id="246e5-105">Tipo de búfer tal como existe en el modelo de sombreador 4 más las variables de recursos y la información de búfer.</span><span class="sxs-lookup"><span data-stu-id="246e5-105">Buffer type as it exists in Shader Model 4 plus resource variables and buffer info.</span></span>



| <span data-ttu-id="246e5-106">Método</span><span class="sxs-lookup"><span data-stu-id="246e5-106">Method</span></span>                                                   | <span data-ttu-id="246e5-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="246e5-107">Description</span></span>                         |
|----------------------------------------------------------|-------------------------------------|
| [<span data-ttu-id="246e5-108">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="246e5-108">**GetDimensions**</span></span>](sm5-object-buffer-getdimensions.md) | <span data-ttu-id="246e5-109">Obtiene las dimensiones de recursos.</span><span class="sxs-lookup"><span data-stu-id="246e5-109">Gets the resource dimensions.</span></span>       |
| [<span data-ttu-id="246e5-110">**Carga**</span><span class="sxs-lookup"><span data-stu-id="246e5-110">**Load**</span></span>](buffer-load.md)                              | <span data-ttu-id="246e5-111">Lee los datos del búfer.</span><span class="sxs-lookup"><span data-stu-id="246e5-111">Reads buffer data.</span></span>                  |
| <span data-ttu-id="246e5-112">[**Operador\[\]**](sm5-object-buffer-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="246e5-112">[**Operator\[\]**](sm5-object-buffer-operatorindex.md)</span></span>  | <span data-ttu-id="246e5-113">Obtiene una variable de recurso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="246e5-113">Gets a read-only resource variable.</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="246e5-114">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="246e5-114">Minimum Shader Model</span></span>

<span data-ttu-id="246e5-115">Este objeto es compatible con los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="246e5-115">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="246e5-116">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="246e5-116">Shader Model</span></span>                                                                | <span data-ttu-id="246e5-117">Compatible</span><span class="sxs-lookup"><span data-stu-id="246e5-117">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="246e5-118">Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="246e5-118">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="246e5-119">sí</span><span class="sxs-lookup"><span data-stu-id="246e5-119">yes</span></span>       |



 

<span data-ttu-id="246e5-120">Este objeto es compatible con los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="246e5-120">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="246e5-121">Vértice</span><span class="sxs-lookup"><span data-stu-id="246e5-121">Vertex</span></span> | <span data-ttu-id="246e5-122">Casco</span><span class="sxs-lookup"><span data-stu-id="246e5-122">Hull</span></span> | <span data-ttu-id="246e5-123">Dominio</span><span class="sxs-lookup"><span data-stu-id="246e5-123">Domain</span></span> | <span data-ttu-id="246e5-124">Geometría</span><span class="sxs-lookup"><span data-stu-id="246e5-124">Geometry</span></span> | <span data-ttu-id="246e5-125">Píxel</span><span class="sxs-lookup"><span data-stu-id="246e5-125">Pixel</span></span> | <span data-ttu-id="246e5-126">Compute</span><span class="sxs-lookup"><span data-stu-id="246e5-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="246e5-127">x</span><span class="sxs-lookup"><span data-stu-id="246e5-127">x</span></span>      | <span data-ttu-id="246e5-128">x</span><span class="sxs-lookup"><span data-stu-id="246e5-128">x</span></span>    | <span data-ttu-id="246e5-129">x</span><span class="sxs-lookup"><span data-stu-id="246e5-129">x</span></span>      | <span data-ttu-id="246e5-130">x</span><span class="sxs-lookup"><span data-stu-id="246e5-130">x</span></span>        | <span data-ttu-id="246e5-131">x</span><span class="sxs-lookup"><span data-stu-id="246e5-131">x</span></span>     | <span data-ttu-id="246e5-132">x</span><span class="sxs-lookup"><span data-stu-id="246e5-132">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="246e5-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="246e5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="246e5-134">Objetos del modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="246e5-134">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




