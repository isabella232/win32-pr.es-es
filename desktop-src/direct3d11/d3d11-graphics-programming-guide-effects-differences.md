---
title: Diferencias entre efectos 10 y efectos 11
description: En este tema se muestran las diferencias entre los efectos 10 y 11.
ms.assetid: c3e5e6bc-c544-49ee-b6d9-021ce87f9b12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29af1b9e7aec72f96a62e0f62668b81a6eec8367
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792322"
---
# <a name="differences-between-effects-10-and-effects-11"></a><span data-ttu-id="fbba9-103">Diferencias entre efectos 10 y efectos 11</span><span class="sxs-lookup"><span data-stu-id="fbba9-103">Differences Between Effects 10 and Effects 11</span></span>

<span data-ttu-id="fbba9-104">En este tema se muestran las diferencias entre los efectos 10 y 11.</span><span class="sxs-lookup"><span data-stu-id="fbba9-104">This topic shows the differences between Effects 10 and Effects 11.</span></span>

## <a name="device-contexts-threading-and-cloning"></a><span data-ttu-id="fbba9-105">Contextos de dispositivo, subprocesos y clonación</span><span class="sxs-lookup"><span data-stu-id="fbba9-105">Device Contexts, Threading, and Cloning</span></span>

<span data-ttu-id="fbba9-106">La interfaz ID3D10Device se ha dividido en dos interfaces en Direct3D 11: ID3D11Device y ID3D11DeviceContext.</span><span class="sxs-lookup"><span data-stu-id="fbba9-106">The ID3D10Device interface has been split into two interfaces in Direct3D 11: ID3D11Device and ID3D11DeviceContext.</span></span> <span data-ttu-id="fbba9-107">Puede crear varios ID3D11DeviceContexts para facilitar la ejecución simultánea en varios subprocesos.</span><span class="sxs-lookup"><span data-stu-id="fbba9-107">You can create multiple ID3D11DeviceContexts to facilitate concurrent execution on multiple threads.</span></span> <span data-ttu-id="fbba9-108">Effects 11 extiende este concepto al marco de trabajo de efectos.</span><span class="sxs-lookup"><span data-stu-id="fbba9-108">Effects 11 extends this concept to the Effects framework.</span></span>

<span data-ttu-id="fbba9-109">Los efectos 11 en tiempo de ejecución son de un solo subproceso.</span><span class="sxs-lookup"><span data-stu-id="fbba9-109">The Effects 11 runtime is single-threaded.</span></span> <span data-ttu-id="fbba9-110">Por esta razón, no debe utilizar una única instancia de ID3DX11Effect con varios subprocesos simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="fbba9-110">For this reason, you should not use a single ID3DX11Effect instance with multiple threads concurrently.</span></span>

<span data-ttu-id="fbba9-111">Para usar el tiempo de ejecución de Effects 11 en varias instancias, debe crear instancias de ID3DX11Effect independientes.</span><span class="sxs-lookup"><span data-stu-id="fbba9-111">To use the Effects 11 runtime on multiple instances, you must create separate ID3DX11Effect instances.</span></span> <span data-ttu-id="fbba9-112">Dado que ID3D11DeviceContext también es de subproceso único, debe pasar instancias de ID3D11DeviceContext diferentes a cada instancia de Effect en Apply.</span><span class="sxs-lookup"><span data-stu-id="fbba9-112">Because the ID3D11DeviceContext is also single-threaded, you should pass different ID3D11DeviceContext instances to each effect instance on Apply.</span></span> <span data-ttu-id="fbba9-113">Puede usar estos contextos de dispositivo independientes para crear listas de comandos de forma que el subproceso de representación pueda aplicarlos en el contexto de dispositivo inmediato.</span><span class="sxs-lookup"><span data-stu-id="fbba9-113">You can use these separate device contexts to create command lists so that the rendering thread can apply them on the immediate device context.</span></span>

