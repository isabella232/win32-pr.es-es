---
title: Texture2DMSArray
description: Texture2DMSArray
ms.assetid: 4200eba8-a9e5-41ba-b04c-4ac7b20274d2
keywords:
- HLSL de Texture2DMSArray
topic_type:
- apiref
api_name:
- Texture2DMSArray
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: effe4819c674a7909cc445b9e9f7b5322fae7676
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/14/2021
ms.locfileid: "104279764"
---
# <a name="texture2dmsarray"></a><span data-ttu-id="0c507-104">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="0c507-104">Texture2DMSArray</span></span>

<span data-ttu-id="0c507-105">Tipo Texture2DMSArray (tal como existe en el modelo de sombreador 4) más las variables de recurso.</span><span class="sxs-lookup"><span data-stu-id="0c507-105">Texture2DMSArray type (as it exists in Shader Model 4) plus resource variables.</span></span>



| <span data-ttu-id="0c507-106">Método</span><span class="sxs-lookup"><span data-stu-id="0c507-106">Method</span></span>                                                                             | <span data-ttu-id="0c507-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="0c507-107">Description</span></span>                                        |
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="0c507-108">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="0c507-108">**GetDimensions**</span></span>](sm5-object-texture2dmsarray-getdimensions.md)                  | <span data-ttu-id="0c507-109">Obtiene las dimensiones de recursos.</span><span class="sxs-lookup"><span data-stu-id="0c507-109">Gets the resource dimensions.</span></span>                      |
| [<span data-ttu-id="0c507-110">**GetSamplePosition**</span><span class="sxs-lookup"><span data-stu-id="0c507-110">**GetSamplePosition**</span></span>](sm5-object-texture2dmsarray-getsampleposition.md)          | <span data-ttu-id="0c507-111">Obtiene la posición del ejemplo especificado.</span><span class="sxs-lookup"><span data-stu-id="0c507-111">Gets the position of the specified sample.</span></span>         |
| [<span data-ttu-id="0c507-112">**Carga**</span><span class="sxs-lookup"><span data-stu-id="0c507-112">**Load**</span></span>](texture2dmsarray-load.md)                                               | <span data-ttu-id="0c507-113">Obtiene un valor.</span><span class="sxs-lookup"><span data-stu-id="0c507-113">Gets one value.</span></span>                                    |
| <span data-ttu-id="0c507-114">[**AdventureWorks. Operator\[\]\[\]**](sm5-object-texture2dmsarray-sampleoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="0c507-114">[**sample.Operator\[\]\[\]**](sm5-object-texture2dmsarray-sampleoperatorindex.md)</span></span>  | <span data-ttu-id="0c507-115">Obtiene una variable de recurso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0c507-115">Gets a read-only resource variable.</span></span>                |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0c507-116">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="0c507-116">Minimum Shader Model</span></span>

<span data-ttu-id="0c507-117">Este objeto es compatible con los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="0c507-117">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="0c507-118">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="0c507-118">Shader Model</span></span>                                                                | <span data-ttu-id="0c507-119">Compatible</span><span class="sxs-lookup"><span data-stu-id="0c507-119">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="0c507-120">Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="0c507-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="0c507-121">sí</span><span class="sxs-lookup"><span data-stu-id="0c507-121">yes</span></span>       |



 

<span data-ttu-id="0c507-122">Este objeto es compatible con los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="0c507-122">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="0c507-123">Vértice</span><span class="sxs-lookup"><span data-stu-id="0c507-123">Vertex</span></span> | <span data-ttu-id="0c507-124">Casco</span><span class="sxs-lookup"><span data-stu-id="0c507-124">Hull</span></span> | <span data-ttu-id="0c507-125">Dominio</span><span class="sxs-lookup"><span data-stu-id="0c507-125">Domain</span></span> | <span data-ttu-id="0c507-126">Geometría</span><span class="sxs-lookup"><span data-stu-id="0c507-126">Geometry</span></span> | <span data-ttu-id="0c507-127">Píxel</span><span class="sxs-lookup"><span data-stu-id="0c507-127">Pixel</span></span> | <span data-ttu-id="0c507-128">Compute</span><span class="sxs-lookup"><span data-stu-id="0c507-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="0c507-129">x</span><span class="sxs-lookup"><span data-stu-id="0c507-129">x</span></span>      | <span data-ttu-id="0c507-130">x</span><span class="sxs-lookup"><span data-stu-id="0c507-130">x</span></span>    | <span data-ttu-id="0c507-131">x</span><span class="sxs-lookup"><span data-stu-id="0c507-131">x</span></span>      | <span data-ttu-id="0c507-132">x</span><span class="sxs-lookup"><span data-stu-id="0c507-132">x</span></span>        | <span data-ttu-id="0c507-133">x</span><span class="sxs-lookup"><span data-stu-id="0c507-133">x</span></span>     | <span data-ttu-id="0c507-134">x</span><span class="sxs-lookup"><span data-stu-id="0c507-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="0c507-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="0c507-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c507-136">Objetos del modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="0c507-136">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




