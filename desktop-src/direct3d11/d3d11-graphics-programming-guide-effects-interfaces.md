---
title: Interfaces del sistema de efectos (Direct3D 11)
description: El sistema de efectos define varias interfaces para administrar el estado del efecto.
ms.assetid: 5cba6055-d153-4837-9a08-96efbde5f48f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af76a54be06e52e320743ca945abb31d1d50d213
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774082"
---
# <a name="effect-system-interfaces-direct3d-11"></a><span data-ttu-id="2ae3c-103">Interfaces del sistema de efectos (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="2ae3c-103">Effect System Interfaces (Direct3D 11)</span></span>

<span data-ttu-id="2ae3c-104">El sistema de efectos define varias interfaces para administrar el estado del efecto.</span><span class="sxs-lookup"><span data-stu-id="2ae3c-104">The effect system defines several interfaces for managing effect state.</span></span> <span data-ttu-id="2ae3c-105">Hay dos tipos de interfaces: las utilizadas por el motor en tiempo de ejecución para representar un efecto e interfaces de reflexión para obtener y establecer las variables de efecto.</span><span class="sxs-lookup"><span data-stu-id="2ae3c-105">There are two types of interfaces: those used by the runtime to render an effect and reflection interfaces for getting and setting effect variables.</span></span>

