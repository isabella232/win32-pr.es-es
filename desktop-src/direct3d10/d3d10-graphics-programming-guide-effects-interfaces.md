---
description: 'El sistema de efectos define varias interfaces para administrar el estado del efecto. Hay dos tipos de interfaces: las utilizadas por el motor en tiempo de ejecución para representar un efecto e interfaces de reflexión para obtener y establecer las variables de efecto.'
ms.assetid: 068d49d2-0e14-4080-9fee-20d984f22545
title: Interfaces del sistema de efectos (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b40b21d98bedaec65550343260e7c52e2df1c302
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152937"
---
# <a name="effect-system-interfaces-direct3d-10"></a><span data-ttu-id="4f9e5-104">Interfaces del sistema de efectos (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="4f9e5-104">Effect System Interfaces (Direct3D 10)</span></span>

<span data-ttu-id="4f9e5-105">El sistema de efectos define varias interfaces para administrar el estado del efecto.</span><span class="sxs-lookup"><span data-stu-id="4f9e5-105">The effect system defines several interfaces for managing effect state.</span></span> <span data-ttu-id="4f9e5-106">Hay dos tipos de interfaces: las utilizadas por el motor en tiempo de ejecución para representar un efecto e interfaces de reflexión para obtener y establecer las variables de efecto.</span><span class="sxs-lookup"><span data-stu-id="4f9e5-106">There are two types of interfaces: those used by the runtime to render an effect and reflection interfaces for getting and setting effect variables.</span></span>

-   [<span data-ttu-id="4f9e5-107">Interfaces en tiempo de ejecución de efectos</span><span class="sxs-lookup"><span data-stu-id="4f9e5-107">Effect Runtime Interfaces</span></span>](#effect-runtime-interfaces)
-   [<span data-ttu-id="4f9e5-108">Interfaces de reflexión de efectos</span><span class="sxs-lookup"><span data-stu-id="4f9e5-108">Effect Reflection Interfaces</span></span>](#effect-reflection-interfaces)

## <a name="effect-runtime-interfaces"></a><span data-ttu-id="4f9e5-109">Interfaces en tiempo de ejecución de efectos</span><span class="sxs-lookup"><span data-stu-id="4f9e5-109">Effect Runtime Interfaces</span></span>

<span data-ttu-id="4f9e5-110">Usar interfaces en tiempo de ejecución para representar un efecto.</span><span class="sxs-lookup"><span data-stu-id="4f9e5-110">Use runtime interfaces to render an effect.</span></span>



| <span data-ttu-id="4f9e5-111">Interfaces en tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="4f9e5-111">Runtime Interfaces</span></span>                                               | <span data-ttu-id="4f9e5-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="4f9e5-112">Description</span></span>                                                          |
|------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="4f9e5-113">**Interfaz ID3D10Effect**</span><span class="sxs-lookup"><span data-stu-id="4f9e5-113">**ID3D10Effect Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)                   | <span data-ttu-id="4f9e5-114">Colección de una o más técnicas para la representación.</span><span class="sxs-lookup"><span data-stu-id="4f9e5-114">Collection of one or more techniques for rendering.</span></span>                  |
| <span data-ttu-id="4f9e5-115">[**Interfaz ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4f9e5-115">[**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))</span></span>                 | <span data-ttu-id="4f9e5-116">Interfaz para agregar comportamientos personalizados al leer archivos de inclusión.</span><span class="sxs-lookup"><span data-stu-id="4f9e5-116">An interface for adding custom behaviors when reading include files.</span></span> |
| [<span data-ttu-id="4f9e5-117">**Interfaz ID3D10EffectPass**</span><span class="sxs-lookup"><span data-stu-id="4f9e5-117">**ID3D10EffectPass Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpass)           | <span data-ttu-id="4f9e5-118">Colección de asignaciones de estado.</span><span class="sxs-lookup"><span data-stu-id="4f9e5-118">A collection of state assignments.</span></span>                                   |
| [<span data-ttu-id="4f9e5-119">**Interfaz ID3D10EffectPool**</span><span class="sxs-lookup"><span data-stu-id="4f9e5-119">**ID3D10EffectPool Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)           | <span data-ttu-id="4f9e5-120">Cree una ubicación de memoria para las variables que se van a compartir entre los efectos.</span><span class="sxs-lookup"><span data-stu-id="4f9e5-120">Create a memory location for variables to be shared between effects.</span></span> |
| [<span data-ttu-id="4f9e5-121">**Interfaz ID3D10EffectTechnique**</span><span class="sxs-lookup"><span data-stu-id="4f9e5-121">**ID3D10EffectTechnique Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttechnique) | <span data-ttu-id="4f9e5-122">Colección de uno o más pasos.</span><span class="sxs-lookup"><span data-stu-id="4f9e5-122">A collection of one or more passes.</span></span>                                  |



 

## <a name="effect-reflection-interfaces"></a><span data-ttu-id="4f9e5-123">Interfaces de reflexión de efectos</span><span class="sxs-lookup"><span data-stu-id="4f9e5-123">Effect Reflection Interfaces</span></span>

<span data-ttu-id="4f9e5-124">La reflexión se implementa en el sistema de efectos para admitir el estado del efecto de lectura (y escritura).</span><span class="sxs-lookup"><span data-stu-id="4f9e5-124">Reflection is implemented in the effect system to support reading (and writing) effect state.</span></span> <span data-ttu-id="4f9e5-125">Hay varias maneras de tener acceso a las variables de efecto.</span><span class="sxs-lookup"><span data-stu-id="4f9e5-125">There are multiple ways to access effect variables.</span></span>

### <a name="setting-groups-of-effect-state"></a><span data-ttu-id="4f9e5-126">Configuración de grupos de estado de efecto</span><span class="sxs-lookup"><span data-stu-id="4f9e5-126">Setting Groups of Effect State</span></span>

<span data-ttu-id="4f9e5-127">Use estas interfaces para obtener y establecer un grupo de estado.</span><span class="sxs-lookup"><span data-stu-id="4f9e5-127">Use these interfaces to get and set a group of state.</span></span>



| <span data-ttu-id="4f9e5-128">Interfaces de reflexión</span><span class="sxs-lookup"><span data-stu-id="4f9e5-128">Reflection Interfaces</span></span>                                                                  | <span data-ttu-id="4f9e5-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="4f9e5-129">Description</span></span>                      |
|----------------------------------------------------------------------------------------|----------------------------------|
| [<span data-ttu-id="4f9e5-130">**Interfaz ID3D10EffectBlendVariable**</span><span class="sxs-lookup"><span data-stu-id="4f9e5-130">**ID3D10EffectBlendVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectblendvariable)               | <span data-ttu-id="4f9e5-131">Obtiene y establece el estado de Blend.</span><span class="sxs-lookup"><span data-stu-id="4f9e5-131">Get and set blend state.</span></span>         |
| [<span data-ttu-id="4f9e5-132">**Interfaz ID3D10EffectDepthStencilVariable**</span><span class="sxs-lookup"><span data-stu-id="4f9e5-132">**ID3D10EffectDepthStencilVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilvariable) | <span data-ttu-id="4f9e5-133">Obtiene y establece el estado de la galería de símbolos de profundidad.</span><span class="sxs-lookup"><span data-stu-id="4f9e5-133">Get and set depth-stencil state.</span></span> |
| [<span data-ttu-id="4f9e5-134">**Interfaz ID3D10EffectRasterizerVariable**</span><span class="sxs-lookup"><span data-stu-id="4f9e5-134">**ID3D10EffectRasterizerVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrasterizervariable)     | <span data-ttu-id="4f9e5-135">Obtiene y establece el estado del rasterizador.</span><span class="sxs-lookup"><span data-stu-id="4f9e5-135">Get and set rasterizer state.</span></span>    |
| [<span data-ttu-id="4f9e5-136">**Interfaz ID3D10EffectSamplerVariable**</span><span class="sxs-lookup"><span data-stu-id="4f9e5-136">**ID3D10EffectSamplerVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectsamplervariable)           | <span data-ttu-id="4f9e5-137">Obtiene y establece el estado del muestrario.</span><span class="sxs-lookup"><span data-stu-id="4f9e5-137">Get and set sampler state.</span></span>       |



 

### <a name="setting-effect-resources"></a><span data-ttu-id="4f9e5-138">Configuración de recursos de efectos</span><span class="sxs-lookup"><span data-stu-id="4f9e5-138">Setting Effect Resources</span></span>

<span data-ttu-id="4f9e5-139">Use estas interfaces para obtener y establecer recursos.</span><span class="sxs-lookup"><span data-stu-id="4f9e5-139">Use these interfaces to get and set resources.</span></span>



| <span data-ttu-id="4f9e5-140">Interfaces de reflexión</span><span class="sxs-lookup"><span data-stu-id="4f9e5-140">Reflection Interfaces</span></span>                                                                          | <span data-ttu-id="4f9e5-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="4f9e5-141">Description</span></span>                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [<span data-ttu-id="4f9e5-142">**Interfaz ID3D10EffectConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="4f9e5-142">**ID3D10EffectConstantBuffer Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectconstantbuffer)                     | <span data-ttu-id="4f9e5-143">Acceder a los datos en un búfer de textura o en un búfer de constantes.</span><span class="sxs-lookup"><span data-stu-id="4f9e5-143">Access data in a texture buffer or constant buffer.</span></span> |
| [<span data-ttu-id="4f9e5-144">**Interfaz ID3D10EffectDepthStencilViewVariable**</span><span class="sxs-lookup"><span data-stu-id="4f9e5-144">**ID3D10EffectDepthStencilViewVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilviewvariable) | <span data-ttu-id="4f9e5-145">Acceder a los datos en un recurso de estarcido de profundidad.</span><span class="sxs-lookup"><span data-stu-id="4f9e5-145">Access data in a depth-stencil resource.</span></span>            |
| [<span data-ttu-id="4f9e5-146">**Interfaz ID3D10EffectRenderTargetViewVariable**</span><span class="sxs-lookup"><span data-stu-id="4f9e5-146">**ID3D10EffectRenderTargetViewVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrendertargetviewvariable) | <span data-ttu-id="4f9e5-147">Acceder a los datos en un destino de representación.</span><span class="sxs-lookup"><span data-stu-id="4f9e5-147">Access data in a render target.</span></span>                     |
| [<span data-ttu-id="4f9e5-148">**Interfaz ID3D10EffectShaderResourceVariable**</span><span class="sxs-lookup"><span data-stu-id="4f9e5-148">**ID3D10EffectShaderResourceVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshaderresourcevariable)     | <span data-ttu-id="4f9e5-149">Acceder a los datos de un recurso de sombreador.</span><span class="sxs-lookup"><span data-stu-id="4f9e5-149">Access data in a shader resource.</span></span>                   |



 

### <a name="setting-other-effect-variables"></a><span data-ttu-id="4f9e5-150">Establecer otras variables de efecto</span><span class="sxs-lookup"><span data-stu-id="4f9e5-150">Setting Other Effect Variables</span></span>

<span data-ttu-id="4f9e5-151">Use estas interfaces para obtener y establecer el estado por el tipo de variable.</span><span class="sxs-lookup"><span data-stu-id="4f9e5-151">Use these interfaces to get and set state by the variable type.</span></span>



| <span data-ttu-id="4f9e5-152">Interfaces de reflexión</span><span class="sxs-lookup"><span data-stu-id="4f9e5-152">Reflection Interfaces</span></span>                                                      | <span data-ttu-id="4f9e5-153">Descripción</span><span class="sxs-lookup"><span data-stu-id="4f9e5-153">Description</span></span>                    |
|----------------------------------------------------------------------------|--------------------------------|
| [<span data-ttu-id="4f9e5-154">**Interfaz ID3D10EffectMatrixVariable**</span><span class="sxs-lookup"><span data-stu-id="4f9e5-154">**ID3D10EffectMatrixVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectmatrixvariable) | <span data-ttu-id="4f9e5-155">Obtiene y establece una matriz.</span><span class="sxs-lookup"><span data-stu-id="4f9e5-155">Get and set a matrix.</span></span>          |
| [<span data-ttu-id="4f9e5-156">**Interfaz ID3D10EffectScalarVariable**</span><span class="sxs-lookup"><span data-stu-id="4f9e5-156">**ID3D10EffectScalarVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectscalarvariable) | <span data-ttu-id="4f9e5-157">Obtiene y establece un valor escalar.</span><span class="sxs-lookup"><span data-stu-id="4f9e5-157">Get and set a scalar.</span></span>          |
| [<span data-ttu-id="4f9e5-158">**Interfaz ID3D10EffectShaderVariable**</span><span class="sxs-lookup"><span data-stu-id="4f9e5-158">**ID3D10EffectShaderVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshadervariable) | <span data-ttu-id="4f9e5-159">Obtiene y establece una variable de sombreador.</span><span class="sxs-lookup"><span data-stu-id="4f9e5-159">Get and set a shader variable.</span></span> |
| [<span data-ttu-id="4f9e5-160">**Interfaz ID3D10EffectStringVariable**</span><span class="sxs-lookup"><span data-stu-id="4f9e5-160">**ID3D10EffectStringVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectstringvariable) | <span data-ttu-id="4f9e5-161">Obtiene y establece una cadena.</span><span class="sxs-lookup"><span data-stu-id="4f9e5-161">Get and set a string.</span></span>          |
| [<span data-ttu-id="4f9e5-162">**Interfaz ID3D10EffectType**</span><span class="sxs-lookup"><span data-stu-id="4f9e5-162">**ID3D10EffectType Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttype)                     | <span data-ttu-id="4f9e5-163">Obtiene un tipo de variable.</span><span class="sxs-lookup"><span data-stu-id="4f9e5-163">Get a variable type.</span></span>           |
| [<span data-ttu-id="4f9e5-164">**Interfaz ID3D10EffectVectorVariable**</span><span class="sxs-lookup"><span data-stu-id="4f9e5-164">**ID3D10EffectVectorVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvectorvariable) | <span data-ttu-id="4f9e5-165">Obtiene y establece un vector.</span><span class="sxs-lookup"><span data-stu-id="4f9e5-165">Get and set a vector.</span></span>          |



 

<span data-ttu-id="4f9e5-166">Todas las interfaces de reflexión derivan de la [**interfaz ID3D10EffectVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable).</span><span class="sxs-lookup"><span data-stu-id="4f9e5-166">All reflection interfaces derive from [**ID3D10EffectVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4f9e5-167">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4f9e5-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f9e5-168">Efectos</span><span class="sxs-lookup"><span data-stu-id="4f9e5-168">Effects</span></span>](d3d10-graphics-programming-guide-effects.md)
</dt> <dt>

[<span data-ttu-id="4f9e5-169">Guía de programación para Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="4f9e5-169">Programming Guide for Direct3D 10</span></span>](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
