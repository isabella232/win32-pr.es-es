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
# <a name="effect-technique-syntax-direct3d-11"></a>Sintaxis de la técnica de efectos (Direct3D 11)

Una técnica de efecto se declara con la sintaxis descrita en esta sección.

 \[  < *Anotaciones* de TechniqueVersion TechniqueName > \]

{

<dl> pasar  \[  < *anotaciones* de PassName > \]  
{
<dl> \[*SetStateGroup*; \] \[ *SetStateGroup*;\]  
...  
\[*SetStateGroup*;\]
</dl> </dd> }  
</dl>

}

## <a name="parameters"></a>Parámetros



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Elemento</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="TechniqueVersion"></span><span id="techniqueversion"></span><span id="TECHNIQUEVERSION"></span>TechniqueVersion<br/></td>
<td>Technique10 o technique11. Las técnicas que usan la funcionalidad nueva en Direct3D 11 (sombreadores 5_0, BindInterfaces, etc.) deben usar technique11.<br/></td>
</tr>
<tr class="even">
<td><span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span><em>TechniqueName</em><br/></td>
<td>Opcional. Cadena ASCII que identifica de forma única el nombre de la técnica de efecto.<br/></td>
</tr>
<tr class="odd">
<td><span id="______________Annotations__"></span><span id="______________annotations__"></span><span id="______________ANNOTATIONS__"></span> <<em>Anotaciones</em> ><br/></td>
<td>[in] Opcional. Una o más partes de la información proporcionada por el usuario (metadatos) que el sistema de efectos omite. Para ver la sintaxis, vea <a href="d3d11-effect-annotation-syntax.md">Sintaxis de anotación (Direct3D 11)</a>.<br/></td>
</tr>
<tr class="even">
<td><span id="pass"></span><span id="PASS"></span>pasar<br/></td>
<td>Palabra clave required.<br/></td>
</tr>
<tr class="odd">
<td><span id="PassName"></span><span id="passname"></span><span id="PASSNAME"></span><em>PassName</em><br/></td>
<td>[in] Opcional. Cadena ASCII que identifica de forma única el nombre del paso.<br/></td>
</tr>
<tr class="even">
<td><span id="SetStateGroup"></span><span id="setstategroup"></span><span id="SETSTATEGROUP"></span><em>SetStateGroup</em><br/></td>
<td>de Establezca uno o varios grupos de Estados como: <br/> 
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Estado</th>
<th>Sintaxis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Estado de Blend</td>
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

<p>Vea [<strong>ID3D11DeviceContext:: OMSetBlendState</strong>] (/Windows/Desktop/API/D3D11/NF-d3d11-id3d11devicecontext-omsetblendstate) para ver la lista de argumentos.</p></td>
</tr>
<tr class="even">
<td>Profundidad: estado de estarcido</td>
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
<p>Vea <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate"><strong>ID3D11DeviceContext:: OMSetDepthStencilState</strong></a> para ver la lista de argumentos.</p></td>
</tr>
<tr class="odd">
<td>Estado del rasterizador</td>
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
<p>Vea [<strong>ID3D11DeviceContext:: RSSetState</strong>] (/Windows/Desktop/API/D3D11/NF-d3d11-id3d11devicecontext-rssetstate) para ver la lista de argumentos.</p></td>
</tr>
<tr class="even">
<td>Estado del sombreador</td>
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
<p>SetXXXShader es uno de SetVertexShader, SetDomainShader, SetHullShader, SetGeometryShader, SetPixelShader o SetComputeShader (que son similares a los métodos de API <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-vssetshader"><strong>ID3D11DeviceContext:: VSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader"><strong>ID3D11DeviceContext::D ssetshader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader"><strong>ID3D11DeviceContext:: HSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-gssetshader"><strong>ID3D11DeviceContext:: GSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader"><strong>ID3D11DeviceContext::P ssetshader</strong></a> y <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-cssetshader"><strong>ID3D11DeviceContext:: CSSetShader</strong></a>).</p>
<p>Shader es una variable de sombreador, que se puede obtener de muchas maneras:</p>
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
<td>Estado de destino de representación</td>
<td>Uno de los valores siguientes:
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
<p>Similar a <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets"><strong>ID3D11DeviceContext:: OMSetRenderTargets</strong></a>.</p></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="examples"></a>Ejemplos

Este ejemplo establece el estado de fusión.


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



En este ejemplo se configura el estado de rasterizador para representar un objeto en alambre.


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



En este ejemplo se establece el estado del sombreador.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Formato de efecto](d3d11-effect-format.md)
</dt> <dt>

[Sintaxis de grupo de efectos (Direct3D 11)](d3d11-effect-group-syntax.md)
</dt> <dt>

[Grupos de Estados de efecto](d3d11-effect-states.md)
</dt> </dl>

 

 





