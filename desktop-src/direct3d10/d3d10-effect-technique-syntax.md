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
# <a name="effect-technique-syntax-direct3d-10"></a><span data-ttu-id="ffb11-103">Sintaxis de la técnica de efectos (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="ffb11-103">Effect Technique Syntax (Direct3D 10)</span></span>

<span data-ttu-id="ffb11-104">Una técnica de efecto se declara con la sintaxis siguiente.</span><span class="sxs-lookup"><span data-stu-id="ffb11-104">An effect technique is declared with the following syntax.</span></span>

<span data-ttu-id="ffb11-105"> \[  < *anotaciones* de technique10 TechniqueName > \]</span><span class="sxs-lookup"><span data-stu-id="ffb11-105">technique10 *TechniqueName* \[ <*Annotations* > \]</span></span>

<span data-ttu-id="ffb11-106">{</span><span class="sxs-lookup"><span data-stu-id="ffb11-106">{</span></span>

<dl> <span data-ttu-id="ffb11-107">pasar  \[  < *anotaciones* de PassName > \]</span><span class="sxs-lookup"><span data-stu-id="ffb11-107">pass *PassName* \[ <*Annotations* > \]</span></span>  
<span data-ttu-id="ffb11-108">{</span><span class="sxs-lookup"><span data-stu-id="ffb11-108">{</span></span>
<dl> <span data-ttu-id="ffb11-109">\[*SetStateGroup*; \] \[ *SetStateGroup*;\]</span><span class="sxs-lookup"><span data-stu-id="ffb11-109">\[ *SetStateGroup*; \] \[ *SetStateGroup*; \]</span></span>  
<span data-ttu-id="ffb11-110">...</span><span class="sxs-lookup"><span data-stu-id="ffb11-110">...</span></span>  
<span data-ttu-id="ffb11-111">\[*SetStateGroup*;\]</span><span class="sxs-lookup"><span data-stu-id="ffb11-111">\[ *SetStateGroup*; \]</span></span>
</dl> </dd> }  
</dl>

<span data-ttu-id="ffb11-112">}</span><span class="sxs-lookup"><span data-stu-id="ffb11-112">}</span></span>

## <a name="parameters"></a><span data-ttu-id="ffb11-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ffb11-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffb11-114"><span id="technique10"></span><span id="TECHNIQUE10"></span>technique10</span><span class="sxs-lookup"><span data-stu-id="ffb11-114"><span id="technique10"></span><span id="TECHNIQUE10"></span>technique10</span></span>
</dt> <dd>

<span data-ttu-id="ffb11-115">Palabra clave required.</span><span class="sxs-lookup"><span data-stu-id="ffb11-115">Required keyword.</span></span>

</dd> <dt>

<span data-ttu-id="ffb11-116"><span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span>*TechniqueName*</span><span class="sxs-lookup"><span data-stu-id="ffb11-116"><span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span>*TechniqueName*</span></span>
</dt> <dd>

<span data-ttu-id="ffb11-117">Opcional.</span><span class="sxs-lookup"><span data-stu-id="ffb11-117">Optional.</span></span> <span data-ttu-id="ffb11-118">Cadena ASCII que identifica de forma única el nombre de la técnica de efecto.</span><span class="sxs-lookup"><span data-stu-id="ffb11-118">An ASCII string that uniquely identifies the name of the effect technique.</span></span>

</dd> <dt>

<span data-ttu-id="ffb11-119"><span id="Annotations"></span><span id="annotations"></span><span id="ANNOTATIONS"></span>*Anotaciones*</span><span class="sxs-lookup"><span data-stu-id="ffb11-119"><span id="Annotations"></span><span id="annotations"></span><span id="ANNOTATIONS"></span>*Annotations*</span></span>
</dt> <dd>

<span data-ttu-id="ffb11-120">\[en \] opcional.</span><span class="sxs-lookup"><span data-stu-id="ffb11-120">\[in\] Optional.</span></span> <span data-ttu-id="ffb11-121">Una o más partes de la información proporcionada por el usuario (metadatos) que el sistema de efectos omite.</span><span class="sxs-lookup"><span data-stu-id="ffb11-121">One or more pieces of user-supplied information (metadata) that is ignored by the effect system.</span></span> <span data-ttu-id="ffb11-122">Para ver la sintaxis, vea [Sintaxis de anotación (Direct3D 10)](d3d10-effect-annotation-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="ffb11-122">For syntax, see [Annotation Syntax (Direct3D 10)](d3d10-effect-annotation-syntax.md).</span></span>

</dd> <dt>

<span data-ttu-id="ffb11-123"><span id="pass"></span><span id="PASS"></span>pasar</span><span class="sxs-lookup"><span data-stu-id="ffb11-123"><span id="pass"></span><span id="PASS"></span>pass</span></span>
</dt> <dd>

<span data-ttu-id="ffb11-124">Palabra clave required.</span><span class="sxs-lookup"><span data-stu-id="ffb11-124">Required keyword.</span></span>

</dd> <dt>

<span data-ttu-id="ffb11-125"><span id="PassName"></span><span id="passname"></span><span id="PASSNAME"></span>*PassName*</span><span class="sxs-lookup"><span data-stu-id="ffb11-125"><span id="PassName"></span><span id="passname"></span><span id="PASSNAME"></span>*PassName*</span></span>
</dt> <dd>

<span data-ttu-id="ffb11-126">\[en \] opcional.</span><span class="sxs-lookup"><span data-stu-id="ffb11-126">\[in\] Optional.</span></span> <span data-ttu-id="ffb11-127">Cadena ASCII que identifica de forma única el nombre del paso.</span><span class="sxs-lookup"><span data-stu-id="ffb11-127">An ASCII string that uniquely identifies the name of the pass.</span></span>

</dd> <dt>

<span data-ttu-id="ffb11-128"><span id="SetStateGroup"></span><span id="setstategroup"></span><span id="SETSTATEGROUP"></span>*SetStateGroup*</span><span class="sxs-lookup"><span data-stu-id="ffb11-128"><span id="SetStateGroup"></span><span id="setstategroup"></span><span id="SETSTATEGROUP"></span>*SetStateGroup*</span></span>
</dt> <dd>

<span data-ttu-id="ffb11-129">\[en \] , establezca uno o varios grupos de Estados como:</span><span class="sxs-lookup"><span data-stu-id="ffb11-129">\[in\] Set one or more state groups such as:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ffb11-130">Estado</span><span class="sxs-lookup"><span data-stu-id="ffb11-130">StateGroup</span></span></th>
<th><span data-ttu-id="ffb11-131">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ffb11-131">Syntax</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ffb11-132">Estado de Blend</span><span class="sxs-lookup"><span data-stu-id="ffb11-132">Blend State</span></span></td>
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

<p><span data-ttu-id="ffb11-133">Vea [<strong>OMSetBlendState</strong>] (/Windows/Desktop/API/D3D10/NF-d3d10-id3d10device-omsetblendstate) para ver la lista de argumentos.</span><span class="sxs-lookup"><span data-stu-id="ffb11-133">See [<strong>OMSetBlendState</strong>](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetblendstate) for the argument list.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ffb11-134">Profundidad: estado de estarcido</span><span class="sxs-lookup"><span data-stu-id="ffb11-134">Depth-stencil State</span></span></td>
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
<p><span data-ttu-id="ffb11-135">Consulte <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetdepthstencilstate"><strong>OMSetDepthStencilState</strong></a> para obtener la lista de argumentos.</span><span class="sxs-lookup"><span data-stu-id="ffb11-135">See <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetdepthstencilstate"><strong>OMSetDepthStencilState</strong></a> for the argument list.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ffb11-136">Estado del rasterizador</span><span class="sxs-lookup"><span data-stu-id="ffb11-136">Rasterizer State</span></span></td>
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
<p><span data-ttu-id="ffb11-137">Vea [<strong>RSSetState</strong>] (/Windows/Desktop/API/D3D10/NF-d3d10-id3d10device-rssetstate) para ver la lista de argumentos.</span><span class="sxs-lookup"><span data-stu-id="ffb11-137">See [<strong>RSSetState</strong>](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-rssetstate) for the argument list.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ffb11-138">Estado del sombreador</span><span class="sxs-lookup"><span data-stu-id="ffb11-138">Shader State</span></span></td>
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
<p><span data-ttu-id="ffb11-139">or</span><span class="sxs-lookup"><span data-stu-id="ffb11-139">or</span></span></p>
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
<p><span data-ttu-id="ffb11-140">or</span><span class="sxs-lookup"><span data-stu-id="ffb11-140">or</span></span></p>
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
<p><span data-ttu-id="ffb11-141">SetXXXShader es uno de <strong>SetVertexShader</strong>, <strong>SetGeometryShader</strong>o <strong>SetPixelShader</strong> (que son similares a los métodos de API <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetshader"><strong>VSSetShader</strong></a>, <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-gssetshader"><strong>GSSetShader</strong></a>y <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-pssetshader"><strong>PSSetShader</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="ffb11-141">SetXXXShader is one of <strong>SetVertexShader</strong>, <strong>SetGeometryShader</strong>, or <strong>SetPixelShader</strong> (which are similar to the API methods <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetshader"><strong>VSSetShader</strong></a>, <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-gssetshader"><strong>GSSetShader</strong></a>, and <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-pssetshader"><strong>PSSetShader</strong></a>).</span></span></p></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

<span data-ttu-id="ffb11-142">Los grupos de Estados de efecto se muestran en [Estado de efecto](d3d10-effect-states.md).</span><span class="sxs-lookup"><span data-stu-id="ffb11-142">Effect state groups are listed in [effect state](d3d10-effect-states.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ffb11-143">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ffb11-143">Examples</span></span>

<span data-ttu-id="ffb11-144">Este ejemplo (de [ejemplo de CubeMapGS](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)) establece el estado de fusión.</span><span class="sxs-lookup"><span data-stu-id="ffb11-144">This example (from [CubeMapGS sample](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)) sets blending state.</span></span>


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



<span data-ttu-id="ffb11-145">En este ejemplo se configura el estado de rasterizador para representar un objeto en alambre.</span><span class="sxs-lookup"><span data-stu-id="ffb11-145">This example sets up the rasterizer state to render an object in wireframe.</span></span>


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



<span data-ttu-id="ffb11-146">En este ejemplo se establece el estado del sombreador (desde el [ejemplo BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)); que usa un sombreador de vértices y píxeles.</span><span class="sxs-lookup"><span data-stu-id="ffb11-146">This example sets shader state (from [BasicHLSL10 sample](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)); which uses a vertex and pixel shader.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="ffb11-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ffb11-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ffb11-148">Formato de efecto</span><span class="sxs-lookup"><span data-stu-id="ffb11-148">Effect Format</span></span>](d3d10-effect-format.md)
</dt> </dl>

 

 



