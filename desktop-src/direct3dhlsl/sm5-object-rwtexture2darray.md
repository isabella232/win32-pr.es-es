---
title: RWTexture2DArray
description: Un recurso de lectura/escritura. | RWTexture2DArray
ms.assetid: 6a6f3655-f1c0-4d5b-91a2-d79da65858b8
keywords:
- HLSL de RWTexture2DArray
topic_type:
- apiref
api_name:
- RWTexture2DArray
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5ada0fcaba729eff37f41f1ae7666841175689ff
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986422"
---
# <a name="rwtexture2darray"></a><span data-ttu-id="53920-105">RWTexture2DArray</span><span class="sxs-lookup"><span data-stu-id="53920-105">RWTexture2DArray</span></span>

<span data-ttu-id="53920-106">Un recurso de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="53920-106">A read/write resource.</span></span>



| <span data-ttu-id="53920-107">Método</span><span class="sxs-lookup"><span data-stu-id="53920-107">Method</span></span>                                                             | <span data-ttu-id="53920-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="53920-108">Description</span></span>                   |
|--------------------------------------------------------------------|-------------------------------|
| [<span data-ttu-id="53920-109">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="53920-109">**GetDimensions**</span></span>](sm5-object-rwtexture2darray-getdimensions.md) | <span data-ttu-id="53920-110">Obtiene las dimensiones de recursos.</span><span class="sxs-lookup"><span data-stu-id="53920-110">Gets the resource dimensions.</span></span> |
| [<span data-ttu-id="53920-111">**Carga**</span><span class="sxs-lookup"><span data-stu-id="53920-111">**Load**</span></span>](rwtexture2darray-load.md)                              | <span data-ttu-id="53920-112">Lee los datos de textura.</span><span class="sxs-lookup"><span data-stu-id="53920-112">Reads texture data.</span></span>           |
| <span data-ttu-id="53920-113">[**Operador\[\]**](sm5-object-rwtexture2darray-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="53920-113">[**Operator\[\]**](sm5-object-rwtexture2darray-operatorindex.md)</span></span>  | <span data-ttu-id="53920-114">Obtiene una variable de recurso.</span><span class="sxs-lookup"><span data-stu-id="53920-114">Gets a resource variable.</span></span>     |



 

<span data-ttu-id="53920-115">Puede prefijar objetos **RWTexture2DArray** con la clase de almacenamiento **globallycoherent**.</span><span class="sxs-lookup"><span data-stu-id="53920-115">You can prefix **RWTexture2DArray** objects with the storage class **globallycoherent**.</span></span> <span data-ttu-id="53920-116">Esta clase de almacenamiento provoca barreras de memoria y sincronizaciones para vaciar los datos en toda la GPU, de modo que otros grupos puedan ver escrituras.</span><span class="sxs-lookup"><span data-stu-id="53920-116">This storage class causes memory barriers and syncs to flush data across the entire GPU such that other groups can see writes.</span></span> <span data-ttu-id="53920-117">Sin este especificador, una barrera de memoria o una sincronización vaciará un UAV solo dentro del grupo actual.</span><span class="sxs-lookup"><span data-stu-id="53920-117">Without this specifier, a memory barrier or sync will flush a UAV only within the current group.</span></span>

<span data-ttu-id="53920-118">Un objeto **RWTexture2DArray** requiere un tipo de elemento en una instrucción de declaración para el objeto.</span><span class="sxs-lookup"><span data-stu-id="53920-118">A **RWTexture2DArray** object requires an element type in a declaration statement for the object.</span></span> <span data-ttu-id="53920-119">Por ejemplo, la siguiente declaración es correcta:</span><span class="sxs-lookup"><span data-stu-id="53920-119">For example, the following declaration is correct:</span></span>


```
RWTexture2DArray<float> tex;
```



<span data-ttu-id="53920-120">Dado que un objeto **RWTexture2DArray** es un objeto de tipo UAV, sus propiedades difieren de un objeto de tipo de vista de recursos de sombreador (SRV), como un objeto [**Texture2DArray**](sm5-object-texture2darray.md) .</span><span class="sxs-lookup"><span data-stu-id="53920-120">Because a **RWTexture2DArray** object is a UAV-type object, its properties differ from a shader resource view (SRV)-type object, such as a [**Texture2DArray**](sm5-object-texture2darray.md) object.</span></span> <span data-ttu-id="53920-121">Por ejemplo, puede leer y escribir en un objeto **RWTexture2DArray** , pero solo puede leer desde un objeto **Texture2DArray** .</span><span class="sxs-lookup"><span data-stu-id="53920-121">For example, you can read from and write to a **RWTexture2DArray** object, but you can only read from a **Texture2DArray** object.</span></span>

<span data-ttu-id="53920-122">Un objeto **RWTexture2DArray** no puede utilizar métodos de un objeto [**Texture2DArray**](sm5-object-texture2darray.md) , como [ejemplo](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="53920-122">A **RWTexture2DArray** object cannot use methods from a [**Texture2DArray**](sm5-object-texture2darray.md) object, such as [Sample](dx-graphics-hlsl-to-sample.md).</span></span> <span data-ttu-id="53920-123">Sin embargo, como puede crear varios tipos de vistas en el mismo recurso, puede declarar varios tipos de textura como una sola textura en varios sombreadores.</span><span class="sxs-lookup"><span data-stu-id="53920-123">However, because you can create multiple view types to the same resource, you can declare multiple texture types as a single texture in multiple shaders.</span></span> <span data-ttu-id="53920-124">Por ejemplo, puede declarar y usar un objeto **RWTexture2DArray** como *Tex* en un sombreador de cálculo y, a continuación, declarar y usar un objeto **Texture2DArray** como *Tex* en un sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="53920-124">For example, you can declare and use a **RWTexture2DArray** object as *tex* in a compute shader and then declare and use a **Texture2DArray** object as *tex* in a pixel shader.</span></span>

> [!Note]  
> <span data-ttu-id="53920-125">El tiempo de ejecución exige determinados patrones de uso al crear varios tipos de vistas en el mismo recurso.</span><span class="sxs-lookup"><span data-stu-id="53920-125">The runtime enforces certain usage patterns when you create multiple view types to the same resource.</span></span> <span data-ttu-id="53920-126">Por ejemplo, el tiempo de ejecución no permite tener una asignación UAV para un recurso y una asignación SRV para el mismo recurso activo al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="53920-126">For example, the runtime does not allow you to have both a UAV mapping for a resource and SRV mapping for the same resource active at the same time.</span></span>

 

## <a name="minimum-shader-model"></a><span data-ttu-id="53920-127">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="53920-127">Minimum Shader Model</span></span>

<span data-ttu-id="53920-128">Este objeto es compatible con los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="53920-128">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="53920-129">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="53920-129">Shader Model</span></span>                                                                | <span data-ttu-id="53920-130">Compatible</span><span class="sxs-lookup"><span data-stu-id="53920-130">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="53920-131">Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="53920-131">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="53920-132">sí</span><span class="sxs-lookup"><span data-stu-id="53920-132">yes</span></span>       |



 

<span data-ttu-id="53920-133">Este objeto es compatible con los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="53920-133">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="53920-134">Vértice</span><span class="sxs-lookup"><span data-stu-id="53920-134">Vertex</span></span> | <span data-ttu-id="53920-135">Casco</span><span class="sxs-lookup"><span data-stu-id="53920-135">Hull</span></span> | <span data-ttu-id="53920-136">Dominio</span><span class="sxs-lookup"><span data-stu-id="53920-136">Domain</span></span> | <span data-ttu-id="53920-137">Geometría</span><span class="sxs-lookup"><span data-stu-id="53920-137">Geometry</span></span> | <span data-ttu-id="53920-138">Píxel</span><span class="sxs-lookup"><span data-stu-id="53920-138">Pixel</span></span> | <span data-ttu-id="53920-139">Compute</span><span class="sxs-lookup"><span data-stu-id="53920-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="53920-140">x</span><span class="sxs-lookup"><span data-stu-id="53920-140">x</span></span>     | <span data-ttu-id="53920-141">x</span><span class="sxs-lookup"><span data-stu-id="53920-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="53920-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="53920-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53920-143">Objetos del modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="53920-143">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




