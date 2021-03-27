---
title: Grupos de Estados de efectos (Direct3D 11)
description: Los Estados de efecto son pares de nombre y valor en forma de expresión.
ms.assetid: 87883483-4fa6-4362-807e-53b79b7d1370
keywords:
- efecto, grupos de Estados (Direct3D 11)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58def71b6362706eb831129b1d222ef3d1cc9341
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995282"
---
# <a name="effect-state-groups-direct3d-11"></a><span data-ttu-id="fc9dc-104">Grupos de Estados de efectos (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="fc9dc-104">Effect State Groups (Direct3D 11)</span></span>

<span data-ttu-id="fc9dc-105">Los Estados de efecto son pares de nombre y valor en forma de expresión.</span><span class="sxs-lookup"><span data-stu-id="fc9dc-105">Effect states are name value pairs in the form of an expression.</span></span>

-   [<span data-ttu-id="fc9dc-106">Estado de Blend</span><span class="sxs-lookup"><span data-stu-id="fc9dc-106">Blend State</span></span>](#blend-state)
-   [<span data-ttu-id="fc9dc-107">Profundidad y estado de estarcido</span><span class="sxs-lookup"><span data-stu-id="fc9dc-107">Depth and Stencil State</span></span>](#depth-and-stencil-state)
-   [<span data-ttu-id="fc9dc-108">Estado del rasterizador</span><span class="sxs-lookup"><span data-stu-id="fc9dc-108">Rasterizer State</span></span>](#rasterizer-state)
-   [<span data-ttu-id="fc9dc-109">Estado de muestra</span><span class="sxs-lookup"><span data-stu-id="fc9dc-109">Sampler State</span></span>](#sampler-state)
-   [<span data-ttu-id="fc9dc-110">Estado del objeto de efecto</span><span class="sxs-lookup"><span data-stu-id="fc9dc-110">Effect Object State</span></span>](#effect-object-state)
-   [<span data-ttu-id="fc9dc-111">Definir y usar objetos de estado</span><span class="sxs-lookup"><span data-stu-id="fc9dc-111">Defining and using state objects</span></span>](#defining-and-using-state-objects)
-   [<span data-ttu-id="fc9dc-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fc9dc-112">Related topics</span></span>](#related-topics)

## <a name="blend-state"></a><span data-ttu-id="fc9dc-113">Estado de Blend</span><span class="sxs-lookup"><span data-stu-id="fc9dc-113">Blend State</span></span>



|                                                                                                                       |                                                           |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="fc9dc-114">ALPHATOCOVERAGEENABLEBLENDENABLESRCBLENDDESTBLENDBLENDOP SRCBLENDALPHADESTBLENDALPHABLENDOPALPHARENDERTARGETWRITEMASK</span><span class="sxs-lookup"><span data-stu-id="fc9dc-114">ALPHATOCOVERAGEENABLEBLENDENABLESRCBLENDDESTBLENDBLENDOP SRCBLENDALPHADESTBLENDALPHABLENDOPALPHARENDERTARGETWRITEMASK</span></span> | <span data-ttu-id="fc9dc-115">Miembros de [ **D3D11 \_ Blend \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)</span><span class="sxs-lookup"><span data-stu-id="fc9dc-115">Members of [**D3D11\_BLEND\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)</span></span> |



 

## <a name="depth-and-stencil-state"></a><span data-ttu-id="fc9dc-116">Profundidad y estado de estarcido</span><span class="sxs-lookup"><span data-stu-id="fc9dc-116">Depth and Stencil State</span></span>



|                                                                                                                                                                |                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="fc9dc-117">DEPTHENABLEDEPTHWRITEMASKDEPTHFUNCSTENCILENABLESTENCILREADMASKSTENCILWRITEMASK</span><span class="sxs-lookup"><span data-stu-id="fc9dc-117">DEPTHENABLEDEPTHWRITEMASKDEPTHFUNCSTENCILENABLESTENCILREADMASKSTENCILWRITEMASK</span></span>                                                                                 | <span data-ttu-id="fc9dc-118">Miembros de la [ **Galería de símbolos de \_ profundidad D3D11 \_ \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)</span><span class="sxs-lookup"><span data-stu-id="fc9dc-118">Members of [**D3D11\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)</span></span>    |
| <span data-ttu-id="fc9dc-119">FRONTFACESTENCILFAILFRONTFACESTENCILZFAILFRONTFACESTENCILPASSFRONTFACESTENCILFUNCBACKFACESTENCILFAILBACKFACESTENCILZFAILBACKFACESTENCILPASSBACKFACESTENCILFUNC</span><span class="sxs-lookup"><span data-stu-id="fc9dc-119">FRONTFACESTENCILFAILFRONTFACESTENCILZFAILFRONTFACESTENCILPASSFRONTFACESTENCILFUNCBACKFACESTENCILFAILBACKFACESTENCILZFAILBACKFACESTENCILPASSBACKFACESTENCILFUNC</span></span> | <span data-ttu-id="fc9dc-120">Miembro de [ **D3D11 \_ Depth \_ STENCILOP \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencilop_desc)</span><span class="sxs-lookup"><span data-stu-id="fc9dc-120">Member of [**D3D11\_DEPTH\_STENCILOP\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencilop_desc)</span></span> |



 

## <a name="rasterizer-state"></a><span data-ttu-id="fc9dc-121">Estado del rasterizador</span><span class="sxs-lookup"><span data-stu-id="fc9dc-121">Rasterizer State</span></span>



|                                                                                                                                 |                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="fc9dc-122">FILLMODE</span><span class="sxs-lookup"><span data-stu-id="fc9dc-122">FILLMODE</span></span>                                                                                                                        | [<span data-ttu-id="fc9dc-123">**\_Modo de relleno de D3D11 \_**</span><span class="sxs-lookup"><span data-stu-id="fc9dc-123">**D3D11\_FILL\_MODE**</span></span>](/windows/desktop/api/D3D11/ne-d3d11-d3d11_fill_mode)                        |
| <span data-ttu-id="fc9dc-124">CULLMODE</span><span class="sxs-lookup"><span data-stu-id="fc9dc-124">CULLMODE</span></span>                                                                                                                        | [<span data-ttu-id="fc9dc-125">**\_Modo de selección de D3D11 \_**</span><span class="sxs-lookup"><span data-stu-id="fc9dc-125">**D3D11\_CULL\_MODE**</span></span>](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cull_mode)                        |
| <span data-ttu-id="fc9dc-126">FRONTCOUNTERCLOCKWISEDEPTHBIASDEPTHBIASCLAMPSLOPESCALEDDEPTHBIAS ZCLIPENABLESCISSORENABLEMULTISAMPLEENABLEANTIALIASEDLINEENABLE</span><span class="sxs-lookup"><span data-stu-id="fc9dc-126">FRONTCOUNTERCLOCKWISEDEPTHBIASDEPTHBIASCLAMPSLOPESCALEDDEPTHBIAS ZCLIPENABLESCISSORENABLEMULTISAMPLEENABLEANTIALIASEDLINEENABLE</span></span> | <span data-ttu-id="fc9dc-127">Miembros de [ **D3D11 \_ rasterizador \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)</span><span class="sxs-lookup"><span data-stu-id="fc9dc-127">Members of [**D3D11\_RASTERIZER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)</span></span> |



 

## <a name="sampler-state"></a><span data-ttu-id="fc9dc-128">Estado de muestra</span><span class="sxs-lookup"><span data-stu-id="fc9dc-128">Sampler State</span></span>



|                                                                                                     |                                                               |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="fc9dc-129">Filter AddressU AddressV AddressW MipLODBias MaxAnisotropy ComparisonFunc BorderColor MinLOD MaxLOD</span><span class="sxs-lookup"><span data-stu-id="fc9dc-129">Filter AddressU AddressV AddressW MipLODBias MaxAnisotropy ComparisonFunc BorderColor MinLOD MaxLOD</span></span> | <span data-ttu-id="fc9dc-130">Miembros de la [ **\_ muestra D3D11 \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)</span><span class="sxs-lookup"><span data-stu-id="fc9dc-130">Members of [**D3D11\_SAMPLER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)</span></span> |



 

<span data-ttu-id="fc9dc-131">Consulte [tipo de muestra (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler) para obtener ejemplos.</span><span class="sxs-lookup"><span data-stu-id="fc9dc-131">See [Sampler Type (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler) for examples.</span></span>

## <a name="effect-object-state"></a><span data-ttu-id="fc9dc-132">Estado del objeto de efecto</span><span class="sxs-lookup"><span data-stu-id="fc9dc-132">Effect Object State</span></span>



| <span data-ttu-id="fc9dc-133">Este objeto de efecto</span><span class="sxs-lookup"><span data-stu-id="fc9dc-133">This Effect Object</span></span>                          | <span data-ttu-id="fc9dc-134">Se asigna a</span><span class="sxs-lookup"><span data-stu-id="fc9dc-134">Maps to</span></span>                                                             |
|---------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="fc9dc-135">RASTERIZERSTATE</span><span class="sxs-lookup"><span data-stu-id="fc9dc-135">RASTERIZERSTATE</span></span>                             | <span data-ttu-id="fc9dc-136">Objeto de estado de [Estado de rasterizador](#rasterizer-state) .</span><span class="sxs-lookup"><span data-stu-id="fc9dc-136">A [Rasterizer State](#rasterizer-state) state object.</span></span>               |
| <span data-ttu-id="fc9dc-137">DEPTHSTENCILSTATE</span><span class="sxs-lookup"><span data-stu-id="fc9dc-137">DEPTHSTENCILSTATE</span></span>                           | <span data-ttu-id="fc9dc-138">Objeto de estado de [Estado de estarcido y de profundidad](#depth-and-stencil-state) .</span><span class="sxs-lookup"><span data-stu-id="fc9dc-138">A [Depth and Stencil State](#depth-and-stencil-state) state object.</span></span> |
| <span data-ttu-id="fc9dc-139">BLENDSTATE</span><span class="sxs-lookup"><span data-stu-id="fc9dc-139">BLENDSTATE</span></span>                                  | <span data-ttu-id="fc9dc-140">Objeto de estado de [Estado de Blend](#blend-state) .</span><span class="sxs-lookup"><span data-stu-id="fc9dc-140">A [Blend State](#blend-state) state object.</span></span>                         |
| <span data-ttu-id="fc9dc-141">VERTEXSHADER</span><span class="sxs-lookup"><span data-stu-id="fc9dc-141">VERTEXSHADER</span></span>                                | <span data-ttu-id="fc9dc-142">Objeto de sombreador de vértices compilado.</span><span class="sxs-lookup"><span data-stu-id="fc9dc-142">A compiled vertex shader object.</span></span>                                    |
| <span data-ttu-id="fc9dc-143">U</span><span class="sxs-lookup"><span data-stu-id="fc9dc-143">PIXELSHADER</span></span>                                 | <span data-ttu-id="fc9dc-144">Objeto de sombreador de píxeles compilado.</span><span class="sxs-lookup"><span data-stu-id="fc9dc-144">A compiled pixel shader object.</span></span>                                     |
| <span data-ttu-id="fc9dc-145">GEOMETRYSHADER</span><span class="sxs-lookup"><span data-stu-id="fc9dc-145">GEOMETRYSHADER</span></span>                              | <span data-ttu-id="fc9dc-146">Objeto de sombreador de geometría compilado.</span><span class="sxs-lookup"><span data-stu-id="fc9dc-146">A compiled geometry shader object.</span></span>                                  |
| <span data-ttu-id="fc9dc-147">\_STENCILREFAB DS \_ BLENDFACTORAB \_ SAMPLEMASK</span><span class="sxs-lookup"><span data-stu-id="fc9dc-147">DS\_STENCILREFAB\_BLENDFACTORAB\_SAMPLEMASK</span></span> | <span data-ttu-id="fc9dc-148">Miembros de [**D3DX11 \_ Pass \_ DESC**](d3dx11-pass-desc.md).</span><span class="sxs-lookup"><span data-stu-id="fc9dc-148">Members of [**D3DX11\_PASS\_DESC**](d3dx11-pass-desc.md).</span></span>          |



 

## <a name="defining-and-using-state-objects"></a><span data-ttu-id="fc9dc-149">Definir y usar objetos de estado</span><span class="sxs-lookup"><span data-stu-id="fc9dc-149">Defining and using state objects</span></span>

<span data-ttu-id="fc9dc-150">Los objetos de estado se declaran en archivos FX con el siguiente formato.</span><span class="sxs-lookup"><span data-stu-id="fc9dc-150">State objects are declared in FX files in the following format.</span></span> <span data-ttu-id="fc9dc-151">StateObjectType es uno de los Estados enumerados anteriormente y MemberName es el nombre de cualquier miembro que tenga un valor no predeterminado.</span><span class="sxs-lookup"><span data-stu-id="fc9dc-151">StateObjectType is one of the states listed above and MemberName is the name of any member that will have a non-default value.</span></span>


```
StateObjectType ObjectName {
  MemberName = value;
  ...
  MemberName = value;
};
    
```



<span data-ttu-id="fc9dc-152">Por ejemplo, para configurar un objeto de estado de Blend con AlphaToCoverageEnable y BlendEnable \[ 0 \] establecido en **false** , se utilizaría el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="fc9dc-152">For example, to set up a blend state object with AlphaToCoverageEnable and BlendEnable\[0\] set to **FALSE** the following code would be used.</span></span>


```
BlendState NoBlend {
  AlphaToCoverageEnable = FALSE;
  BlendEnable[0] = FALSE;
};
    
```



<span data-ttu-id="fc9dc-153">El objeto de estado se aplica a un paso de técnica mediante una de las funciones de SetStateGroup descritas en sintaxis de la [técnica de efectos (Direct3D 11)](d3d11-effect-technique-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="fc9dc-153">The state object is applied to a technique pass using one of the SetStateGroup functions described in [Effect Technique Syntax (Direct3D 11)](d3d11-effect-technique-syntax.md).</span></span> <span data-ttu-id="fc9dc-154">Por ejemplo, para aplicar el objeto BlendState descrito anteriormente, se utilizaría el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="fc9dc-154">For example, to apply the BlendState object described above the following code would be used.</span></span>


```
SetBlendState( NoBlend, float4( 0.0f, 0.0f, 0.0f, 0.0f ), 0xFFFFFFFF );
    
```



## <a name="related-topics"></a><span data-ttu-id="fc9dc-155">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fc9dc-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc9dc-156">Sintaxis de la técnica de efectos</span><span class="sxs-lookup"><span data-stu-id="fc9dc-156">Effect Technique Syntax</span></span>](d3d11-effect-technique-syntax.md)
</dt> <dt>

[<span data-ttu-id="fc9dc-157">Formato de efecto (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="fc9dc-157">Effect Format (Direct3D 11)</span></span>](d3d11-effect-format.md)
</dt> </dl>

 

 