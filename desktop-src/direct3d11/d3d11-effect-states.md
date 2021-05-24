---
title: Grupos de estados de efecto (Direct3D 11)
description: Los estados de efecto son pares de valor de nombre en forma de expresión.
ms.assetid: 87883483-4fa6-4362-807e-53b79b7d1370
keywords:
- efecto, grupos de estados (Direct3D 11)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a757926d8c4c259adc94f505a778cf73233b5a
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335345"
---
# <a name="effect-state-groups-direct3d-11"></a><span data-ttu-id="5b2d1-104">Grupos de estados de efecto (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="5b2d1-104">Effect State Groups (Direct3D 11)</span></span>

<span data-ttu-id="5b2d1-105">Los estados de efecto son pares de valor de nombre en forma de expresión.</span><span class="sxs-lookup"><span data-stu-id="5b2d1-105">Effect states are name value pairs in the form of an expression.</span></span>

-   [<span data-ttu-id="5b2d1-106">Estado de blend</span><span class="sxs-lookup"><span data-stu-id="5b2d1-106">Blend State</span></span>](#blend-state)
-   [<span data-ttu-id="5b2d1-107">Profundidad y estado de galería de símbolos</span><span class="sxs-lookup"><span data-stu-id="5b2d1-107">Depth and Stencil State</span></span>](#depth-and-stencil-state)
-   [<span data-ttu-id="5b2d1-108">Estado del rasterizador</span><span class="sxs-lookup"><span data-stu-id="5b2d1-108">Rasterizer State</span></span>](#rasterizer-state)
-   [<span data-ttu-id="5b2d1-109">Estado del muestreador</span><span class="sxs-lookup"><span data-stu-id="5b2d1-109">Sampler State</span></span>](#sampler-state)
-   [<span data-ttu-id="5b2d1-110">Estado del objeto de efecto</span><span class="sxs-lookup"><span data-stu-id="5b2d1-110">Effect Object State</span></span>](#effect-object-state)
-   [<span data-ttu-id="5b2d1-111">Definición y uso de objetos de estado</span><span class="sxs-lookup"><span data-stu-id="5b2d1-111">Defining and using state objects</span></span>](#defining-and-using-state-objects)
-   [<span data-ttu-id="5b2d1-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5b2d1-112">Related topics</span></span>](#related-topics)

## <a name="blend-state"></a><span data-ttu-id="5b2d1-113">Estado de blend</span><span class="sxs-lookup"><span data-stu-id="5b2d1-113">Blend State</span></span>



| <span data-ttu-id="5b2d1-114">Estado del efecto</span><span class="sxs-lookup"><span data-stu-id="5b2d1-114">Effect state</span></span>                                                                                                                      | <span data-ttu-id="5b2d1-115">Grupo</span><span class="sxs-lookup"><span data-stu-id="5b2d1-115">Group</span></span>                                                          |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="5b2d1-116">ALPHATOCOVERAGEENABLEBLENDENABLESRCBLENDDESTBLENDBLENDOP SRCBLEPHADESTBLEPHABLENDOPALPHARENDERTARGETWRITEMASK</span><span class="sxs-lookup"><span data-stu-id="5b2d1-116">ALPHATOCOVERAGEENABLEBLENDENABLESRCBLENDDESTBLENDBLENDOP SRCBLENDALPHADESTBLENDALPHABLENDOPALPHARENDERTARGETWRITEMASK</span></span> | <span data-ttu-id="5b2d1-117">Miembros de [ **D3D11 \_ BLEND \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)</span><span class="sxs-lookup"><span data-stu-id="5b2d1-117">Members of [**D3D11\_BLEND\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)</span></span> |



 

## <a name="depth-and-stencil-state"></a><span data-ttu-id="5b2d1-118">Profundidad y estado de galería de símbolos</span><span class="sxs-lookup"><span data-stu-id="5b2d1-118">Depth and Stencil State</span></span>



|  <span data-ttu-id="5b2d1-119">Estado del efecto</span><span class="sxs-lookup"><span data-stu-id="5b2d1-119">Effect state</span></span>                                                                                                                                                              | <span data-ttu-id="5b2d1-120">Grupo</span><span class="sxs-lookup"><span data-stu-id="5b2d1-120">Group</span></span>                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="5b2d1-121">DEPTHENABLEDEPTHWRITEMASKDEPTHFUNCSTENCILENABLESTENCILREADMASKSTENCILWRITEMASK</span><span class="sxs-lookup"><span data-stu-id="5b2d1-121">DEPTHENABLEDEPTHWRITEMASKDEPTHFUNCSTENCILENABLESTENCILREADMASKSTENCILWRITEMASK</span></span>                                                                                 | <span data-ttu-id="5b2d1-122">Miembros de [ **D3D11 \_ DEPTH \_ STENCIL \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)</span><span class="sxs-lookup"><span data-stu-id="5b2d1-122">Members of [**D3D11\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)</span></span>    |
| <span data-ttu-id="5b2d1-123">FRONTFACESTENCINCIILFRONTFACESTENCILZFAILFRONTFACESTENCILPASSFRONTFACESTENCILFUNCBACKFACESTENCINCIILBACKFACESTENCILZFAILBACKFACESTENCILPASSBACKFACESTENCILFACESTENCILFUNC</span><span class="sxs-lookup"><span data-stu-id="5b2d1-123">FRONTFACESTENCILFAILFRONTFACESTENCILZFAILFRONTFACESTENCILPASSFRONTFACESTENCILFUNCBACKFACESTENCILFAILBACKFACESTENCILZFAILBACKFACESTENCILPASSBACKFACESTENCILFUNC</span></span> | <span data-ttu-id="5b2d1-124">Miembro de [ **D3D11 \_ DEPTH \_ STENCISTONE \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencilop_desc)</span><span class="sxs-lookup"><span data-stu-id="5b2d1-124">Member of [**D3D11\_DEPTH\_STENCILOP\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencilop_desc)</span></span> |



 

## <a name="rasterizer-state"></a><span data-ttu-id="5b2d1-125">Estado del rasterizador</span><span class="sxs-lookup"><span data-stu-id="5b2d1-125">Rasterizer State</span></span>



| <span data-ttu-id="5b2d1-126">Estado del efecto</span><span class="sxs-lookup"><span data-stu-id="5b2d1-126">Effect state</span></span>                                                                                                                                | <span data-ttu-id="5b2d1-127">Grupo</span><span class="sxs-lookup"><span data-stu-id="5b2d1-127">Group</span></span>                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="5b2d1-128">FILLMODE</span><span class="sxs-lookup"><span data-stu-id="5b2d1-128">FILLMODE</span></span>                                                                                                                        | [<span data-ttu-id="5b2d1-129">**MODO DE RELLENO D3D11 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5b2d1-129">**D3D11\_FILL\_MODE**</span></span>](/windows/desktop/api/D3D11/ne-d3d11-d3d11_fill_mode)                        |
| <span data-ttu-id="5b2d1-130">CULLMODE</span><span class="sxs-lookup"><span data-stu-id="5b2d1-130">CULLMODE</span></span>                                                                                                                        | [<span data-ttu-id="5b2d1-131">**MODO CULL D3D11 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5b2d1-131">**D3D11\_CULL\_MODE**</span></span>](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cull_mode)                        |
| <span data-ttu-id="5b2d1-132">FRONTCOUNTERCLOCKWISEDEPTHBIASDEPTHBIASCLAMPSSTONEESCALEDDEPTHBIAS ZCLIPENABLESCISSORENABLEMULTISAMPLEENABLEANTIALIASEDLINEENABLE</span><span class="sxs-lookup"><span data-stu-id="5b2d1-132">FRONTCOUNTERCLOCKWISEDEPTHBIASDEPTHBIASCLAMPSLOPESCALEDDEPTHBIAS ZCLIPENABLESCISSORENABLEMULTISAMPLEENABLEANTIALIASEDLINEENABLE</span></span> | <span data-ttu-id="5b2d1-133">Miembros de [ **D3D11 \_ RASTERIZER \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)</span><span class="sxs-lookup"><span data-stu-id="5b2d1-133">Members of [**D3D11\_RASTERIZER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)</span></span> |



 

## <a name="sampler-state"></a><span data-ttu-id="5b2d1-134">Estado del muestreador</span><span class="sxs-lookup"><span data-stu-id="5b2d1-134">Sampler State</span></span>



| <span data-ttu-id="5b2d1-135">Estado del efecto</span><span class="sxs-lookup"><span data-stu-id="5b2d1-135">Effect state</span></span>                                                                                                    | <span data-ttu-id="5b2d1-136">Grupo</span><span class="sxs-lookup"><span data-stu-id="5b2d1-136">Group</span></span>                                                              |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="5b2d1-137">Filter AddressU AddressV AddressW MipLODBias MaxAnisotropy ComparisonFunc BorderColor MinLOD MaxLOD</span><span class="sxs-lookup"><span data-stu-id="5b2d1-137">Filter AddressU AddressV AddressW MipLODBias MaxAnisotropy ComparisonFunc BorderColor MinLOD MaxLOD</span></span> | <span data-ttu-id="5b2d1-138">Miembros de [ **D3D11 \_ SAMPLER \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)</span><span class="sxs-lookup"><span data-stu-id="5b2d1-138">Members of [**D3D11\_SAMPLER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)</span></span> |



 

<span data-ttu-id="5b2d1-139">Vea [Sampler Type (DirectX HLSL) (Tipo de sampler [HLSL de DirectX])](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler) para obtener ejemplos.</span><span class="sxs-lookup"><span data-stu-id="5b2d1-139">See [Sampler Type (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler) for examples.</span></span>

## <a name="effect-object-state"></a><span data-ttu-id="5b2d1-140">Estado del objeto de efecto</span><span class="sxs-lookup"><span data-stu-id="5b2d1-140">Effect Object State</span></span>



| <span data-ttu-id="5b2d1-141">Este objeto de efecto</span><span class="sxs-lookup"><span data-stu-id="5b2d1-141">This Effect Object</span></span>                          | <span data-ttu-id="5b2d1-142">Se asigna a</span><span class="sxs-lookup"><span data-stu-id="5b2d1-142">Maps to</span></span>                                                             |
|---------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="5b2d1-143">RASTERIZERSTATE</span><span class="sxs-lookup"><span data-stu-id="5b2d1-143">RASTERIZERSTATE</span></span>                             | <span data-ttu-id="5b2d1-144">Objeto [de estado de rasterizador.](#rasterizer-state)</span><span class="sxs-lookup"><span data-stu-id="5b2d1-144">A [Rasterizer State](#rasterizer-state) state object.</span></span>               |
| <span data-ttu-id="5b2d1-145">DEPTHSTENCILSTATE</span><span class="sxs-lookup"><span data-stu-id="5b2d1-145">DEPTHSTENCILSTATE</span></span>                           | <span data-ttu-id="5b2d1-146">Objeto [de estado Depth y Stencil State.](#depth-and-stencil-state)</span><span class="sxs-lookup"><span data-stu-id="5b2d1-146">A [Depth and Stencil State](#depth-and-stencil-state) state object.</span></span> |
| <span data-ttu-id="5b2d1-147">BLENDSTATE</span><span class="sxs-lookup"><span data-stu-id="5b2d1-147">BLENDSTATE</span></span>                                  | <span data-ttu-id="5b2d1-148">Objeto [de estado de blend.](#blend-state)</span><span class="sxs-lookup"><span data-stu-id="5b2d1-148">A [Blend State](#blend-state) state object.</span></span>                         |
| <span data-ttu-id="5b2d1-149">VERTEXSHADER</span><span class="sxs-lookup"><span data-stu-id="5b2d1-149">VERTEXSHADER</span></span>                                | <span data-ttu-id="5b2d1-150">Objeto de sombreador de vértices compilado.</span><span class="sxs-lookup"><span data-stu-id="5b2d1-150">A compiled vertex shader object.</span></span>                                    |
| <span data-ttu-id="5b2d1-151">PIXELSHADER</span><span class="sxs-lookup"><span data-stu-id="5b2d1-151">PIXELSHADER</span></span>                                 | <span data-ttu-id="5b2d1-152">Objeto de sombreador de píxeles compilado.</span><span class="sxs-lookup"><span data-stu-id="5b2d1-152">A compiled pixel shader object.</span></span>                                     |
| <span data-ttu-id="5b2d1-153">GEOMETRYSHADER</span><span class="sxs-lookup"><span data-stu-id="5b2d1-153">GEOMETRYSHADER</span></span>                              | <span data-ttu-id="5b2d1-154">Objeto de sombreador de geometría compilado.</span><span class="sxs-lookup"><span data-stu-id="5b2d1-154">A compiled geometry shader object.</span></span>                                  |
| <span data-ttu-id="5b2d1-155">DS \_ STENCILREFAB \_ BLENDFACTORAB \_ SAMPLEMASK</span><span class="sxs-lookup"><span data-stu-id="5b2d1-155">DS\_STENCILREFAB\_BLENDFACTORAB\_SAMPLEMASK</span></span> | <span data-ttu-id="5b2d1-156">Miembros de [**D3DX11 \_ PASS \_ DESC**](d3dx11-pass-desc.md).</span><span class="sxs-lookup"><span data-stu-id="5b2d1-156">Members of [**D3DX11\_PASS\_DESC**](d3dx11-pass-desc.md).</span></span>          |



 

## <a name="defining-and-using-state-objects"></a><span data-ttu-id="5b2d1-157">Definición y uso de objetos de estado</span><span class="sxs-lookup"><span data-stu-id="5b2d1-157">Defining and using state objects</span></span>

<span data-ttu-id="5b2d1-158">Los objetos de estado se declaran en archivos FX con el formato siguiente.</span><span class="sxs-lookup"><span data-stu-id="5b2d1-158">State objects are declared in FX files in the following format.</span></span> <span data-ttu-id="5b2d1-159">StateObjectType es uno de los estados enumerados anteriormente y MemberName es el nombre de cualquier miembro que tenga un valor no predeterminado.</span><span class="sxs-lookup"><span data-stu-id="5b2d1-159">StateObjectType is one of the states listed above and MemberName is the name of any member that will have a non-default value.</span></span>


```
StateObjectType ObjectName {
  MemberName = value;
  ...
  MemberName = value;
};
    
```



<span data-ttu-id="5b2d1-160">Por ejemplo, para configurar un objeto de estado de mezcla con AlphaToCoverageEnable y BlendEnable 0 establecido en FALSE, se usaría \[ \] el código siguiente. </span><span class="sxs-lookup"><span data-stu-id="5b2d1-160">For example, to set up a blend state object with AlphaToCoverageEnable and BlendEnable\[0\] set to **FALSE** the following code would be used.</span></span>


```
BlendState NoBlend {
  AlphaToCoverageEnable = FALSE;
  BlendEnable[0] = FALSE;
};
    
```



<span data-ttu-id="5b2d1-161">El objeto de estado se aplica a un paso de técnica mediante una de las funciones SetStateGroup descritas en Sintaxis de técnica de [efecto (Direct3D 11).](d3d11-effect-technique-syntax.md)</span><span class="sxs-lookup"><span data-stu-id="5b2d1-161">The state object is applied to a technique pass using one of the SetStateGroup functions described in [Effect Technique Syntax (Direct3D 11)](d3d11-effect-technique-syntax.md).</span></span> <span data-ttu-id="5b2d1-162">Por ejemplo, para aplicar el objeto BlendState descrito anteriormente, se usaría el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="5b2d1-162">For example, to apply the BlendState object described above the following code would be used.</span></span>


```
SetBlendState( NoBlend, float4( 0.0f, 0.0f, 0.0f, 0.0f ), 0xFFFFFFFF );
    
```



## <a name="related-topics"></a><span data-ttu-id="5b2d1-163">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5b2d1-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b2d1-164">Sintaxis de la técnica de efecto</span><span class="sxs-lookup"><span data-stu-id="5b2d1-164">Effect Technique Syntax</span></span>](d3d11-effect-technique-syntax.md)
</dt> <dt>

[<span data-ttu-id="5b2d1-165">Formato de efecto (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="5b2d1-165">Effect Format (Direct3D 11)</span></span>](d3d11-effect-format.md)
</dt> </dl>

 

 