---
title: RWTexture1D
description: Un recurso de lectura/escritura. | RWTexture1D
ms.assetid: 47866e5a-b26b-4264-9291-c8940882d662
keywords:
- HLSL de RWTexture1D
topic_type:
- apiref
api_name:
- RWTexture1D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 695b73cc14541505ee1b2d4391aac2d145eec8d7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986235"
---
# <a name="rwtexture1d"></a><span data-ttu-id="9ea0f-105">RWTexture1D</span><span class="sxs-lookup"><span data-stu-id="9ea0f-105">RWTexture1D</span></span>

<span data-ttu-id="9ea0f-106">Un recurso de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="9ea0f-106">A read/write resource.</span></span>



| <span data-ttu-id="9ea0f-107">Método</span><span class="sxs-lookup"><span data-stu-id="9ea0f-107">Method</span></span>                                                        | <span data-ttu-id="9ea0f-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="9ea0f-108">Description</span></span>                   |
|---------------------------------------------------------------|-------------------------------|
| [<span data-ttu-id="9ea0f-109">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="9ea0f-109">**GetDimensions**</span></span>](sm5-object-rwtexture1d-getdimensions.md) | <span data-ttu-id="9ea0f-110">Obtiene las dimensiones de recursos.</span><span class="sxs-lookup"><span data-stu-id="9ea0f-110">Gets the resource dimensions.</span></span> |
| [<span data-ttu-id="9ea0f-111">**Carga**</span><span class="sxs-lookup"><span data-stu-id="9ea0f-111">**Load**</span></span>](rwtexture1d-load.md)                              | <span data-ttu-id="9ea0f-112">Lee los datos de textura.</span><span class="sxs-lookup"><span data-stu-id="9ea0f-112">Reads texture data.</span></span>           |
| <span data-ttu-id="9ea0f-113">[**Operador\[\]**](sm5-object-rwtexture1d-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="9ea0f-113">[**Operator\[\]**](sm5-object-rwtexture1d-operatorindex.md)</span></span>  | <span data-ttu-id="9ea0f-114">Obtiene una variable de recurso.</span><span class="sxs-lookup"><span data-stu-id="9ea0f-114">Gets a resource variable.</span></span>     |



 

<span data-ttu-id="9ea0f-115">Puede prefijar objetos **RWTexture1D** con la clase de almacenamiento **globallycoherent**.</span><span class="sxs-lookup"><span data-stu-id="9ea0f-115">You can prefix **RWTexture1D** objects with the storage class **globallycoherent**.</span></span> <span data-ttu-id="9ea0f-116">Esta clase de almacenamiento provoca barreras de memoria y sincronizaciones para vaciar los datos en toda la GPU, de modo que otros grupos puedan ver escrituras.</span><span class="sxs-lookup"><span data-stu-id="9ea0f-116">This storage class causes memory barriers and syncs to flush data across the entire GPU such that other groups can see writes.</span></span> <span data-ttu-id="9ea0f-117">Sin este especificador, una barrera de memoria o una sincronización vaciará un UAV solo dentro del grupo actual.</span><span class="sxs-lookup"><span data-stu-id="9ea0f-117">Without this specifier, a memory barrier or sync will flush a UAV only within the current group.</span></span>

<span data-ttu-id="9ea0f-118">Un objeto **RWTexture1D** requiere un tipo de elemento en una instrucción de declaración para el objeto.</span><span class="sxs-lookup"><span data-stu-id="9ea0f-118">A **RWTexture1D** object requires an element type in a declaration statement for the object.</span></span> <span data-ttu-id="9ea0f-119">Por ejemplo, la siguiente declaración es correcta:</span><span class="sxs-lookup"><span data-stu-id="9ea0f-119">For example, the following declaration is correct:</span></span>


```
RWTexture1D<float> tex;
```



<span data-ttu-id="9ea0f-120">Dado que un objeto **RWTexture1D** es un objeto de tipo UAV, sus propiedades difieren de un objeto de tipo de vista de recursos de sombreador (SRV), como un objeto [**Texture1D**](sm5-object-texture1d.md) .</span><span class="sxs-lookup"><span data-stu-id="9ea0f-120">Because a **RWTexture1D** object is a UAV-type object, its properties differ from a shader resource view (SRV)-type object, such as a [**Texture1D**](sm5-object-texture1d.md) object.</span></span> <span data-ttu-id="9ea0f-121">Por ejemplo, puede leer y escribir en un objeto **RWTexture1D** , pero solo puede leer desde un objeto **Texture1D** .</span><span class="sxs-lookup"><span data-stu-id="9ea0f-121">For example, you can read from and write to a **RWTexture1D** object, but you can only read from a **Texture1D** object.</span></span>

<span data-ttu-id="9ea0f-122">Un objeto **RWTexture1D** no puede utilizar métodos de un objeto [**Texture1D**](sm5-object-texture1d.md) , como [ejemplo](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="9ea0f-122">A **RWTexture1D** object cannot use methods from a [**Texture1D**](sm5-object-texture1d.md) object, such as [Sample](dx-graphics-hlsl-to-sample.md).</span></span> <span data-ttu-id="9ea0f-123">Sin embargo, como puede crear varios tipos de vistas en el mismo recurso, puede declarar varios tipos de textura como una sola textura en varios sombreadores.</span><span class="sxs-lookup"><span data-stu-id="9ea0f-123">However, because you can create multiple view types to the same resource, you can declare multiple texture types as a single texture in multiple shaders.</span></span> <span data-ttu-id="9ea0f-124">Por ejemplo, puede declarar y usar un objeto **RWTexture1D** como *Tex* en un sombreador de cálculo y, a continuación, declarar y usar un objeto **Texture1D** como *Tex* en un sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="9ea0f-124">For example, you can declare and use a **RWTexture1D** object as *tex* in a compute shader and then declare and use a **Texture1D** object as *tex* in a pixel shader.</span></span>

> [!Note]  
> <span data-ttu-id="9ea0f-125">El tiempo de ejecución exige determinados patrones de uso al crear varios tipos de vistas en el mismo recurso.</span><span class="sxs-lookup"><span data-stu-id="9ea0f-125">The runtime enforces certain usage patterns when you create multiple view types to the same resource.</span></span> <span data-ttu-id="9ea0f-126">Por ejemplo, el tiempo de ejecución no permite tener una asignación UAV para un recurso y una asignación SRV para el mismo recurso activo al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="9ea0f-126">For example, the runtime does not allow you to have both a UAV mapping for a resource and SRV mapping for the same resource active at the same time.</span></span>

 

## <a name="minimum-shader-model"></a><span data-ttu-id="9ea0f-127">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="9ea0f-127">Minimum Shader Model</span></span>

<span data-ttu-id="9ea0f-128">Este objeto es compatible con los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="9ea0f-128">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="9ea0f-129">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="9ea0f-129">Shader Model</span></span>                                                                | <span data-ttu-id="9ea0f-130">Compatible</span><span class="sxs-lookup"><span data-stu-id="9ea0f-130">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="9ea0f-131">Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="9ea0f-131">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="9ea0f-132">sí</span><span class="sxs-lookup"><span data-stu-id="9ea0f-132">yes</span></span>       |



 

<span data-ttu-id="9ea0f-133">Este objeto es compatible con los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="9ea0f-133">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="9ea0f-134">Vértice</span><span class="sxs-lookup"><span data-stu-id="9ea0f-134">Vertex</span></span> | <span data-ttu-id="9ea0f-135">Casco</span><span class="sxs-lookup"><span data-stu-id="9ea0f-135">Hull</span></span> | <span data-ttu-id="9ea0f-136">Dominio</span><span class="sxs-lookup"><span data-stu-id="9ea0f-136">Domain</span></span> | <span data-ttu-id="9ea0f-137">Geometría</span><span class="sxs-lookup"><span data-stu-id="9ea0f-137">Geometry</span></span> | <span data-ttu-id="9ea0f-138">Píxel</span><span class="sxs-lookup"><span data-stu-id="9ea0f-138">Pixel</span></span> | <span data-ttu-id="9ea0f-139">Compute</span><span class="sxs-lookup"><span data-stu-id="9ea0f-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="9ea0f-140">x</span><span class="sxs-lookup"><span data-stu-id="9ea0f-140">x</span></span>     | <span data-ttu-id="9ea0f-141">x</span><span class="sxs-lookup"><span data-stu-id="9ea0f-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="9ea0f-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="9ea0f-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ea0f-143">Objetos del modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="9ea0f-143">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