-   [<span data-ttu-id="2ae3c-106">Interfaces en tiempo de ejecución de efectos</span><span class="sxs-lookup"><span data-stu-id="2ae3c-106">Effect Runtime Interfaces</span></span>](#effect-runtime-interfaces)
-   [<span data-ttu-id="2ae3c-107">Interfaces de reflexión de efectos</span><span class="sxs-lookup"><span data-stu-id="2ae3c-107">Effect Reflection Interfaces</span></span>](#effect-reflection-interfaces)

## <a name="effect-runtime-interfaces"></a><span data-ttu-id="2ae3c-108">Interfaces en tiempo de ejecución de efectos</span><span class="sxs-lookup"><span data-stu-id="2ae3c-108">Effect Runtime Interfaces</span></span>

<span data-ttu-id="2ae3c-109">Usar interfaces en tiempo de ejecución para representar un efecto.</span><span class="sxs-lookup"><span data-stu-id="2ae3c-109">Use runtime interfaces to render an effect.</span></span>



| <span data-ttu-id="2ae3c-110">Interfaces en tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="2ae3c-110">Runtime Interfaces</span></span>                                       | <span data-ttu-id="2ae3c-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="2ae3c-111">Description</span></span>                                                    |
|----------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="2ae3c-112">**ID3DX11Effect**</span><span class="sxs-lookup"><span data-stu-id="2ae3c-112">**ID3DX11Effect**</span></span>](id3dx11effect.md)                   | <span data-ttu-id="2ae3c-113">Colección de uno o más grupos y técnicas para la representación.</span><span class="sxs-lookup"><span data-stu-id="2ae3c-113">Collection of one or more groups and techniques for rendering.</span></span> |
| [<span data-ttu-id="2ae3c-114">**ID3DX11EffectPass**</span><span class="sxs-lookup"><span data-stu-id="2ae3c-114">**ID3DX11EffectPass**</span></span>](id3dx11effectpass.md)           | <span data-ttu-id="2ae3c-115">Colección de asignaciones de estado.</span><span class="sxs-lookup"><span data-stu-id="2ae3c-115">A collection of state assignments.</span></span>                             |
| [<span data-ttu-id="2ae3c-116">**ID3DX11EffectTechnique**</span><span class="sxs-lookup"><span data-stu-id="2ae3c-116">**ID3DX11EffectTechnique**</span></span>](id3dx11effecttechnique.md) | <span data-ttu-id="2ae3c-117">Colección de uno o más pasos.</span><span class="sxs-lookup"><span data-stu-id="2ae3c-117">A collection of one or more passes.</span></span>                            |
| [<span data-ttu-id="2ae3c-118">**ID3DX11EffectGroup**</span><span class="sxs-lookup"><span data-stu-id="2ae3c-118">**ID3DX11EffectGroup**</span></span>](id3dx11effectgroup.md)         | <span data-ttu-id="2ae3c-119">Colección de una o más técnicas.</span><span class="sxs-lookup"><span data-stu-id="2ae3c-119">A collection of one or more techniques.</span></span>                        |



 

## <a name="effect-reflection-interfaces"></a><span data-ttu-id="2ae3c-120">Interfaces de reflexión de efectos</span><span class="sxs-lookup"><span data-stu-id="2ae3c-120">Effect Reflection Interfaces</span></span>

<span data-ttu-id="2ae3c-121">La reflexión se implementa en el sistema de efectos para admitir el estado del efecto de lectura (y escritura).</span><span class="sxs-lookup"><span data-stu-id="2ae3c-121">Reflection is implemented in the effect system to support reading (and writing) effect state.</span></span> <span data-ttu-id="2ae3c-122">Hay varias maneras de tener acceso a las variables de efecto.</span><span class="sxs-lookup"><span data-stu-id="2ae3c-122">There are multiple ways to access effect variables.</span></span>

### <a name="setting-groups-of-effect-state"></a><span data-ttu-id="2ae3c-123">Configuración de grupos de estado de efecto</span><span class="sxs-lookup"><span data-stu-id="2ae3c-123">Setting Groups of Effect State</span></span>

<span data-ttu-id="2ae3c-124">Use estas interfaces para obtener y establecer un grupo de estado.</span><span class="sxs-lookup"><span data-stu-id="2ae3c-124">Use these interfaces to get and set a group of state.</span></span>



| <span data-ttu-id="2ae3c-125">Interfaces de reflexión</span><span class="sxs-lookup"><span data-stu-id="2ae3c-125">Reflection Interfaces</span></span>                                                          | <span data-ttu-id="2ae3c-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="2ae3c-126">Description</span></span>                      |
|--------------------------------------------------------------------------------|----------------------------------|
| [<span data-ttu-id="2ae3c-127">**ID3DX11EffectBlendVariable**</span><span class="sxs-lookup"><span data-stu-id="2ae3c-127">**ID3DX11EffectBlendVariable**</span></span>](id3dx11effectblendvariable.md)               | <span data-ttu-id="2ae3c-128">Obtiene y establece el estado de Blend.</span><span class="sxs-lookup"><span data-stu-id="2ae3c-128">Get and set blend state.</span></span>         |
| [<span data-ttu-id="2ae3c-129">**ID3DX11EffectDepthStencilVariable**</span><span class="sxs-lookup"><span data-stu-id="2ae3c-129">**ID3DX11EffectDepthStencilVariable**</span></span>](id3dx11effectdepthstencilvariable.md) | <span data-ttu-id="2ae3c-130">Obtiene y establece el estado de la galería de símbolos de profundidad.</span><span class="sxs-lookup"><span data-stu-id="2ae3c-130">Get and set depth-stencil state.</span></span> |
| [<span data-ttu-id="2ae3c-131">**ID3DX11EffectRasterizerVariable**</span><span class="sxs-lookup"><span data-stu-id="2ae3c-131">**ID3DX11EffectRasterizerVariable**</span></span>](id3dx11effectrasterizervariable.md)     | <span data-ttu-id="2ae3c-132">Obtiene y establece el estado del rasterizador.</span><span class="sxs-lookup"><span data-stu-id="2ae3c-132">Get and set rasterizer state.</span></span>    |
| [<span data-ttu-id="2ae3c-133">**ID3DX11EffectSamplerVariable**</span><span class="sxs-lookup"><span data-stu-id="2ae3c-133">**ID3DX11EffectSamplerVariable**</span></span>](id3dx11effectsamplervariable.md)           | <span data-ttu-id="2ae3c-134">Obtiene y establece el estado del muestrario.</span><span class="sxs-lookup"><span data-stu-id="2ae3c-134">Get and set sampler state.</span></span>       |



 

### <a name="setting-effect-resources"></a><span data-ttu-id="2ae3c-135">Configuración de recursos de efectos</span><span class="sxs-lookup"><span data-stu-id="2ae3c-135">Setting Effect Resources</span></span>

<span data-ttu-id="2ae3c-136">Use estas interfaces para obtener y establecer recursos.</span><span class="sxs-lookup"><span data-stu-id="2ae3c-136">Use these interfaces to get and set resources.</span></span>



| <span data-ttu-id="2ae3c-137">Interfaces de reflexión</span><span class="sxs-lookup"><span data-stu-id="2ae3c-137">Reflection Interfaces</span></span>                                                                        | <span data-ttu-id="2ae3c-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="2ae3c-138">Description</span></span>                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [<span data-ttu-id="2ae3c-139">**ID3DX11EffectConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="2ae3c-139">**ID3DX11EffectConstantBuffer**</span></span>](id3dx11effectconstantbuffer.md)                           | <span data-ttu-id="2ae3c-140">Acceder a los datos en un búfer de textura o en un búfer de constantes.</span><span class="sxs-lookup"><span data-stu-id="2ae3c-140">Access data in a texture buffer or constant buffer.</span></span> |
| [<span data-ttu-id="2ae3c-141">**ID3DX11EffectDepthStencilViewVariable**</span><span class="sxs-lookup"><span data-stu-id="2ae3c-141">**ID3DX11EffectDepthStencilViewVariable**</span></span>](id3dx11effectdepthstencilviewvariable.md)       | <span data-ttu-id="2ae3c-142">Acceder a los datos en un recurso de estarcido de profundidad.</span><span class="sxs-lookup"><span data-stu-id="2ae3c-142">Access data in a depth-stencil resource.</span></span>            |
| [<span data-ttu-id="2ae3c-143">**ID3DX11EffectRenderTargetViewVariable**</span><span class="sxs-lookup"><span data-stu-id="2ae3c-143">**ID3DX11EffectRenderTargetViewVariable**</span></span>](id3dx11effectrendertargetviewvariable.md)       | <span data-ttu-id="2ae3c-144">Acceder a los datos en un destino de representación.</span><span class="sxs-lookup"><span data-stu-id="2ae3c-144">Access data in a render target.</span></span>                     |
| [<span data-ttu-id="2ae3c-145">**ID3DX11EffectShaderResourceVariable**</span><span class="sxs-lookup"><span data-stu-id="2ae3c-145">**ID3DX11EffectShaderResourceVariable**</span></span>](id3dx11effectshaderresourcevariable.md)           | <span data-ttu-id="2ae3c-146">Acceder a los datos de un recurso de sombreador.</span><span class="sxs-lookup"><span data-stu-id="2ae3c-146">Access data in a shader resource.</span></span>                   |
| [<span data-ttu-id="2ae3c-147">**ID3DX11EffectUnorderedAccessViewVariable**</span><span class="sxs-lookup"><span data-stu-id="2ae3c-147">**ID3DX11EffectUnorderedAccessViewVariable**</span></span>](id3dx11effectunorderedaccessviewvariable.md) | <span data-ttu-id="2ae3c-148">Acceder a los datos en una vista de acceso desordenado.</span><span class="sxs-lookup"><span data-stu-id="2ae3c-148">Access data in an unordered access view.</span></span>            |



 

### <a name="setting-other-effect-variables"></a><span data-ttu-id="2ae3c-149">Establecer otras variables de efecto</span><span class="sxs-lookup"><span data-stu-id="2ae3c-149">Setting Other Effect Variables</span></span>

<span data-ttu-id="2ae3c-150">Use estas interfaces para obtener y establecer el estado por el tipo de variable.</span><span class="sxs-lookup"><span data-stu-id="2ae3c-150">Use these interfaces to get and set state by the variable type.</span></span>



| <span data-ttu-id="2ae3c-151">Interfaces de reflexión</span><span class="sxs-lookup"><span data-stu-id="2ae3c-151">Reflection Interfaces</span></span>                                                            | <span data-ttu-id="2ae3c-152">Descripción</span><span class="sxs-lookup"><span data-stu-id="2ae3c-152">Description</span></span>               |
|----------------------------------------------------------------------------------|---------------------------|
| [<span data-ttu-id="2ae3c-153">**ID3DX11EffectClassInstanceVariable**</span><span class="sxs-lookup"><span data-stu-id="2ae3c-153">**ID3DX11EffectClassInstanceVariable**</span></span>](id3dx11effectclassinstancevariable.md) | <span data-ttu-id="2ae3c-154">Obtiene una instancia de clase.</span><span class="sxs-lookup"><span data-stu-id="2ae3c-154">Get a class instance.</span></span>     |
| [<span data-ttu-id="2ae3c-155">**ID3DX11EffectInterfaceVariable**</span><span class="sxs-lookup"><span data-stu-id="2ae3c-155">**ID3DX11EffectInterfaceVariable**</span></span>](id3dx11effectinterfacevariable.md)         | <span data-ttu-id="2ae3c-156">Obtiene y establece una interfaz.</span><span class="sxs-lookup"><span data-stu-id="2ae3c-156">Get and set an interface.</span></span> |
| [<span data-ttu-id="2ae3c-157">**ID3DX11EffectMatrixVariable**</span><span class="sxs-lookup"><span data-stu-id="2ae3c-157">**ID3DX11EffectMatrixVariable**</span></span>](id3dx11effectmatrixvariable.md)               | <span data-ttu-id="2ae3c-158">Obtiene y establece una matriz.</span><span class="sxs-lookup"><span data-stu-id="2ae3c-158">Get and set a matrix.</span></span>     |
| [<span data-ttu-id="2ae3c-159">**ID3DX11EffectScalarVariable**</span><span class="sxs-lookup"><span data-stu-id="2ae3c-159">**ID3DX11EffectScalarVariable**</span></span>](id3dx11effectscalarvariable.md)               | <span data-ttu-id="2ae3c-160">Obtiene y establece un valor escalar.</span><span class="sxs-lookup"><span data-stu-id="2ae3c-160">Get and set a scalar.</span></span>     |
| [<span data-ttu-id="2ae3c-161">**ID3DX11EffectShaderVariable**</span><span class="sxs-lookup"><span data-stu-id="2ae3c-161">**ID3DX11EffectShaderVariable**</span></span>](id3dx11effectshadervariable.md)               | <span data-ttu-id="2ae3c-162">Obtiene una variable de sombreador.</span><span class="sxs-lookup"><span data-stu-id="2ae3c-162">Get a shader variable.</span></span>    |
| [<span data-ttu-id="2ae3c-163">**ID3DX11EffectStringVariable**</span><span class="sxs-lookup"><span data-stu-id="2ae3c-163">**ID3DX11EffectStringVariable**</span></span>](id3dx11effectstringvariable.md)               | <span data-ttu-id="2ae3c-164">Obtiene y establece una cadena.</span><span class="sxs-lookup"><span data-stu-id="2ae3c-164">Get and set a string.</span></span>     |
| [<span data-ttu-id="2ae3c-165">**ID3DX11EffectType**</span><span class="sxs-lookup"><span data-stu-id="2ae3c-165">**ID3DX11EffectType**</span></span>](id3dx11effecttype.md)                                   | <span data-ttu-id="2ae3c-166">Obtiene un tipo de variable.</span><span class="sxs-lookup"><span data-stu-id="2ae3c-166">Get a variable type.</span></span>      |
| [<span data-ttu-id="2ae3c-167">**ID3DX11EffectVectorVariable**</span><span class="sxs-lookup"><span data-stu-id="2ae3c-167">**ID3DX11EffectVectorVariable**</span></span>](id3dx11effectvectorvariable.md)               | <span data-ttu-id="2ae3c-168">Obtiene y establece un vector.</span><span class="sxs-lookup"><span data-stu-id="2ae3c-168">Get and set a vector.</span></span>     |



 

<span data-ttu-id="2ae3c-169">Todas las interfaces de reflexión derivan de [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="2ae3c-169">All reflection interfaces derive from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2ae3c-170">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2ae3c-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ae3c-171">Efectos (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="2ae3c-171">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> <dt>

[<span data-ttu-id="2ae3c-172">Programming Guide for Direct3D 11 (Guía de programación para Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="2ae3c-172">Programming Guide for Direct3D 11</span></span>](dx-graphics-overviews.md)
</dt> </dl>

 

 




