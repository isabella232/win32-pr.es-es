---
title: RWTexture2D
description: Un recurso de lectura/escritura. | RWTexture2D
ms.assetid: 19b383f1-c787-4c20-b77a-60ef9f212b9f
keywords:
- HLSL de RWTexture2D
topic_type:
- apiref
api_name:
- RWTexture2D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ccdeae4dd47d3ad4bf5d756c2ca362033eae6814
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362193"
---
# <a name="rwtexture2d"></a><span data-ttu-id="65fa2-105">RWTexture2D</span><span class="sxs-lookup"><span data-stu-id="65fa2-105">RWTexture2D</span></span>

<span data-ttu-id="65fa2-106">Un recurso de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="65fa2-106">A read/write resource.</span></span>



| <span data-ttu-id="65fa2-107">Método</span><span class="sxs-lookup"><span data-stu-id="65fa2-107">Method</span></span>                                                        | <span data-ttu-id="65fa2-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="65fa2-108">Description</span></span>                   |
|---------------------------------------------------------------|-------------------------------|
| [<span data-ttu-id="65fa2-109">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="65fa2-109">**GetDimensions**</span></span>](sm5-object-rwtexture2d-getdimensions.md) | <span data-ttu-id="65fa2-110">Obtiene las dimensiones de recursos.</span><span class="sxs-lookup"><span data-stu-id="65fa2-110">Gets the resource dimensions.</span></span> |
| [<span data-ttu-id="65fa2-111">**Carga**</span><span class="sxs-lookup"><span data-stu-id="65fa2-111">**Load**</span></span>](rwtexture2d-load.md)                              | <span data-ttu-id="65fa2-112">Lee los datos de textura.</span><span class="sxs-lookup"><span data-stu-id="65fa2-112">Reads texture data.</span></span>           |
| <span data-ttu-id="65fa2-113">[**Operador\[\]**](sm5-object-rwtexture2d-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="65fa2-113">[**Operator\[\]**](sm5-object-rwtexture2d-operatorindex.md)</span></span>  | <span data-ttu-id="65fa2-114">Obtiene una variable de recurso.</span><span class="sxs-lookup"><span data-stu-id="65fa2-114">Gets a resource variable.</span></span>     |



 

<span data-ttu-id="65fa2-115">Puede prefijar objetos RWTexture2D con la clase de almacenamiento **globallycoherent**.</span><span class="sxs-lookup"><span data-stu-id="65fa2-115">You can prefix RWTexture2D objects with the storage class **globallycoherent**.</span></span> <span data-ttu-id="65fa2-116">Esta clase de almacenamiento provoca barreras de memoria y sincronizaciones para vaciar los datos en toda la GPU, de modo que otros grupos puedan ver escrituras.</span><span class="sxs-lookup"><span data-stu-id="65fa2-116">This storage class causes memory barriers and syncs to flush data across the entire GPU such that other groups can see writes.</span></span> <span data-ttu-id="65fa2-117">Sin este especificador, una barrera de memoria o una sincronización solo vaciará una vista de acceso desordenado (UAV) en el grupo actual.</span><span class="sxs-lookup"><span data-stu-id="65fa2-117">Without this specifier, a memory barrier or sync will flush only an unordered access view (UAV) within the current group.</span></span>

<span data-ttu-id="65fa2-118">Un objeto RWTexture2D requiere un tipo de elemento en una instrucción de declaración para el objeto.</span><span class="sxs-lookup"><span data-stu-id="65fa2-118">A RWTexture2D object requires an element type in a declaration statement for the object.</span></span> <span data-ttu-id="65fa2-119">Por ejemplo, la siguiente declaración no es correcta:</span><span class="sxs-lookup"><span data-stu-id="65fa2-119">For example, the following declaration is not correct:</span></span>


```
// The following declaration is incorrectly coded.
RWTexture2D myTexture;
```



<span data-ttu-id="65fa2-120">La siguiente declaración es correcta:</span><span class="sxs-lookup"><span data-stu-id="65fa2-120">The following declaration is correct:</span></span>


```
// The following declaration is correctly coded.
RWTexture2D<float> tex;
```



<span data-ttu-id="65fa2-121">Dado que un objeto RWTexture2D es un objeto de tipo UAV, sus propiedades difieren de un objeto de tipo de vista de recursos de sombreador (SRV), como un objeto [Texture2D](sm5-object-texture2d.md) .</span><span class="sxs-lookup"><span data-stu-id="65fa2-121">Because a RWTexture2D object is a UAV-type object, its properties differ from a shader resource view (SRV)-type object, such as a [Texture2D](sm5-object-texture2d.md) object.</span></span> <span data-ttu-id="65fa2-122">Por ejemplo, puede leer y escribir en un objeto RWTexture2D, pero solo puede leer desde un objeto Texture2D.</span><span class="sxs-lookup"><span data-stu-id="65fa2-122">For example, you can read from and write to a RWTexture2D object, but you can only read from a Texture2D object.</span></span>

<span data-ttu-id="65fa2-123">Un objeto RWTexture2D no puede utilizar métodos de un objeto [Texture2D](sm5-object-texture2d.md) , como [ejemplo](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="65fa2-123">A RWTexture2D object cannot use methods from a [Texture2D](sm5-object-texture2d.md) object, such as [Sample](dx-graphics-hlsl-to-sample.md).</span></span> <span data-ttu-id="65fa2-124">Sin embargo, como puede crear varios tipos de vistas en el mismo recurso, puede declarar varios tipos de textura como una sola textura en varios sombreadores.</span><span class="sxs-lookup"><span data-stu-id="65fa2-124">However, because you can create multiple view types to the same resource, you can declare multiple texture types as a single texture in multiple shaders.</span></span> <span data-ttu-id="65fa2-125">Por ejemplo, los fragmentos de código siguientes muestran cómo se puede declarar y usar un objeto RWTexture2D como *Tex* en un sombreador de cálculo y, a continuación, declarar y usar un objeto Texture2D como *Tex* en un sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="65fa2-125">For example, the following code snippets show how you can declare and use a RWTexture2D object as *tex* in a compute shader and then declare and use a Texture2D object as *tex* in a pixel shader.</span></span>

> [!Note]  
> <span data-ttu-id="65fa2-126">El tiempo de ejecución exige determinados patrones de uso al crear varios tipos de vistas en el mismo recurso.</span><span class="sxs-lookup"><span data-stu-id="65fa2-126">The runtime enforces certain usage patterns when you create multiple view types to the same resource.</span></span> <span data-ttu-id="65fa2-127">Por ejemplo, el tiempo de ejecución no permite tener una asignación UAV para un recurso y una asignación SRV para el mismo recurso activo al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="65fa2-127">For example, the runtime does not allow you to have both a UAV mapping for a resource and SRV mapping for the same resource active at the same time.</span></span>

 

<span data-ttu-id="65fa2-128">El código siguiente es para el sombreador de cálculo:</span><span class="sxs-lookup"><span data-stu-id="65fa2-128">The following code is for the compute shader:</span></span>


```
RWTexture2D<float> tex;
[numthreads(groupDim_x, groupDim_y, 1)]
void main(
    uint3 groupId : SV_GroupID,
    uint3 groupThreadId : SV_GroupThreadID,
    uint3 dispatchThreadId : SV_DispatchThreadID,
    uint groupIndex : SV_GroupIndex)
{
    tex [dispatchThreadId.xy] = <something>;
}
```



<span data-ttu-id="65fa2-129">El siguiente código es para el sombreador de píxeles:</span><span class="sxs-lookup"><span data-stu-id="65fa2-129">The following code is for the pixel shader:</span></span>


```
struct PixelShaderInput
{
    float4 pos : SV_POSITION;
    float2 tex : TEXTURE;
};

Texture2D<float> tex;
float4 main(PixelShaderInput input) : SV_TARGET
{
    return tex.Sample(TextureSampler, input.tex);
}
```



## <a name="minimum-shader-model"></a><span data-ttu-id="65fa2-130">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="65fa2-130">Minimum Shader Model</span></span>

<span data-ttu-id="65fa2-131">Este objeto es compatible con los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="65fa2-131">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="65fa2-132">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="65fa2-132">Shader Model</span></span>                                                                | <span data-ttu-id="65fa2-133">Compatible</span><span class="sxs-lookup"><span data-stu-id="65fa2-133">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="65fa2-134">Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="65fa2-134">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="65fa2-135">sí</span><span class="sxs-lookup"><span data-stu-id="65fa2-135">yes</span></span>       |



 

<span data-ttu-id="65fa2-136">Este objeto es compatible con los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="65fa2-136">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="65fa2-137">Vértice</span><span class="sxs-lookup"><span data-stu-id="65fa2-137">Vertex</span></span> | <span data-ttu-id="65fa2-138">Casco</span><span class="sxs-lookup"><span data-stu-id="65fa2-138">Hull</span></span> | <span data-ttu-id="65fa2-139">Dominio</span><span class="sxs-lookup"><span data-stu-id="65fa2-139">Domain</span></span> | <span data-ttu-id="65fa2-140">Geometría</span><span class="sxs-lookup"><span data-stu-id="65fa2-140">Geometry</span></span> | <span data-ttu-id="65fa2-141">Píxel</span><span class="sxs-lookup"><span data-stu-id="65fa2-141">Pixel</span></span> | <span data-ttu-id="65fa2-142">Compute</span><span class="sxs-lookup"><span data-stu-id="65fa2-142">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="65fa2-143">x</span><span class="sxs-lookup"><span data-stu-id="65fa2-143">x</span></span>     | <span data-ttu-id="65fa2-144">x</span><span class="sxs-lookup"><span data-stu-id="65fa2-144">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="65fa2-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="65fa2-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65fa2-146">Objetos del modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="65fa2-146">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




