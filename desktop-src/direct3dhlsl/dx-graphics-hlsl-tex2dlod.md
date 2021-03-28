---
title: tex2Dlod
description: Muestrea una textura 2D con mapas MIP. El LOD de mipmap se especifica en t.w.
ms.assetid: 689eff39-f6ac-4c25-8b92-ca68707ae8ad
keywords:
- HLSL de tex2Dlod
topic_type:
- apiref
api_name:
- tex2Dlod
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f63a922fe86dc10d984369a1a872f84089b4db34
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104983983"
---
# <a name="tex2dlod"></a><span data-ttu-id="15e51-105">tex2Dlod</span><span class="sxs-lookup"><span data-stu-id="15e51-105">tex2Dlod</span></span>

<span data-ttu-id="15e51-106">Muestrea una textura 2D con mapas MIP.</span><span class="sxs-lookup"><span data-stu-id="15e51-106">Samples a 2D texture with mipmaps.</span></span> <span data-ttu-id="15e51-107">El LOD de mipmap se especifica en t.w.</span><span class="sxs-lookup"><span data-stu-id="15e51-107">The mipmap LOD is specified in t.w.</span></span>



| <span data-ttu-id="15e51-108">RET tex2Dlod (s, t)</span><span class="sxs-lookup"><span data-stu-id="15e51-108">ret tex2Dlod(s, t)</span></span> |
|--------------------|



 

## <a name="parameters"></a><span data-ttu-id="15e51-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="15e51-109">Parameters</span></span>



| <span data-ttu-id="15e51-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="15e51-110">Item</span></span>                                                   | <span data-ttu-id="15e51-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="15e51-111">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="15e51-112"><span id="s"></span><span id="S"></span>*seg*</span><span class="sxs-lookup"><span data-stu-id="15e51-112"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="15e51-113">\[en \] el estado de la muestra.</span><span class="sxs-lookup"><span data-stu-id="15e51-113">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="15e51-114"><span id="t"></span><span id="T"></span>*h*</span><span class="sxs-lookup"><span data-stu-id="15e51-114"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="15e51-115">\[en \] la coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="15e51-115">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="15e51-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="15e51-116">Return Value</span></span>

<span data-ttu-id="15e51-117">Valor de los datos de textura.</span><span class="sxs-lookup"><span data-stu-id="15e51-117">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="15e51-118">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="15e51-118">Type Description</span></span>



