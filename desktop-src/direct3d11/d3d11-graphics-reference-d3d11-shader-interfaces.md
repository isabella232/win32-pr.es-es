---
title: 'Interfaces de sombreador (gráficos de Direct3D 11) '
description: Esta sección contiene información sobre las interfaces del sombreador.
ms.assetid: 1791d2c9-3791-47fe-b887-a8117ecc798b
keywords:
- interfaces, sombreador de Direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41fcecdff6f35b634ecbbeca0b85bc5ba42fd1e5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479461"
---
# <a name="shader-interfaces-direct3d-11-graphics"></a>Interfaces de sombreador (gráficos de Direct3D 11) 

Esta sección contiene información sobre las interfaces del sombreador.

Cada una de estas interfaces de sombreador administra un sombreador compilado. La interfaz se crea cuando se compila un sombreador y, a continuación, se pasa a varias API que necesitan acceso a un sombreador compilado. por ejemplo, al enlazar un sombreador a una fase de canalización u obtener una firma de sombreador.


## <a name="in-this-section"></a>En esta sección




| Tema | Descripción | 
|-------|-------------|
| <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance"><strong>ID3D11ClassInstance</strong></a><br /> | Esta interfaz encapsula una clase HLSL.<br /> | 
| <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage"><strong>ID3D11ClassLinkage</strong></a><br /> | Esta interfaz encapsula una vinculación dinámica HLSL.<br /> | 
| <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11computeshader"><strong>ID3D11ComputeShader</strong></a><br /> | Una interfaz de sombreador de proceso administra un programa ejecutable (un sombreador de proceso) que controla la fase del sombreador de proceso.<br /> | 
| <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11domainshader"><strong>ID3D11DomainShader</strong></a><br /> | Una interfaz de sombreador de dominio administra un programa ejecutable (un sombreador de dominio) que controla la fase del sombreador de dominio.<br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionlinkinggraph"><strong>ID3D11FunctionLinkingGraph</strong></a><br /> | Se usa una interfaz function-linking-graph para construir sombreadores que constan de una secuencia de llamadas de función precompiladas que pasan valores entre sí. <br /><blockquote>[!Note]<br />Esta interfaz forma parte de la tecnología de vinculación de sombreador HLSL que puede usar en todas las plataformas de Direct3D 11 para crear funciones HLSL precompiladas, empaquetarlas en bibliotecas y vincularlas a sombreadores completos en tiempo de ejecución.</blockquote><br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionreflection"><strong>ID3D11FunctionReflection</strong></a><br /> | Una interfaz de reflexión de función tiene acceso a la información de la función. <br /><blockquote>[!Note]<br />Esta interfaz forma parte de la tecnología de vinculación de sombreador HLSL que puede usar en todas las plataformas de Direct3D 11 para crear funciones HLSL precompiladas, empaquetarlas en bibliotecas y vincularlas a sombreadores completos en tiempo de ejecución.</blockquote><br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionparameterreflection"><strong>ID3D11FunctionParameterReflection</strong></a><br /> | Una interfaz function-parameter-reflection tiene acceso a la información de parámetro de función. <br /><blockquote>[!Note]<br />Esta interfaz forma parte de la tecnología de vinculación de sombreador HLSL que puede usar en todas las plataformas de Direct3D 11 para crear funciones HLSL precompiladas, empaquetarlas en bibliotecas y vincularlas a sombreadores completos en tiempo de ejecución.</blockquote><br /> | 
| <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11geometryshader"><strong>ID3D11GeometryShader</strong></a><br /> | Una interfaz de sombreador de geometría administra un programa ejecutable (un sombreador de geometría) que controla la fase del sombreador de geometría.<br /> | 
| <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11hullshader"><strong>ID3D11HullShader</strong></a><br /> | Una interfaz de sombreador de casco administra un programa ejecutable (un sombreador de casco) que controla la fase del sombreador de casco.<br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11libraryreflection"><strong>ID3D11LibraryReflection</strong></a><br /> | Una interfaz de reflexión de biblioteca accede a la información de la biblioteca. <br /><blockquote>[!Note]<br />Esta interfaz forma parte de la tecnología de vinculación de sombreador HLSL que puede usar en todas las plataformas de Direct3D 11 para crear funciones HLSL precompiladas, empaquetarlas en bibliotecas y vincularlas a sombreadores completos en tiempo de ejecución.</blockquote><br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linker"><strong>ID3D11Linker</strong></a><br /> | Se usa una interfaz del vinculador para vincular un módulo de sombreador. <br /><blockquote>[!Note]<br />Esta interfaz forma parte de la tecnología de vinculación de sombreador HLSL que puede usar en todas las plataformas de Direct3D 11 para crear funciones HLSL precompiladas, empaquetarlas en bibliotecas y vincularlas a sombreadores completos en tiempo de ejecución.</blockquote><br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linkingnode"><strong>ID3D11LinkingNode</strong></a><br /> | Se usa una interfaz de nodo de vinculación para la vinculación del sombreador. <br /><blockquote>[!Note]<br />Esta interfaz forma parte de la tecnología de vinculación de sombreador HLSL que puede usar en todas las plataformas de Direct3D 11 para crear funciones HLSL precompiladas, empaquetarlas en bibliotecas y vincularlas a sombreadores completos en tiempo de ejecución.</blockquote><br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11module"><strong>ID3D11Module</strong></a><br /> | Una interfaz de módulo crea una instancia de un módulo que se usa para volver a enlace de recursos. <br /><blockquote>[!Note]<br />Esta interfaz forma parte de la tecnología de vinculación de sombreador HLSL que puede usar en todas las plataformas de Direct3D 11 para crear funciones HLSL precompiladas, empaquetarlas en bibliotecas y vincularlas a sombreadores completos en tiempo de ejecución.</blockquote><br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11moduleinstance"><strong>ID3D11ModuleInstance</strong></a><br /> | Se usa una interfaz de instancia de módulo para volver a enlace de recursos. <br /><blockquote>[!Note]<br />Esta interfaz forma parte de la tecnología de vinculación de sombreador HLSL que puede usar en todas las plataformas de Direct3D 11 para crear funciones HLSL precompiladas, empaquetarlas en bibliotecas y vincularlas a sombreadores completos en tiempo de ejecución.</blockquote><br /> | 
| <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11pixelshader"><strong>ID3D11PixelShader</strong></a><br /> | Una interfaz de sombreador de píxeles administra un programa ejecutable (un sombreador de píxeles) que controla la fase del sombreador de píxeles.<br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflection"><strong>ID3D11ShaderReflection</strong></a><br /> | Una interfaz de reflexión de sombreador tiene acceso a la información del sombreador.<br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectionconstantbuffer"><strong>ID3D11ShaderReflectionConstantBuffer</strong></a><br /> | Esta interfaz de reflexión de sombreador proporciona acceso a un búfer constante.<br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectiontype"><strong>ID3D11ShaderReflectionType</strong></a><br /> | Esta interfaz de reflexión de sombreador proporciona acceso al tipo de variable.<br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectionvariable"><strong>ID3D11ShaderReflectionVariable</strong></a><br /> | Esta interfaz de reflexión de sombreador proporciona acceso a una variable.<br /> | 
| <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertrace"><strong>ID3D11ShaderTrace</strong></a><br /> | Una <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertrace"><strong>interfaz ID3D11ShaderTrace</strong></a> implementa métodos para obtener seguimientos de ejecuciones de sombreador.<br /> | 
| <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertracefactory"><strong>ID3D11ShaderTraceFactory</strong></a><br /> | Una <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertracefactory"><strong>interfaz ID3D11ShaderTraceFactory</strong></a> implementa un método para generar objetos de información de seguimiento de sombreador.<br /> | 
| <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11vertexshader"><strong>ID3D11VertexShader</strong></a><br /> | Una interfaz de sombreador de vértices administra un programa ejecutable (un sombreador de vértices) que controla la fase del sombreador de vértices.<br /> | 




 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de los sombreadores](d3d11-graphics-reference-d3d11-shader.md)
</dt> </dl>

 

