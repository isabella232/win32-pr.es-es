---
title: Sintaxis de técnica de efecto (Direct3D 11)
description: Se declara una técnica de efecto con la sintaxis descrita en esta sección.
ms.assetid: 54a6ebd1-a6b4-473b-bf53-a3323445de71
keywords:
- technique11, Efecto 11 de Direct3D
- pass, Efecto 11 de Direct3D
- CompileShader, efecto 11 de Direct3D
- SetStateGroup, efecto 11 de Direct3D
- Efecto SetBlendState, Direct3D 11
- SetDepthStencilState, efecto Direct3D 11
- SetRasterizerState, efecto 11 de Direct3D
- Efecto SetVertexShader, Direct3D 11
- SetGeometryShader, efecto 11 de Direct3D
- SetPixelShader, efecto Direct3D 11
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b62876aea57864dfc495410e85ec2a9db24cbe1
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625561"
---
# <a name="effect-technique-syntax-direct3d-11"></a>Sintaxis de técnica de efecto (Direct3D 11)

Se declara una técnica de efecto con la sintaxis descrita en esta sección.

Anotaciones TechniqueVersion *TechniqueName* \[  <  > \]

{

<dl> pass *PassName* \[  < *Annotations* > \]  
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
<col  />
<col  />
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
<td>Técnica10 o técnica11. Las técnicas que usan la funcionalidad nueva de Direct3D 11 (sombreadores 5_0, BindInterfaces, etc.) deben usar technique11.<br/></td>
</tr>
<tr class="even">
<td><span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span><em>TechniqueName</em><br/></td>
<td>Opcional. Cadena ASCII que identifica de forma única el nombre de la técnica de efecto.<br/></td>
</tr>
<tr class="odd">
<td><span id="______________Annotations__"></span><span id="______________annotations__"></span><span id="______________ANNOTATIONS__"></span> <<em>Anotaciones</em> ><br/></td>
<td>[in] Opcional. Uno o varios fragmentos de información proporcionados por el usuario (metadatos) que el sistema de efectos omite. Para obtener sintaxis, vea <a href="d3d11-effect-annotation-syntax.md">Annotation Syntax (Direct3D 11) (Sintaxis de anotación [Direct3D 11]).</a><br/></td>
</tr>
<tr class="even">
<td><span id="pass"></span><span id="PASS"></span>Pasar<br/></td>
<td>Palabra clave required.<br/></td>
</tr>
<tr class="odd">
<td><span id="PassName"></span><span id="passname"></span><span id="PASSNAME"></span><em>PassName</em><br/></td>
<td>[in] Opcional. Cadena ASCII que identifica de forma única el nombre del paso.<br/></td>
</tr>
<tr class="even">
<td><span id="SetStateGroup"></span><span id="setstategroup"></span><span id="SETSTATEGROUP"></span><em>SetStateGroup</em><br/></td>
<td>[in] Establezca uno o varios grupos de estado, como: <br/> 
<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>StateGroup</th>
<th>Sintaxis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Estado de blend</td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetBlendState( arguments ); </code></pre></td>
</tr>
</tbody>
</table>

<p>Vea [<strong>ID3D11DeviceContext::OMSetBlendState</strong>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetblendstate) para obtener la lista de argumentos.</p></td>
</tr>
<tr class="even">
<td>Estado de la galería de símbolos de profundidad</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetDepthStencilState( arguments ); </code></pre></td>
</tr>
</tbody>
</table>

</div>
<p>Vea <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate"><strong>ID3D11DeviceContext::OMSetDepthStencilState</strong></a> para obtener la lista de argumentos.</p></td>
</tr>
<tr class="odd">
<td>Estado del rasterizador</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetRasterizerState( arguments ); </code></pre></td>
</tr>
</tbody>
</table>

</div>
<p>Vea [<strong>ID3D11DeviceContext::RSSetState</strong>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetstate) para obtener la lista de argumentos.</p></td>
</tr>
<tr class="even">
<td>Estado del sombreador</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetXXXShader( Shader );</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p>SetXXXShader es uno de los métodos SetVertexShader, SetDomainShader, SetHullShader, SetGeometryShader, SetPixelShader o SetComputeShader (que son similares a los métodos de API <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-vssetshader"><strong>ID3D11DeviceContext::VSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader"><strong>ID3D11DeviceContext::D SSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader"><strong>ID3D11DeviceContext::HSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-gssetshader"><strong>ID3D11DeviceContext::GSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader"><strong>ID3D11DeviceContext::P SSetShader</strong></a> e <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-cssetshader"><strong>ID3D11DeviceContext::CSSetShader</strong></a>).</p>
<p>Shader es una variable de sombreador, que se puede obtener de muchas maneras:</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
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
<td>Representar estado de destino</td>
<td>Uno de los valores siguientes:
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
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
<p>Similar a <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets"><strong>ID3D11DeviceContext::OMSetRenderTargets.</strong></a></p></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="examples"></a>Ejemplos

En este ejemplo se establece el estado de combinación.


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



En este ejemplo se configura el estado del rasterizador para representar un objeto en wireframe.


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

[Sintaxis del grupo de efectos (Direct3D 11)](d3d11-effect-group-syntax.md)
</dt> <dt>

[Grupos de estados de efecto](d3d11-effect-states.md)
</dt> </dl>

 

 