| <span data-ttu-id="15e51-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="15e51-119">Name</span></span> | <span data-ttu-id="15e51-120">Entrada o salida</span><span class="sxs-lookup"><span data-stu-id="15e51-120">In/Out</span></span> | [<span data-ttu-id="15e51-121">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="15e51-121">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="15e51-122">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="15e51-122">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="15e51-123">Tamaño</span><span class="sxs-lookup"><span data-stu-id="15e51-123">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="15e51-124">s</span><span class="sxs-lookup"><span data-stu-id="15e51-124">s</span></span>    | <span data-ttu-id="15e51-125">in</span><span class="sxs-lookup"><span data-stu-id="15e51-125">in</span></span>     | [<span data-ttu-id="15e51-126">**object**</span><span class="sxs-lookup"><span data-stu-id="15e51-126">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="15e51-127">sampler2D</span><span class="sxs-lookup"><span data-stu-id="15e51-127">sampler2D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="15e51-128">1</span><span class="sxs-lookup"><span data-stu-id="15e51-128">1</span></span>    |
| <span data-ttu-id="15e51-129">t</span><span class="sxs-lookup"><span data-stu-id="15e51-129">t</span></span>    | <span data-ttu-id="15e51-130">in</span><span class="sxs-lookup"><span data-stu-id="15e51-130">in</span></span>     | [<span data-ttu-id="15e51-131">**medios**</span><span class="sxs-lookup"><span data-stu-id="15e51-131">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="15e51-132">**float**</span><span class="sxs-lookup"><span data-stu-id="15e51-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="15e51-133">4</span><span class="sxs-lookup"><span data-stu-id="15e51-133">4</span></span>    |
| <span data-ttu-id="15e51-134">direcc</span><span class="sxs-lookup"><span data-stu-id="15e51-134">ret</span></span>  | <span data-ttu-id="15e51-135">out</span><span class="sxs-lookup"><span data-stu-id="15e51-135">out</span></span>    | [<span data-ttu-id="15e51-136">**medios**</span><span class="sxs-lookup"><span data-stu-id="15e51-136">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="15e51-137">**float**</span><span class="sxs-lookup"><span data-stu-id="15e51-137">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="15e51-138">4</span><span class="sxs-lookup"><span data-stu-id="15e51-138">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="15e51-139">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="15e51-139">Minimum Shader Model</span></span>

<span data-ttu-id="15e51-140">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="15e51-140">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="15e51-141">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="15e51-141">Shader Model</span></span>                                                                       | <span data-ttu-id="15e51-142">Compatible</span><span class="sxs-lookup"><span data-stu-id="15e51-142">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="15e51-143">Modelador [modelo 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="15e51-143">[Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) and higher shader models</span></span> | <span data-ttu-id="15e51-144">sí</span><span class="sxs-lookup"><span data-stu-id="15e51-144">yes</span></span>       |
| [<span data-ttu-id="15e51-145">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="15e51-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)                          | <span data-ttu-id="15e51-146">no</span><span class="sxs-lookup"><span data-stu-id="15e51-146">no</span></span>        |
| [<span data-ttu-id="15e51-147">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="15e51-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="15e51-148">no</span><span class="sxs-lookup"><span data-stu-id="15e51-148">no</span></span>        |



 

## <a name="remarks"></a><span data-ttu-id="15e51-149">Observaciones</span><span class="sxs-lookup"><span data-stu-id="15e51-149">Remarks</span></span>

<span data-ttu-id="15e51-150">A partir de Direct3D 10, puede usar la nueva sintaxis de HLSL para tener acceso a las texturas y otros recursos.</span><span class="sxs-lookup"><span data-stu-id="15e51-150">Starting with Direct3D 10, you can use new HLSL syntax to access textures and other resources.</span></span> <span data-ttu-id="15e51-151">Puede reemplazar las funciones de búsqueda de textura de estilo intrínseco, como **tex2Dlod**, con un estilo más orientado a objetos.</span><span class="sxs-lookup"><span data-stu-id="15e51-151">You can replace intrinsic-style texture lookup functions, such as **tex2Dlod**, with a more object-oriented style.</span></span> <span data-ttu-id="15e51-152">En este estilo orientado a objetos, las texturas se desacoplan de los muestreadores y tienen métodos para cargar y realizar el muestreo.</span><span class="sxs-lookup"><span data-stu-id="15e51-152">In this object-oriented style, textures are decoupled from samplers and have methods for loading and sampling.</span></span>

<span data-ttu-id="15e51-153">Para muestrear una textura 2D, en lugar de usar **tex2Dlod** como en este código:</span><span class="sxs-lookup"><span data-stu-id="15e51-153">To sample a 2D texture, instead of using **tex2Dlod** as in this code:</span></span>


```
sampler S;
...
color = tex2Dlod(S, Location);
```



<span data-ttu-id="15e51-154">Use el método [SampleLevel](dx-graphics-hlsl-to-samplelevel.md) de un [**objeto Texture**](dx-graphics-hlsl-to-type.md) como en este código:</span><span class="sxs-lookup"><span data-stu-id="15e51-154">Use the [SampleLevel](dx-graphics-hlsl-to-samplelevel.md) method of a [**Texture Object**](dx-graphics-hlsl-to-type.md) as in this code:</span></span>


```
Texture2D MyTexture;
SamplerState MySampler;
...
color = MyTexture.SampleLevel(MySampler, Location, LOD);
```



<span data-ttu-id="15e51-155">Para usar las funciones de búsqueda de textura de estilo intrínseco, como **tex2Dlod**, con el [modelo de sombreador 4](dx-graphics-hlsl-sm4.md) y versiones posteriores, use [**D3DCOMPILE habilitar la \_ \_ \_ compatibilidad con versiones anteriores**](d3dcompile-constants.md) para compilar.</span><span class="sxs-lookup"><span data-stu-id="15e51-155">To use the intrinsic-style texture lookup functions, such as **tex2Dlod**, with [shader model 4](dx-graphics-hlsl-sm4.md) and higher, use [**D3DCOMPILE\_ENABLE\_BACKWARDS\_COMPATIBILITY**](d3dcompile-constants.md) to compile.</span></span> <span data-ttu-id="15e51-156">Sin embargo, si desea tener como destino el modelo de sombreador 4 y superior (incluso [ \* \_ 4 \_ 0 de \_ nivel \_ 9 \_ \* ](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro)) con código de estilo orientado a objetos más reciente, migre a la sintaxis de HLSL más reciente.</span><span class="sxs-lookup"><span data-stu-id="15e51-156">However, if you want to target shader model 4 and higher (even [\*\_4\_0\_level\_9\_\*](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro)) with newer object-oriented style code, migrate to the newer HLSL syntax.</span></span>

## <a name="see-also"></a><span data-ttu-id="15e51-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="15e51-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15e51-158">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="15e51-158">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

