---
title: Sintaxis de la técnica de efectos (Direct3D 11)
description: Una técnica de efecto se declara con la sintaxis descrita en esta sección.
ms.assetid: 54a6ebd1-a6b4-473b-bf53-a3323445de71
keywords:
- technique11, efecto Direct3D 11
- Pass, efecto Direct3D 11
- CompileShader, efecto Direct3D 11
- SetStateGroup, efecto Direct3D 11
- SetBlendState, efecto Direct3D 11
- SetDepthStencilState, efecto Direct3D 11
- SetRasterizerState, efecto Direct3D 11
- SetVertexShader, efecto Direct3D 11
- SetGeometryShader, efecto Direct3D 11
- SetPixelShader, efecto Direct3D 11
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73fb668f308869ef9cca5cce99d522f18a287f3c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104149007"
---
# <a name="effect-technique-syntax-direct3d-11"></a><span data-ttu-id="6be50-113">Sintaxis de la técnica de efectos (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="6be50-113">Effect Technique Syntax (Direct3D 11)</span></span>

<span data-ttu-id="6be50-114">Una técnica de efecto se declara con la sintaxis descrita en esta sección.</span><span class="sxs-lookup"><span data-stu-id="6be50-114">An effect technique is declared with the syntax described in this section.</span></span>

<span data-ttu-id="6be50-115"> \[  < *Anotaciones* de TechniqueVersion TechniqueName > \]</span><span class="sxs-lookup"><span data-stu-id="6be50-115">TechniqueVersion *TechniqueName* \[ <*Annotations* > \]</span></span>

