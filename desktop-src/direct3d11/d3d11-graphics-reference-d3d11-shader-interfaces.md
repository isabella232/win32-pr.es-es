---
title: 'Interfaces de sombreador (gráficos de Direct3D 11) '
description: Esta sección contiene información sobre las interfaces del sombreador.
ms.assetid: 1791d2c9-3791-47fe-b887-a8117ecc798b
keywords:
- interfaces, sombreador de Direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d55e591d56442b641482a76a4ec93c0055029fc0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104421808"
---
# <a name="shader-interfaces-direct3d-11-graphics"></a>Interfaces de sombreador (gráficos de Direct3D 11) 

Esta sección contiene información sobre las interfaces del sombreador.

Cada una de estas interfaces de sombreador administra un sombreador compilado. La interfaz se crea cuando se compila un sombreador y, a continuación, se pasa a varias API que necesitan acceso a un sombreador compilado; por ejemplo, al enlazar un sombreador a una fase de canalización u obtener una firma de sombreador.


## <a name="in-this-section"></a>En esta sección



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tema</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance"><strong>ID3D11ClassInstance</strong></a><br/></td>
<td>Esta interfaz encapsula una clase HLSL.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage"><strong>ID3D11ClassLinkage</strong></a><br/></td>
<td>Esta interfaz encapsula una vinculación dinámica de HLSL.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11computeshader"><strong>ID3D11ComputeShader</strong></a><br/></td>
<td>Una interfaz de sombreador de cálculo administra un programa ejecutable (un sombreador de cálculo) que controla la fase del sombreador de cálculo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11domainshader"><strong>ID3D11DomainShader</strong></a><br/></td>
<td>Una interfaz de sombreador de dominio administra un programa ejecutable (un sombreador de dominio) que controla la fase del sombreador del dominio.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionlinkinggraph"><strong>ID3D11FunctionLinkingGraph</strong></a><br/></td>
<td>Una interfaz function-linking-Graph se usa para construir sombreadores que constan de una secuencia de llamadas a funciones precompiladas que pasan valores entre sí. <br/>
<blockquote>
[!Note]<br />
Esta interfaz forma parte de la tecnología de vinculación del sombreador de HLSL que puede usar en todas las plataformas de Direct3D 11 para crear funciones HLSL precompiladas, empaquetarlas en bibliotecas y vincularlas a los sombreadores completos en tiempo de ejecución.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionreflection"><strong>ID3D11FunctionReflection</strong></a><br/></td>
<td>Una interfaz de reflexión de funciones obtiene acceso a la información de la función. <br/>
<blockquote>
[!Note]<br />
Esta interfaz forma parte de la tecnología de vinculación del sombreador de HLSL que puede usar en todas las plataformas de Direct3D 11 para crear funciones HLSL precompiladas, empaquetarlas en bibliotecas y vincularlas a los sombreadores completos en tiempo de ejecución.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionparameterreflection"><strong>ID3D11FunctionParameterReflection</strong></a><br/></td>
<td>Una interfaz de función-parámetro-reflexión obtiene acceso a la información de parámetros de función. <br/>
<blockquote>
[!Note]<br />
Esta interfaz forma parte de la tecnología de vinculación del sombreador de HLSL que puede usar en todas las plataformas de Direct3D 11 para crear funciones HLSL precompiladas, empaquetarlas en bibliotecas y vincularlas a los sombreadores completos en tiempo de ejecución.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11geometryshader"><strong>ID3D11GeometryShader</strong></a><br/></td>
<td>Una interfaz de sombreador de geometría administra un programa ejecutable (un sombreador de geometría) que controla la fase del sombreador de geometría.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11hullshader"><strong>ID3D11HullShader</strong></a><br/></td>
<td>Una interfaz de sombreador de casco administra un programa ejecutable (un sombreador de casco) que controla la fase del sombreador de casco.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11libraryreflection"><strong>ID3D11LibraryReflection</strong></a><br/></td>
<td>Una interfaz de reflexión de biblioteca obtiene acceso a la información de la biblioteca. <br/>
<blockquote>
[!Note]<br />
Esta interfaz forma parte de la tecnología de vinculación del sombreador de HLSL que puede usar en todas las plataformas de Direct3D 11 para crear funciones HLSL precompiladas, empaquetarlas en bibliotecas y vincularlas a los sombreadores completos en tiempo de ejecución.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linker"><strong>ID3D11Linker</strong></a><br/></td>
<td>Una interfaz del enlazador se usa para vincular un módulo de sombreador. <br/>
<blockquote>
[!Note]<br />
Esta interfaz forma parte de la tecnología de vinculación del sombreador de HLSL que puede usar en todas las plataformas de Direct3D 11 para crear funciones HLSL precompiladas, empaquetarlas en bibliotecas y vincularlas a los sombreadores completos en tiempo de ejecución.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linkingnode"><strong>ID3D11LinkingNode</strong></a><br/></td>
<td>Una interfaz de nodo de vinculación se usa para la vinculación del sombreador. <br/>
<blockquote>
[!Note]<br />
Esta interfaz forma parte de la tecnología de vinculación del sombreador de HLSL que puede usar en todas las plataformas de Direct3D 11 para crear funciones HLSL precompiladas, empaquetarlas en bibliotecas y vincularlas a los sombreadores completos en tiempo de ejecución.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11module"><strong>ID3D11Module</strong></a><br/></td>
<td>Una interfaz de módulo crea una instancia de un módulo que se usa para el reenlace de recursos. <br/>
<blockquote>
[!Note]<br />
Esta interfaz forma parte de la tecnología de vinculación del sombreador de HLSL que puede usar en todas las plataformas de Direct3D 11 para crear funciones HLSL precompiladas, empaquetarlas en bibliotecas y vincularlas a los sombreadores completos en tiempo de ejecución.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11moduleinstance"><strong>ID3D11ModuleInstance</strong></a><br/></td>
<td>Una interfaz de instancia de módulo se usa para volver a enlazar recursos. <br/>
<blockquote>
[!Note]<br />
Esta interfaz forma parte de la tecnología de vinculación del sombreador de HLSL que puede usar en todas las plataformas de Direct3D 11 para crear funciones HLSL precompiladas, empaquetarlas en bibliotecas y vincularlas a los sombreadores completos en tiempo de ejecución.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11pixelshader"><strong>ID3D11PixelShader</strong></a><br/></td>
<td>Una interfaz de sombreador de píxeles administra un programa ejecutable (un sombreador de píxeles) que controla la fase del sombreador de píxeles.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflection"><strong>ID3D11ShaderReflection</strong></a><br/></td>
<td>Una interfaz de reflexión del sombreador obtiene acceso a la información del sombreador.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectionconstantbuffer"><strong>ID3D11ShaderReflectionConstantBuffer</strong></a><br/></td>
<td>Esta interfaz de reflexión del sombreador proporciona acceso a un búfer de constantes.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectiontype"><strong>ID3D11ShaderReflectionType</strong></a><br/></td>
<td>Esta interfaz de reflexión del sombreador proporciona acceso al tipo de variable.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectionvariable"><strong>ID3D11ShaderReflectionVariable</strong></a><br/></td>
<td>Esta interfaz de reflexión del sombreador proporciona acceso a una variable.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertrace"><strong>ID3D11ShaderTrace</strong></a><br/></td>
<td>Una interfaz <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertrace"><strong>ID3D11ShaderTrace</strong></a> implementa métodos para obtener los seguimientos de las ejecuciones del sombreador.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertracefactory"><strong>ID3D11ShaderTraceFactory</strong></a><br/></td>
<td>Una interfaz <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertracefactory"><strong>ID3D11ShaderTraceFactory</strong></a> implementa un método para generar objetos de información de seguimiento de sombreador.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11vertexshader"><strong>ID3D11VertexShader</strong></a><br/></td>
<td>Una interfaz de sombreador de vértices administra un programa ejecutable (un sombreador de vértices) que controla la fase del sombreador de vértices.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de los sombreadores](d3d11-graphics-reference-d3d11-shader.md)
</dt> </dl>

 

