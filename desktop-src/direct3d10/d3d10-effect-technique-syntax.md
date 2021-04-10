---
description: Una técnica de efecto se declara con la sintaxis siguiente.
ms.assetid: 84f9b74d-8397-4cd5-91a0-7f910ba7b19e
title: Sintaxis de la técnica de efectos (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f781a0e1ea247e9ffae02e6afc9de77c8e0c6b68
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153016"
---
# <a name="effect-technique-syntax-direct3d-10"></a>Sintaxis de la técnica de efectos (Direct3D 10)

Una técnica de efecto se declara con la sintaxis siguiente.

 \[  < *anotaciones* de technique10 TechniqueName > \]

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

<dl> <dt>

<span id="technique10"></span><span id="TECHNIQUE10"></span>technique10
</dt> <dd>

Palabra clave required.

</dd> <dt>

<span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span>*TechniqueName*
</dt> <dd>

Opcional. Cadena ASCII que identifica de forma única el nombre de la técnica de efecto.

</dd> <dt>

<span id="Annotations"></span><span id="annotations"></span><span id="ANNOTATIONS"></span>*Anotaciones*
</dt> <dd>

\[en \] opcional. Una o más partes de la información proporcionada por el usuario (metadatos) que el sistema de efectos omite. Para ver la sintaxis, vea [Sintaxis de anotación (Direct3D 10)](d3d10-effect-annotation-syntax.md).

</dd> <dt>

<span id="pass"></span><span id="PASS"></span>pasar
</dt> <dd>

Palabra clave required.

</dd> <dt>

<span id="PassName"></span><span id="passname"></span><span id="PASSNAME"></span>*PassName*
</dt> <dd>

\[en \] opcional. Cadena ASCII que identifica de forma única el nombre del paso.

</dd> <dt>

<span id="SetStateGroup"></span><span id="setstategroup"></span><span id="SETSTATEGROUP"></span>*SetStateGroup*
</dt> <dd>

\[en \] , establezca uno o varios grupos de Estados como:



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

<p>Vea [<strong>OMSetBlendState</strong>] (/Windows/Desktop/API/D3D10/NF-d3d10-id3d10device-omsetblendstate) para ver la lista de argumentos.</p></td>
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
<p>Consulte <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetdepthstencilstate"><strong>OMSetDepthStencilState</strong></a> para obtener la lista de argumentos.</p></td>
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
<p>Vea [<strong>RSSetState</strong>] (/Windows/Desktop/API/D3D10/NF-d3d10-id3d10device-rssetstate) para ver la lista de argumentos.</p></td>
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
<td><pre><code>SetXXXShader( CompileShader( shader_profile, ShaderFunction( args ) ) );</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p>or</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetXXXShader( CompileShader( NULL ) );</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p>or</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetXXXShader( NULL );</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p>SetXXXShader es uno de <strong>SetVertexShader</strong>, <strong>SetGeometryShader</strong>o <strong>SetPixelShader</strong> (que son similares a los métodos de API <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetshader"><strong>VSSetShader</strong></a>, <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-gssetshader"><strong>GSSetShader</strong></a>y <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-pssetshader"><strong>PSSetShader</strong></a>).</p></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

Los grupos de Estados de efecto se muestran en [Estado de efecto](d3d10-effect-states.md).

## <a name="examples"></a>Ejemplos

Este ejemplo (de [ejemplo de CubeMapGS](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)) establece el estado de fusión.


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



En este ejemplo se establece el estado del sombreador (desde el [ejemplo BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)); que usa un sombreador de vértices y píxeles.


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

[Formato de efecto](d3d10-effect-format.md)
</dt> </dl>

 

 