<span data-ttu-id="6be50-116">{</span><span class="sxs-lookup"><span data-stu-id="6be50-116">{</span></span>

<dl> <span data-ttu-id="6be50-117">pasar  \[  < *anotaciones* de PassName > \]</span><span class="sxs-lookup"><span data-stu-id="6be50-117">pass *PassName* \[ <*Annotations* > \]</span></span>  
<span data-ttu-id="6be50-118">{</span><span class="sxs-lookup"><span data-stu-id="6be50-118">{</span></span>
<dl> <span data-ttu-id="6be50-119">\[*SetStateGroup*; \] \[ *SetStateGroup*;\]</span><span class="sxs-lookup"><span data-stu-id="6be50-119">\[ *SetStateGroup*; \] \[ *SetStateGroup*; \]</span></span>  
<span data-ttu-id="6be50-120">...</span><span class="sxs-lookup"><span data-stu-id="6be50-120">...</span></span>  
<span data-ttu-id="6be50-121">\[*SetStateGroup*;\]</span><span class="sxs-lookup"><span data-stu-id="6be50-121">\[ *SetStateGroup*; \]</span></span>
</dl> </dd> }  
</dl>

<span data-ttu-id="6be50-122">}</span><span class="sxs-lookup"><span data-stu-id="6be50-122">}</span></span>

## <a name="parameters"></a><span data-ttu-id="6be50-123">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6be50-123">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6be50-124">Elemento</span><span class="sxs-lookup"><span data-stu-id="6be50-124">Item</span></span></th>
<th><span data-ttu-id="6be50-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="6be50-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6be50-126"><span id="TechniqueVersion"></span><span id="techniqueversion"></span><span id="TECHNIQUEVERSION"></span>TechniqueVersion</span><span class="sxs-lookup"><span data-stu-id="6be50-126"><span id="TechniqueVersion"></span><span id="techniqueversion"></span><span id="TECHNIQUEVERSION"></span>TechniqueVersion</span></span><br/></td>
<td><span data-ttu-id="6be50-127">Technique10 o technique11.</span><span class="sxs-lookup"><span data-stu-id="6be50-127">Either technique10 or technique11.</span></span> <span data-ttu-id="6be50-128">Las técnicas que usan la funcionalidad nueva en Direct3D 11 (sombreadores 5_0, BindInterfaces, etc.) deben usar technique11.</span><span class="sxs-lookup"><span data-stu-id="6be50-128">Techniques which use functionality new to Direct3D 11 (5_0 shaders, BindInterfaces, etc) must use technique11.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6be50-129"><span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span><em>TechniqueName</em></span><span class="sxs-lookup"><span data-stu-id="6be50-129"><span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span><em>TechniqueName</em></span></span><br/></td>
<td><span data-ttu-id="6be50-130">Opcional.</span><span class="sxs-lookup"><span data-stu-id="6be50-130">Optional.</span></span> <span data-ttu-id="6be50-131">Cadena ASCII que identifica de forma única el nombre de la técnica de efecto.</span><span class="sxs-lookup"><span data-stu-id="6be50-131">An ASCII string that uniquely identifies the name of the effect technique.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6be50-132"><span id="______________Annotations__"></span><span id="______________annotations__"></span><span id="______________ANNOTATIONS__"></span> <<em>Anotaciones</em> ></span><span class="sxs-lookup"><span data-stu-id="6be50-132"><span id="______________Annotations__"></span><span id="______________annotations__"></span><span id="______________ANNOTATIONS__"></span> <<em>Annotations</em> ></span></span><br/></td>
<td><span data-ttu-id="6be50-133">[in] Opcional.</span><span class="sxs-lookup"><span data-stu-id="6be50-133">[in] Optional.</span></span> <span data-ttu-id="6be50-134">Una o más partes de la información proporcionada por el usuario (metadatos) que el sistema de efectos omite.</span><span class="sxs-lookup"><span data-stu-id="6be50-134">One or more pieces of user-supplied information (metadata) that is ignored by the effect system.</span></span> <span data-ttu-id="6be50-135">Para ver la sintaxis, vea <a href="d3d11-effect-annotation-syntax.md">Sintaxis de anotación (Direct3D 11)</a>.</span><span class="sxs-lookup"><span data-stu-id="6be50-135">For syntax, see <a href="d3d11-effect-annotation-syntax.md">Annotation Syntax (Direct3D 11)</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6be50-136"><span id="pass"></span><span id="PASS"></span>pasar</span><span class="sxs-lookup"><span data-stu-id="6be50-136"><span id="pass"></span><span id="PASS"></span>pass</span></span><br/></td>
<td><span data-ttu-id="6be50-137">Palabra clave required.</span><span class="sxs-lookup"><span data-stu-id="6be50-137">Required keyword.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6be50-138"><span id="PassName"></span><span id="passname"></span><span id="PASSNAME"></span><em>PassName</em></span><span class="sxs-lookup"><span data-stu-id="6be50-138"><span id="PassName"></span><span id="passname"></span><span id="PASSNAME"></span><em>PassName</em></span></span><br/></td>
<td><span data-ttu-id="6be50-139">[in] Opcional.</span><span class="sxs-lookup"><span data-stu-id="6be50-139">[in] Optional.</span></span> <span data-ttu-id="6be50-140">Cadena ASCII que identifica de forma única el nombre del paso.</span><span class="sxs-lookup"><span data-stu-id="6be50-140">An ASCII string that uniquely identifies the name of the pass.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6be50-141"><span id="SetStateGroup"></span><span id="setstategroup"></span><span id="SETSTATEGROUP"></span><em>SetStateGroup</em></span><span class="sxs-lookup"><span data-stu-id="6be50-141"><span id="SetStateGroup"></span><span id="setstategroup"></span><span id="SETSTATEGROUP"></span><em>SetStateGroup</em></span></span><br/></td>
<td><span data-ttu-id="6be50-142">de Establezca uno o varios grupos de Estados como:</span><span class="sxs-lookup"><span data-stu-id="6be50-142">[in] Set one or more state groups such as:</span></span> <br/> 
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6be50-143">Estado</span><span class="sxs-lookup"><span data-stu-id="6be50-143">StateGroup</span></span></th>
<th><span data-ttu-id="6be50-144">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6be50-144">Syntax</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6be50-145">Estado de Blend</span><span class="sxs-lookup"><span data-stu-id="6be50-145">Blend State</span></span></td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetBlendState( arguments ); </code></pre></td>
</tr>
</tbody>
</table>

<p><span data-ttu-id="6be50-146">Vea [<strong>ID3D11DeviceContext:: OMSetBlendState</strong>] (/Windows/Desktop/API/D3D11/NF-d3d11-id3d11devicecontext-omsetblendstate) para ver la lista de argumentos.</span><span class="sxs-lookup"><span data-stu-id="6be50-146">See [<strong>ID3D11DeviceContext::OMSetBlendState</strong>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetblendstate) for the argument list.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6be50-147">Profundidad: estado de estarcido</span><span class="sxs-lookup"><span data-stu-id="6be50-147">Depth-stencil State</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetDepthStencilState( arguments ); </code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="6be50-148">Vea <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate"><strong>ID3D11DeviceContext:: OMSetDepthStencilState</strong></a> para ver la lista de argumentos.</span><span class="sxs-lookup"><span data-stu-id="6be50-148">See <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate"><strong>ID3D11DeviceContext::OMSetDepthStencilState</strong></a> for the argument list.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6be50-149">Estado del rasterizador</span><span class="sxs-lookup"><span data-stu-id="6be50-149">Rasterizer State</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetRasterizerState( arguments ); </code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="6be50-150">Vea [<strong>ID3D11DeviceContext:: RSSetState</strong>] (/Windows/Desktop/API/D3D11/NF-d3d11-id3d11devicecontext-rssetstate) para ver la lista de argumentos.</span><span class="sxs-lookup"><span data-stu-id="6be50-150">See [<strong>ID3D11DeviceContext::RSSetState</strong>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetstate) for the argument list.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6be50-151">Estado del sombreador</span><span class="sxs-lookup"><span data-stu-id="6be50-151">Shader State</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetXXXShader( Shader );</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="6be50-152">SetXXXShader es uno de SetVertexShader, SetDomainShader, SetHullShader, SetGeometryShader, SetPixelShader o SetComputeShader (que son similares a los métodos de API <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-vssetshader"><strong>ID3D11DeviceContext:: VSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader"><strong>ID3D11DeviceContext::D ssetshader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader"><strong>ID3D11DeviceContext:: HSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-gssetshader"><strong>ID3D11DeviceContext:: GSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader"><strong>ID3D11DeviceContext::P ssetshader</strong></a> y <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-cssetshader"><strong>ID3D11DeviceContext:: CSSetShader</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="6be50-152">SetXXXShader is one of SetVertexShader, SetDomainShader, SetHullShader, SetGeometryShader, SetPixelShader or SetComputeShader (which are similar to the API methods <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-vssetshader"><strong>ID3D11DeviceContext::VSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader"><strong>ID3D11DeviceContext::DSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader"><strong>ID3D11DeviceContext::HSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-gssetshader"><strong>ID3D11DeviceContext::GSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader"><strong>ID3D11DeviceContext::PSSetShader</strong></a> and <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-cssetshader"><strong>ID3D11DeviceContext::CSSetShader</strong></a>).</span></span></p>
<p><span data-ttu-id="6be50-153">Shader es una variable de sombreador, que se puede obtener de muchas maneras:</span><span class="sxs-lookup"><span data-stu-id="6be50-153">Shader is a shader variable, which can be obtained in many ways:</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetXXXShader( CompileShader( shader_profile, ShaderFunction( args ) ) );
SetXXXShader( CompileShader( NULL ) );
SetXXXShader( NULL );
SetXXXShader( myShaderVar );
SetXXXShader( myShaderArray[2] );
SetXXXShader( myShaderArray[uIndex] );
SetGeometryShader( ConstructGSWithSO( Shader, strStream0 ) );
SetGeometryShader( ConstructGSWithSO( Shader, strStream0, strStream1, strStream2, strStream3, RastStream ) );</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6be50-154">Estado de destino de representación</span><span class="sxs-lookup"><span data-stu-id="6be50-154">Render Target State</span></span></td>
<td><span data-ttu-id="6be50-155">Uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="6be50-155">One of:</span></span>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetRenderTargets( RTV0, DSV );
SetRenderTargets( RTV0, RTV1, DSV );
...
SetRenderTargets( RTV0, RTV1, RTV2, RTV3, RTV4, RTV5, RTV6, RTV7, DSV );</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="6be50-156">Similar a <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets"><strong>ID3D11DeviceContext:: OMSetRenderTargets</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="6be50-156">Similar to <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets"><strong>ID3D11DeviceContext::OMSetRenderTargets</strong></a>.</span></span></p></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="examples"></a><span data-ttu-id="6be50-157">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="6be50-157">Examples</span></span>

<span data-ttu-id="6be50-158">Este ejemplo establece el estado de fusión.</span><span class="sxs-lookup"><span data-stu-id="6be50-158">This example sets blending state.</span></span>


```
BlendState NoBlend
{ 
    BlendEnable[0] = False;
};

...

technique10
{
    pass p2 
    {
        ...
        SetBlendState( NoBlend, float4( 0.0f, 0.0f, 0.0f, 0.0f ), 0xFFFFFFFF );
    }
}
```



<span data-ttu-id="6be50-159">En este ejemplo se configura el estado de rasterizador para representar un objeto en alambre.</span><span class="sxs-lookup"><span data-stu-id="6be50-159">This example sets up the rasterizer state to render an object in wireframe.</span></span>


```
RasterizerState rsWireframe { FillMode = WireFrame; };

...

technique10
{
    pass p1 
    {
        ....
        SetRasterizerState( rsWireframe );
    }
}
```



<span data-ttu-id="6be50-160">En este ejemplo se establece el estado del sombreador.</span><span class="sxs-lookup"><span data-stu-id="6be50-160">This example sets shader state.</span></span>


```
technique10 RenderSceneWithTexture1Light
{
    pass P0
    {
        SetVertexShader( CompileShader( vs_4_0, RenderSceneVS( 1, true, true ) ) );
        SetGeometryShader( NULL );
        SetPixelShader( CompileShader( ps_4_0, RenderScenePS( true ) ) );
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="6be50-161">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6be50-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6be50-162">Formato de efecto</span><span class="sxs-lookup"><span data-stu-id="6be50-162">Effect Format</span></span>](d3d11-effect-format.md)
</dt> <dt>

[<span data-ttu-id="6be50-163">Sintaxis de grupo de efectos (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="6be50-163">Effect Group Syntax (Direct3D 11)</span></span>](d3d11-effect-group-syntax.md)
</dt> <dt>

[<span data-ttu-id="6be50-164">Grupos de Estados de efecto</span><span class="sxs-lookup"><span data-stu-id="6be50-164">Effect State Groups</span></span>](d3d11-effect-states.md)
</dt> </dl>

 

 