<span data-ttu-id="fbba9-114">La forma más fácil de crear varios efectos que encapsulan la misma funcionalidad, para su uso en varios subprocesos, es crear un efecto y luego hacer copias clonadas.</span><span class="sxs-lookup"><span data-stu-id="fbba9-114">The easiest way to create multiple effects that encapsulate the same functionality, for use on multiple threads, is to create one effect and then make cloned copies.</span></span> <span data-ttu-id="fbba9-115">La clonación presenta las siguientes ventajas en comparación con la creación de varias copias desde cero:</span><span class="sxs-lookup"><span data-stu-id="fbba9-115">Cloning has the following advantages over creating multiple copies from scratch:</span></span>

1.  <span data-ttu-id="fbba9-116">La rutina de clonación es más rápida que la rutina de creación.</span><span class="sxs-lookup"><span data-stu-id="fbba9-116">The cloning routine is faster than the creation routine.</span></span>
2.  <span data-ttu-id="fbba9-117">Los efectos clonados comparten los sombreadores creados, los bloques de estado y las instancias de clase (por lo que no es necesario volver a crearlos).</span><span class="sxs-lookup"><span data-stu-id="fbba9-117">Cloned effects share created shaders, state blocks, and class instances (so they don't have to be recreated).</span></span>
3.  <span data-ttu-id="fbba9-118">Los efectos clonados pueden compartir búferes de constantes.</span><span class="sxs-lookup"><span data-stu-id="fbba9-118">Cloned effects can share constant buffers.</span></span>
4.  <span data-ttu-id="fbba9-119">Los efectos clonados comienzan con el estado que coincide con el efecto actual (valores de variable, tanto si se ha optimizado como si no).</span><span class="sxs-lookup"><span data-stu-id="fbba9-119">Cloned effects begin with state that matches the current effect (variable values, whether or not it has been optimized).</span></span>

<span data-ttu-id="fbba9-120">Consulte [clonar un efecto](d3d11-graphics-programming-guide-effects-cloning.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="fbba9-120">See [Cloning an Effect](d3d11-graphics-programming-guide-effects-cloning.md) for more information.</span></span>

## <a name="effect-pools-and-groups"></a><span data-ttu-id="fbba9-121">Grupos de efectos y grupos</span><span class="sxs-lookup"><span data-stu-id="fbba9-121">Effect Pools and Groups</span></span>

<span data-ttu-id="fbba9-122">Con diferencia el uso más frecuente de los grupos de efectos en Direct3D 10 era para agrupar materiales.</span><span class="sxs-lookup"><span data-stu-id="fbba9-122">By far the most prevalent use of effect pools in Direct3D 10 was for grouping materials.</span></span> <span data-ttu-id="fbba9-123">Los grupos de efectos se han quitado de los efectos 11 y se han agregado grupos, que es un método más eficaz de agrupación de materiales.</span><span class="sxs-lookup"><span data-stu-id="fbba9-123">Effect Pools have been removed from Effects 11 and groups have been added, which is a more efficient method of grouping materials.</span></span>

<span data-ttu-id="fbba9-124">Un grupo de efectos es simplemente un conjunto de técnicas.</span><span class="sxs-lookup"><span data-stu-id="fbba9-124">An effect group is simply a set of techniques.</span></span> <span data-ttu-id="fbba9-125">Consulte [Sintaxis de grupo de efectos (Direct3D 11)](d3d11-effect-group-syntax.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="fbba9-125">See [Effect Group Syntax (Direct3D 11)](d3d11-effect-group-syntax.md) for more information.</span></span>

<span data-ttu-id="fbba9-126">Considere la siguiente jerarquía de efectos con cuatro efectos secundarios y un grupo de efectos:</span><span class="sxs-lookup"><span data-stu-id="fbba9-126">Consider the following effect hierarchy with four child effects and one effect pool:</span></span>


```
// Effect Pool
cbufer A { ... }
PixelShader pPSGrass;
PixelShader pPSWater;

// Effect Child 1
#include "EffectPool.fx"
technique10 GrassMaterialLowSpec { ... }

// Effect Child 2
#include "EffectPool.fx"
technique10 GrassMaterialHighSpec { ... }

// Effect Child 3
#include "EffectPool.fx"
technique10 WaterMaterialLowSpec { ... }

// Effect Child 4
#include "EffectPool.fx"
technique10 WaterMaterialHighSpec { ... }
```



<span data-ttu-id="fbba9-127">Puede lograr la misma funcionalidad en Effects 11 mediante el uso de grupos:</span><span class="sxs-lookup"><span data-stu-id="fbba9-127">You can achieve the same functionality in Effects 11 by using groups:</span></span>


```
cbufer A { ... }
PixelShader pPSGrass;
PixelShader pPSWater;

fxgroup GrassMaterial
{
    technique10 LowSpec { ... }
    technique10 HighSpec { ... }
}

fxgroup WaterMaterial
{
    technique10 LowSpec { ... }
    technique10 HighSpec { ... }
}
```



## <a name="new-shader-stages"></a><span data-ttu-id="fbba9-128">Nuevas etapas del sombreador</span><span class="sxs-lookup"><span data-stu-id="fbba9-128">New Shader Stages</span></span>

<span data-ttu-id="fbba9-129">Hay tres nuevas fases del sombreador en Direct3D 11: el sombreador de casco, el sombreador de dominios y el sombreador de proceso.</span><span class="sxs-lookup"><span data-stu-id="fbba9-129">There are three new shader stages in Direct3D 11: the hull shader, domain shader, and compute shader.</span></span> <span data-ttu-id="fbba9-130">Los efectos 11 lo controlan de manera similar a los sombreadores de vértices, los sombreadores de geometría y los sombreadores de píxeles.</span><span class="sxs-lookup"><span data-stu-id="fbba9-130">Effects 11 handles these in a similar manner to vertex shaders, geometry shaders, and pixel shaders.</span></span>

<span data-ttu-id="fbba9-131">Se han agregado tres nuevos tipos de variables a Effects 11:</span><span class="sxs-lookup"><span data-stu-id="fbba9-131">Three new variable types have been added to Effects 11:</span></span>

-   <span data-ttu-id="fbba9-132">HullShader</span><span class="sxs-lookup"><span data-stu-id="fbba9-132">HullShader</span></span>
-   <span data-ttu-id="fbba9-133">DomainShader</span><span class="sxs-lookup"><span data-stu-id="fbba9-133">DomainShader</span></span>
-   <span data-ttu-id="fbba9-134">ComputeShader</span><span class="sxs-lookup"><span data-stu-id="fbba9-134">ComputeShader</span></span>

<span data-ttu-id="fbba9-135">Si usa estos sombreadores en una técnica, debe etiquetar esa técnica "technique11" y no "technique10".</span><span class="sxs-lookup"><span data-stu-id="fbba9-135">If you use these shaders in a technique, you must label that technique "technique11", and not "technique10".</span></span> <span data-ttu-id="fbba9-136">El sombreador de cálculo no se puede establecer en el mismo paso que cualquier otro estado de gráficos (otros sombreadores, bloques de estado o destinos de representación).</span><span class="sxs-lookup"><span data-stu-id="fbba9-136">The compute shader cannot be set in the same pass as any other graphics state (other shaders, state blocks, or render targets).</span></span>

## <a name="new-texture-types"></a><span data-ttu-id="fbba9-137">Nuevos tipos de textura</span><span class="sxs-lookup"><span data-stu-id="fbba9-137">New Texture Types</span></span>

<span data-ttu-id="fbba9-138">Direct3D 11 admite los siguientes tipos de textura:</span><span class="sxs-lookup"><span data-stu-id="fbba9-138">Direct3D 11 supports the following texture types:</span></span>

-   [<span data-ttu-id="fbba9-139">AppendStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="fbba9-139">AppendStructuredBuffer</span></span>](/windows/desktop/direct3dhlsl/sm5-object-appendstructuredbuffer)
-   [<span data-ttu-id="fbba9-140">ByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="fbba9-140">ByteAddressBuffer</span></span>](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer)
-   [<span data-ttu-id="fbba9-141">ConsumeStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="fbba9-141">ConsumeStructuredBuffer</span></span>](/windows/desktop/direct3dhlsl/sm5-object-consumestructuredbuffer)
-   [<span data-ttu-id="fbba9-142">StructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="fbba9-142">StructuredBuffer</span></span>](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer)

## <a name="unordered-access-views"></a><span data-ttu-id="fbba9-143">Vistas de acceso desordenado</span><span class="sxs-lookup"><span data-stu-id="fbba9-143">Unordered Access Views</span></span>

<span data-ttu-id="fbba9-144">Effects 11 permite obtener y establecer los nuevos tipos de vistas de acceso desordenado.</span><span class="sxs-lookup"><span data-stu-id="fbba9-144">Effects 11 supports getting and setting the new unordered access view types.</span></span> <span data-ttu-id="fbba9-145">Esto funciona de forma similar a las texturas.</span><span class="sxs-lookup"><span data-stu-id="fbba9-145">This works in a similar manner as textures.</span></span>

<span data-ttu-id="fbba9-146">Considere este ejemplo de efectos HLSL:</span><span class="sxs-lookup"><span data-stu-id="fbba9-146">Consider this Effects HLSL example:</span></span>


```
  
RWTexture1D<float> myUAV;
```



<span data-ttu-id="fbba9-147">Puede establecer esta variable en C++ de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="fbba9-147">You can set this variable in C++ as follows:</span></span>


```
  
ID3D11UnorderedAccessView* pUAVTexture1D = NULL;
ID3DX11EffectUnorderedAccessViewVariable* pUAVVar;
pUAVVar = pEffect->GetVariableByName("myUAV")->AsUnorderedAccessView();
pUAVVar->SetUnorderedAccessView( pUAVTexture1D );
```



<span data-ttu-id="fbba9-148">Direct3D 11 admite los siguientes tipos de vistas de acceso desordenado:</span><span class="sxs-lookup"><span data-stu-id="fbba9-148">Direct3D 11 supports the following unordered access view types:</span></span>

-   <span data-ttu-id="fbba9-149">RWBuffer</span><span class="sxs-lookup"><span data-stu-id="fbba9-149">RWBuffer</span></span>
-   <span data-ttu-id="fbba9-150">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="fbba9-150">RWByteAddressBuffer</span></span>
-   <span data-ttu-id="fbba9-151">RWStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="fbba9-151">RWStructuredBuffer</span></span>
-   <span data-ttu-id="fbba9-152">RWTexture1D</span><span class="sxs-lookup"><span data-stu-id="fbba9-152">RWTexture1D</span></span>
-   <span data-ttu-id="fbba9-153">RWTexture1DArray</span><span class="sxs-lookup"><span data-stu-id="fbba9-153">RWTexture1DArray</span></span>
-   <span data-ttu-id="fbba9-154">RWTexture2D</span><span class="sxs-lookup"><span data-stu-id="fbba9-154">RWTexture2D</span></span>
-   <span data-ttu-id="fbba9-155">RWTexture2DArray</span><span class="sxs-lookup"><span data-stu-id="fbba9-155">RWTexture2DArray</span></span>
-   <span data-ttu-id="fbba9-156">RWTexture3D</span><span class="sxs-lookup"><span data-stu-id="fbba9-156">RWTexture3D</span></span>

## <a name="interfaces-and-class-instances"></a><span data-ttu-id="fbba9-157">Interfaces e instancias de clase</span><span class="sxs-lookup"><span data-stu-id="fbba9-157">Interfaces and Class Instances</span></span>

<span data-ttu-id="fbba9-158">Para ver la sintaxis de la interfaz y la clase, consulte [interfaces y clases](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking-class).</span><span class="sxs-lookup"><span data-stu-id="fbba9-158">For interface and class syntax, see [Interfaces and Classes](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking-class).</span></span>

<span data-ttu-id="fbba9-159">Para usar interfaces y clases en efectos, vea [interfaces y clases en efectos](d3d11-graphics-programming-guide-effects-interfaces-and-classes.md).</span><span class="sxs-lookup"><span data-stu-id="fbba9-159">For using interfaces and classes in effects, see [Interfaces and Classes in Effects](d3d11-graphics-programming-guide-effects-interfaces-and-classes.md).</span></span>

## <a name="addressable-stream-out"></a><span data-ttu-id="fbba9-160">Transmisión por secuencias direccionable</span><span class="sxs-lookup"><span data-stu-id="fbba9-160">Addressable Stream Out</span></span>

<span data-ttu-id="fbba9-161">En Direct3D 10, los sombreadores de geometría pueden generar un flujo de datos a la unidad de salida de la secuencia y la unidad de rasterizador.</span><span class="sxs-lookup"><span data-stu-id="fbba9-161">In Direct3D 10, geometry shaders could output one stream of data to the stream output unit and the rasterizer unit.</span></span> <span data-ttu-id="fbba9-162">En Direct3D 11, los sombreadores de geometría pueden generar hasta cuatro flujos de datos en la unidad de salida de flujo y, como máximo, uno de esos flujos en la unidad de rasterizador.</span><span class="sxs-lookup"><span data-stu-id="fbba9-162">In Direct3D11, geometry shaders can output up to four streams of data to the stream output unit, and at most one of those streams to the rasterizer unit.</span></span> <span data-ttu-id="fbba9-163">El intrínseco **ConstructGSWithSO** se ha actualizado para reflejar esta nueva funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="fbba9-163">The **ConstructGSWithSO** intrinsic has been updated to reflect this new functionality.</span></span>

<span data-ttu-id="fbba9-164">Consulte [Sintaxis de Stream out](d3d11-graphics-reference-effect-streamout.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="fbba9-164">See [Stream Out Syntax](d3d11-graphics-reference-effect-streamout.md) for more information.</span></span>

## <a name="setting-and-unsetting-device-state"></a><span data-ttu-id="fbba9-165">Establecer y desconfigurar el estado del dispositivo</span><span class="sxs-lookup"><span data-stu-id="fbba9-165">Setting and Unsetting Device State</span></span>

<span data-ttu-id="fbba9-166">En los efectos 10, podría crear búferes de constantes y búferes de texturas administrados por el usuario mediante las funciones [**ID3D10EffectConstantBuffer:: SetConstantBuffer**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-setconstantbuffer) y [**SetTextureBuffer**](id3dx11effectconstantbuffer-settexturebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="fbba9-166">In Effects 10, you could make constant buffers and texture buffers user-managed by using the [**ID3D10EffectConstantBuffer::SetConstantBuffer**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-setconstantbuffer) and [**SetTextureBuffer**](id3dx11effectconstantbuffer-settexturebuffer.md) functions.</span></span> <span data-ttu-id="fbba9-167">Después de llamar a estas funciones, el tiempo de ejecución de los efectos 10 deja de administrar el búfer de constantes o el búfer de textura y el usuario debe rellenar los datos mediante la interfaz ID3D10Device.</span><span class="sxs-lookup"><span data-stu-id="fbba9-167">After you call these functions, the Effects 10 runtime no longer manages the constant buffer or texture buffer and the user must fill the data by using the ID3D10Device interface.</span></span>

<span data-ttu-id="fbba9-168">En Effects 11, también puede hacer que los bloques de estado (estado de Blend, estado de rasterizador, estado de estarcido de profundidad y estado de muestra) se administren mediante el uso de las siguientes llamadas:</span><span class="sxs-lookup"><span data-stu-id="fbba9-168">In Effects 11, you can also make the state blocks (blend state, rasterizer state, depth-stencil state, and sampler state) user-managed by using the following calls:</span></span>

-   [<span data-ttu-id="fbba9-169">**ID3DX11EffectBlendVariable::SetBlendState**</span><span class="sxs-lookup"><span data-stu-id="fbba9-169">**ID3DX11EffectBlendVariable::SetBlendState**</span></span>](id3dx11effectblendvariable-setblendstate.md)
-   [<span data-ttu-id="fbba9-170">**ID3DX11EffectRasterizerVariable::SetRasterizerState**</span><span class="sxs-lookup"><span data-stu-id="fbba9-170">**ID3DX11EffectRasterizerVariable::SetRasterizerState**</span></span>](id3dx11effectrasterizervariable-setrasterizerstate.md)
-   [<span data-ttu-id="fbba9-171">**ID3DX11EffectDepthStencilVariable::SetDepthStencilState**</span><span class="sxs-lookup"><span data-stu-id="fbba9-171">**ID3DX11EffectDepthStencilVariable::SetDepthStencilState**</span></span>](id3dx11effectdepthstencilvariable-setdepthstencilstate.md)
-   [<span data-ttu-id="fbba9-172">**ID3DX11EffectSamplerVariable::SetSampler**</span><span class="sxs-lookup"><span data-stu-id="fbba9-172">**ID3DX11EffectSamplerVariable::SetSampler**</span></span>](id3dx11effectsamplervariable-setsampler.md)

<span data-ttu-id="fbba9-173">Después de llamar a estas funciones, el tiempo de ejecución de Effects 11 ya no administra las variables de bloque de estado y los valores permanecerán sin cambios.</span><span class="sxs-lookup"><span data-stu-id="fbba9-173">After you call these functions, the Effects 11 runtime no longer manages the state block variables, and there values will remain unchanged.</span></span> <span data-ttu-id="fbba9-174">Tenga en cuenta que, dado que los bloques de estado son inmutables, el usuario debe establecer un nuevo bloque de estado para cambiar los valores.</span><span class="sxs-lookup"><span data-stu-id="fbba9-174">Note that because state blocks are immutable, the user must set a new state block to change the values.</span></span>

<span data-ttu-id="fbba9-175">También puede revertir los búferes de constantes, los búferes de textura y los bloques de estado al estado no administrado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="fbba9-175">You can also revert constant buffers, texture buffers, and state blocks to the non-user managed state.</span></span> <span data-ttu-id="fbba9-176">Si no establece estas variables, el tiempo de ejecución de Effects 11 continuará actualizarlas cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="fbba9-176">If you unset these variables, the Effects 11 runtime will continue to update them when necessary.</span></span> <span data-ttu-id="fbba9-177">Puede utilizar las siguientes llamadas para no establecer las variables administradas por el usuario:</span><span class="sxs-lookup"><span data-stu-id="fbba9-177">You can use the following calls to unset user managed variables:</span></span>

-   [<span data-ttu-id="fbba9-178">**ID3DX11EffectConstantBuffer::UndoSetConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="fbba9-178">**ID3DX11EffectConstantBuffer::UndoSetConstantBuffer**</span></span>](id3dx11effectconstantbuffer-undosetconstantbuffer.md)
-   [<span data-ttu-id="fbba9-179">**ID3DX11EffectConstantBuffer::UndoSetTextureBuffer**</span><span class="sxs-lookup"><span data-stu-id="fbba9-179">**ID3DX11EffectConstantBuffer::UndoSetTextureBuffer**</span></span>](id3dx11effectconstantbuffer-undosettexturebuffer.md)
-   [<span data-ttu-id="fbba9-180">**ID3DX11EffectBlendVariable::UndoSetBlendState**</span><span class="sxs-lookup"><span data-stu-id="fbba9-180">**ID3DX11EffectBlendVariable::UndoSetBlendState**</span></span>](id3dx11effectblendvariable-undosetblendstate.md)
-   [<span data-ttu-id="fbba9-181">**ID3DX11EffectRasterizerVariable::UndoSetRasterizerState**</span><span class="sxs-lookup"><span data-stu-id="fbba9-181">**ID3DX11EffectRasterizerVariable::UndoSetRasterizerState**</span></span>](id3dx11effectrasterizervariable-undosetrasterizerstate.md)
-   [<span data-ttu-id="fbba9-182">**ID3DX11EffectDepthStencilVariable::UndoSetDepthStencilState**</span><span class="sxs-lookup"><span data-stu-id="fbba9-182">**ID3DX11EffectDepthStencilVariable::UndoSetDepthStencilState**</span></span>](id3dx11effectdepthstencilvariable-undosetdepthstencilstate.md)
-   [<span data-ttu-id="fbba9-183">**ID3DX11EffectSamplerVariable::UndoSetSampler**</span><span class="sxs-lookup"><span data-stu-id="fbba9-183">**ID3DX11EffectSamplerVariable::UndoSetSampler**</span></span>](id3dx11effectsamplervariable-undosetsampler.md)

## <a name="effects-virtual-machine"></a><span data-ttu-id="fbba9-184">Efectos de la máquina virtual</span><span class="sxs-lookup"><span data-stu-id="fbba9-184">Effects Virtual Machine</span></span>

<span data-ttu-id="fbba9-185">Se ha quitado la máquina virtual de efectos, que evaluó expresiones complejas fuera de las funciones.</span><span class="sxs-lookup"><span data-stu-id="fbba9-185">The effects virtual machine, which evaluated complex expressions outside of functions, has been removed.</span></span>

<span data-ttu-id="fbba9-186">No se admiten los siguientes ejemplos de expresiones complejas:</span><span class="sxs-lookup"><span data-stu-id="fbba9-186">The following examples of complex expressions are not supported:</span></span>

1.  <span data-ttu-id="fbba9-187">SetPixelShader (myPSArray (i \* 3 + j));</span><span class="sxs-lookup"><span data-stu-id="fbba9-187">SetPixelShader( myPSArray( i \* 3 + j ) );</span></span>
2.  <span data-ttu-id="fbba9-188">SetPixelShader (myPSArray ((float) i);</span><span class="sxs-lookup"><span data-stu-id="fbba9-188">SetPixelShader( myPSArray( (float)i );</span></span>
3.  <span data-ttu-id="fbba9-189">FILTRO = i + 2;</span><span class="sxs-lookup"><span data-stu-id="fbba9-189">FILTER = i + 2;</span></span>

<span data-ttu-id="fbba9-190">Se admiten los siguientes ejemplos de expresiones no complejas:</span><span class="sxs-lookup"><span data-stu-id="fbba9-190">The following examples of non-complex expressions are supported:</span></span>

1.  <span data-ttu-id="fbba9-191">SetPixelShader( myPS );</span><span class="sxs-lookup"><span data-stu-id="fbba9-191">SetPixelShader( myPS );</span></span>
2.  <span data-ttu-id="fbba9-192">SetPixelShader (myPS \[ i \] );</span><span class="sxs-lookup"><span data-stu-id="fbba9-192">SetPixelShader( myPS\[i\] );</span></span>
3.  <span data-ttu-id="fbba9-193">SetPixelShader (myPS \[ uIndex \] );//uIndex es una variable uint</span><span class="sxs-lookup"><span data-stu-id="fbba9-193">SetPixelShader( myPS\[ uIndex \] ); // uIndex is a uint variable</span></span>
4.  <span data-ttu-id="fbba9-194">FILTRO = i;</span><span class="sxs-lookup"><span data-stu-id="fbba9-194">FILTER = i;</span></span>
5.  <span data-ttu-id="fbba9-195">FILTER = ANISOTRÓPICO;</span><span class="sxs-lookup"><span data-stu-id="fbba9-195">FILTER = ANISOTROPIC;</span></span>

<span data-ttu-id="fbba9-196">Estas expresiones pueden aparecer en expresiones de bloque de estado (como FILTER) y expresiones Pass (como SetPixelShader).</span><span class="sxs-lookup"><span data-stu-id="fbba9-196">These expressions could appear in state block expressions (such as FILTER) and pass expressions (such as SetPixelShader).</span></span>

## <a name="source-availability-and-location"></a><span data-ttu-id="fbba9-197">Disponibilidad y ubicación de origen</span><span class="sxs-lookup"><span data-stu-id="fbba9-197">Source Availability and Location</span></span>

<span data-ttu-id="fbba9-198">Los efectos 10 se distribuyeron en D3D10.dll.</span><span class="sxs-lookup"><span data-stu-id="fbba9-198">Effects 10 was distributed in D3D10.dll.</span></span> <span data-ttu-id="fbba9-199">Effects 11 se distribuye como Source, con las soluciones de Visual Studio correspondientes para compilarlo.</span><span class="sxs-lookup"><span data-stu-id="fbba9-199">Effects 11 is distributed as source, with corresponding Visual Studio solutions to compile it.</span></span> <span data-ttu-id="fbba9-200">Al crear aplicaciones de tipo Effects, se recomienda incluir directamente los efectos 11 en esas aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="fbba9-200">When you create effects-type applications, we recommend that you include the Effects 11 source directly in those applications.</span></span>

<span data-ttu-id="fbba9-201">Puede obtener los efectos 11 de [Effects para la actualización de Direct3D 11](https://github.com/Microsoft/FX11).</span><span class="sxs-lookup"><span data-stu-id="fbba9-201">You can get Effects 11 from [Effects for Direct3D 11 Update](https://github.com/Microsoft/FX11).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fbba9-202">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fbba9-202">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fbba9-203">Efectos (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="fbba9-203">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 