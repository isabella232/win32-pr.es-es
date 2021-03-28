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
# <a name="shader-interfaces-direct3d-11-graphics"></a><span data-ttu-id="95f4b-104">Interfaces de sombreador (gráficos de Direct3D 11) </span><span class="sxs-lookup"><span data-stu-id="95f4b-104">Shader Interfaces (Direct3D 11 Graphics)</span></span>

<span data-ttu-id="95f4b-105">Esta sección contiene información sobre las interfaces del sombreador.</span><span class="sxs-lookup"><span data-stu-id="95f4b-105">This section contains information about the shader interfaces.</span></span>

<span data-ttu-id="95f4b-106">Cada una de estas interfaces de sombreador administra un sombreador compilado.</span><span class="sxs-lookup"><span data-stu-id="95f4b-106">Each of these shader interfaces manages a compiled shader.</span></span> <span data-ttu-id="95f4b-107">La interfaz se crea cuando se compila un sombreador y, a continuación, se pasa a varias API que necesitan acceso a un sombreador compilado; por ejemplo, al enlazar un sombreador a una fase de canalización u obtener una firma de sombreador.</span><span class="sxs-lookup"><span data-stu-id="95f4b-107">The interface is created when a shader is compiled, and is then passed to various APIs that need access to a compiled shader; such as when binding a shader to a pipeline stage or getting a shader signature.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="95f4b-108">En esta sección</span><span class="sxs-lookup"><span data-stu-id="95f4b-108">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="95f4b-109">Tema</span><span class="sxs-lookup"><span data-stu-id="95f4b-109">Topic</span></span></th>
<th><span data-ttu-id="95f4b-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="95f4b-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="95f4b-111"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance"><strong>ID3D11ClassInstance</strong></a></span><span class="sxs-lookup"><span data-stu-id="95f4b-111"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance"><strong>ID3D11ClassInstance</strong></a></span></span><br/></td>
<td><span data-ttu-id="95f4b-112">Esta interfaz encapsula una clase HLSL.</span><span class="sxs-lookup"><span data-stu-id="95f4b-112">This interface encapsulates an HLSL class.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95f4b-113"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage"><strong>ID3D11ClassLinkage</strong></a></span><span class="sxs-lookup"><span data-stu-id="95f4b-113"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage"><strong>ID3D11ClassLinkage</strong></a></span></span><br/></td>
<td><span data-ttu-id="95f4b-114">Esta interfaz encapsula una vinculación dinámica de HLSL.</span><span class="sxs-lookup"><span data-stu-id="95f4b-114">This interface encapsulates an HLSL dynamic linkage.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95f4b-115"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11computeshader"><strong>ID3D11ComputeShader</strong></a></span><span class="sxs-lookup"><span data-stu-id="95f4b-115"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11computeshader"><strong>ID3D11ComputeShader</strong></a></span></span><br/></td>
<td><span data-ttu-id="95f4b-116">Una interfaz de sombreador de cálculo administra un programa ejecutable (un sombreador de cálculo) que controla la fase del sombreador de cálculo.</span><span class="sxs-lookup"><span data-stu-id="95f4b-116">A compute-shader interface manages an executable program (a compute shader) that controls the compute-shader stage.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95f4b-117"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11domainshader"><strong>ID3D11DomainShader</strong></a></span><span class="sxs-lookup"><span data-stu-id="95f4b-117"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11domainshader"><strong>ID3D11DomainShader</strong></a></span></span><br/></td>
<td><span data-ttu-id="95f4b-118">Una interfaz de sombreador de dominio administra un programa ejecutable (un sombreador de dominio) que controla la fase del sombreador del dominio.</span><span class="sxs-lookup"><span data-stu-id="95f4b-118">A domain-shader interface manages an executable program (a domain shader) that controls the domain-shader stage.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95f4b-119"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionlinkinggraph"><strong>ID3D11FunctionLinkingGraph</strong></a></span><span class="sxs-lookup"><span data-stu-id="95f4b-119"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionlinkinggraph"><strong>ID3D11FunctionLinkingGraph</strong></a></span></span><br/></td>
<td><span data-ttu-id="95f4b-120">Una interfaz function-linking-Graph se usa para construir sombreadores que constan de una secuencia de llamadas a funciones precompiladas que pasan valores entre sí.</span><span class="sxs-lookup"><span data-stu-id="95f4b-120">A function-linking-graph interface is used for constructing shaders that consist of a sequence of precompiled function calls that pass values to each other.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="95f4b-121">Esta interfaz forma parte de la tecnología de vinculación del sombreador de HLSL que puede usar en todas las plataformas de Direct3D 11 para crear funciones HLSL precompiladas, empaquetarlas en bibliotecas y vincularlas a los sombreadores completos en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="95f4b-121">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95f4b-122"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionreflection"><strong>ID3D11FunctionReflection</strong></a></span><span class="sxs-lookup"><span data-stu-id="95f4b-122"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionreflection"><strong>ID3D11FunctionReflection</strong></a></span></span><br/></td>
<td><span data-ttu-id="95f4b-123">Una interfaz de reflexión de funciones obtiene acceso a la información de la función.</span><span class="sxs-lookup"><span data-stu-id="95f4b-123">A function-reflection interface accesses function info.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="95f4b-124">Esta interfaz forma parte de la tecnología de vinculación del sombreador de HLSL que puede usar en todas las plataformas de Direct3D 11 para crear funciones HLSL precompiladas, empaquetarlas en bibliotecas y vincularlas a los sombreadores completos en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="95f4b-124">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95f4b-125"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionparameterreflection"><strong>ID3D11FunctionParameterReflection</strong></a></span><span class="sxs-lookup"><span data-stu-id="95f4b-125"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionparameterreflection"><strong>ID3D11FunctionParameterReflection</strong></a></span></span><br/></td>
<td><span data-ttu-id="95f4b-126">Una interfaz de función-parámetro-reflexión obtiene acceso a la información de parámetros de función.</span><span class="sxs-lookup"><span data-stu-id="95f4b-126">A function-parameter-reflection interface accesses function-parameter info.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="95f4b-127">Esta interfaz forma parte de la tecnología de vinculación del sombreador de HLSL que puede usar en todas las plataformas de Direct3D 11 para crear funciones HLSL precompiladas, empaquetarlas en bibliotecas y vincularlas a los sombreadores completos en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="95f4b-127">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95f4b-128"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11geometryshader"><strong>ID3D11GeometryShader</strong></a></span><span class="sxs-lookup"><span data-stu-id="95f4b-128"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11geometryshader"><strong>ID3D11GeometryShader</strong></a></span></span><br/></td>
<td><span data-ttu-id="95f4b-129">Una interfaz de sombreador de geometría administra un programa ejecutable (un sombreador de geometría) que controla la fase del sombreador de geometría.</span><span class="sxs-lookup"><span data-stu-id="95f4b-129">A geometry-shader interface manages an executable program (a geometry shader) that controls the geometry-shader stage.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95f4b-130"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11hullshader"><strong>ID3D11HullShader</strong></a></span><span class="sxs-lookup"><span data-stu-id="95f4b-130"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11hullshader"><strong>ID3D11HullShader</strong></a></span></span><br/></td>
<td><span data-ttu-id="95f4b-131">Una interfaz de sombreador de casco administra un programa ejecutable (un sombreador de casco) que controla la fase del sombreador de casco.</span><span class="sxs-lookup"><span data-stu-id="95f4b-131">A hull-shader interface manages an executable program (a hull shader) that controls the hull-shader stage.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95f4b-132"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11libraryreflection"><strong>ID3D11LibraryReflection</strong></a></span><span class="sxs-lookup"><span data-stu-id="95f4b-132"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11libraryreflection"><strong>ID3D11LibraryReflection</strong></a></span></span><br/></td>
<td><span data-ttu-id="95f4b-133">Una interfaz de reflexión de biblioteca obtiene acceso a la información de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="95f4b-133">A library-reflection interface accesses library info.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="95f4b-134">Esta interfaz forma parte de la tecnología de vinculación del sombreador de HLSL que puede usar en todas las plataformas de Direct3D 11 para crear funciones HLSL precompiladas, empaquetarlas en bibliotecas y vincularlas a los sombreadores completos en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="95f4b-134">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95f4b-135"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linker"><strong>ID3D11Linker</strong></a></span><span class="sxs-lookup"><span data-stu-id="95f4b-135"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linker"><strong>ID3D11Linker</strong></a></span></span><br/></td>
<td><span data-ttu-id="95f4b-136">Una interfaz del enlazador se usa para vincular un módulo de sombreador.</span><span class="sxs-lookup"><span data-stu-id="95f4b-136">A linker interface is used to link a shader module.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="95f4b-137">Esta interfaz forma parte de la tecnología de vinculación del sombreador de HLSL que puede usar en todas las plataformas de Direct3D 11 para crear funciones HLSL precompiladas, empaquetarlas en bibliotecas y vincularlas a los sombreadores completos en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="95f4b-137">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95f4b-138"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linkingnode"><strong>ID3D11LinkingNode</strong></a></span><span class="sxs-lookup"><span data-stu-id="95f4b-138"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linkingnode"><strong>ID3D11LinkingNode</strong></a></span></span><br/></td>
<td><span data-ttu-id="95f4b-139">Una interfaz de nodo de vinculación se usa para la vinculación del sombreador.</span><span class="sxs-lookup"><span data-stu-id="95f4b-139">A linking-node interface is used for shader linking.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="95f4b-140">Esta interfaz forma parte de la tecnología de vinculación del sombreador de HLSL que puede usar en todas las plataformas de Direct3D 11 para crear funciones HLSL precompiladas, empaquetarlas en bibliotecas y vincularlas a los sombreadores completos en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="95f4b-140">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95f4b-141"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11module"><strong>ID3D11Module</strong></a></span><span class="sxs-lookup"><span data-stu-id="95f4b-141"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11module"><strong>ID3D11Module</strong></a></span></span><br/></td>
<td><span data-ttu-id="95f4b-142">Una interfaz de módulo crea una instancia de un módulo que se usa para el reenlace de recursos.</span><span class="sxs-lookup"><span data-stu-id="95f4b-142">A module interface creates an instance of a module that is used for resource rebinding.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="95f4b-143">Esta interfaz forma parte de la tecnología de vinculación del sombreador de HLSL que puede usar en todas las plataformas de Direct3D 11 para crear funciones HLSL precompiladas, empaquetarlas en bibliotecas y vincularlas a los sombreadores completos en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="95f4b-143">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95f4b-144"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11moduleinstance"><strong>ID3D11ModuleInstance</strong></a></span><span class="sxs-lookup"><span data-stu-id="95f4b-144"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11moduleinstance"><strong>ID3D11ModuleInstance</strong></a></span></span><br/></td>
<td><span data-ttu-id="95f4b-145">Una interfaz de instancia de módulo se usa para volver a enlazar recursos.</span><span class="sxs-lookup"><span data-stu-id="95f4b-145">A module-instance interface is used for resource rebinding.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="95f4b-146">Esta interfaz forma parte de la tecnología de vinculación del sombreador de HLSL que puede usar en todas las plataformas de Direct3D 11 para crear funciones HLSL precompiladas, empaquetarlas en bibliotecas y vincularlas a los sombreadores completos en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="95f4b-146">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95f4b-147"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11pixelshader"><strong>ID3D11PixelShader</strong></a></span><span class="sxs-lookup"><span data-stu-id="95f4b-147"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11pixelshader"><strong>ID3D11PixelShader</strong></a></span></span><br/></td>
<td><span data-ttu-id="95f4b-148">Una interfaz de sombreador de píxeles administra un programa ejecutable (un sombreador de píxeles) que controla la fase del sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="95f4b-148">A pixel-shader interface manages an executable program (a pixel shader) that controls the pixel-shader stage.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95f4b-149"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflection"><strong>ID3D11ShaderReflection</strong></a></span><span class="sxs-lookup"><span data-stu-id="95f4b-149"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflection"><strong>ID3D11ShaderReflection</strong></a></span></span><br/></td>
<td><span data-ttu-id="95f4b-150">Una interfaz de reflexión del sombreador obtiene acceso a la información del sombreador.</span><span class="sxs-lookup"><span data-stu-id="95f4b-150">A shader-reflection interface accesses shader information.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95f4b-151"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectionconstantbuffer"><strong>ID3D11ShaderReflectionConstantBuffer</strong></a></span><span class="sxs-lookup"><span data-stu-id="95f4b-151"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectionconstantbuffer"><strong>ID3D11ShaderReflectionConstantBuffer</strong></a></span></span><br/></td>
<td><span data-ttu-id="95f4b-152">Esta interfaz de reflexión del sombreador proporciona acceso a un búfer de constantes.</span><span class="sxs-lookup"><span data-stu-id="95f4b-152">This shader-reflection interface provides access to a constant buffer.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95f4b-153"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectiontype"><strong>ID3D11ShaderReflectionType</strong></a></span><span class="sxs-lookup"><span data-stu-id="95f4b-153"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectiontype"><strong>ID3D11ShaderReflectionType</strong></a></span></span><br/></td>
<td><span data-ttu-id="95f4b-154">Esta interfaz de reflexión del sombreador proporciona acceso al tipo de variable.</span><span class="sxs-lookup"><span data-stu-id="95f4b-154">This shader-reflection interface provides access to variable type.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95f4b-155"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectionvariable"><strong>ID3D11ShaderReflectionVariable</strong></a></span><span class="sxs-lookup"><span data-stu-id="95f4b-155"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectionvariable"><strong>ID3D11ShaderReflectionVariable</strong></a></span></span><br/></td>
<td><span data-ttu-id="95f4b-156">Esta interfaz de reflexión del sombreador proporciona acceso a una variable.</span><span class="sxs-lookup"><span data-stu-id="95f4b-156">This shader-reflection interface provides access to a variable.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95f4b-157"><a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertrace"><strong>ID3D11ShaderTrace</strong></a></span><span class="sxs-lookup"><span data-stu-id="95f4b-157"><a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertrace"><strong>ID3D11ShaderTrace</strong></a></span></span><br/></td>
<td><span data-ttu-id="95f4b-158">Una interfaz <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertrace"><strong>ID3D11ShaderTrace</strong></a> implementa métodos para obtener los seguimientos de las ejecuciones del sombreador.</span><span class="sxs-lookup"><span data-stu-id="95f4b-158">An <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertrace"><strong>ID3D11ShaderTrace</strong></a> interface implements methods for obtaining traces of shader executions.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95f4b-159"><a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertracefactory"><strong>ID3D11ShaderTraceFactory</strong></a></span><span class="sxs-lookup"><span data-stu-id="95f4b-159"><a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertracefactory"><strong>ID3D11ShaderTraceFactory</strong></a></span></span><br/></td>
<td><span data-ttu-id="95f4b-160">Una interfaz <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertracefactory"><strong>ID3D11ShaderTraceFactory</strong></a> implementa un método para generar objetos de información de seguimiento de sombreador.</span><span class="sxs-lookup"><span data-stu-id="95f4b-160">An <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertracefactory"><strong>ID3D11ShaderTraceFactory</strong></a> interface implements a method for generating shader trace information objects.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95f4b-161"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11vertexshader"><strong>ID3D11VertexShader</strong></a></span><span class="sxs-lookup"><span data-stu-id="95f4b-161"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11vertexshader"><strong>ID3D11VertexShader</strong></a></span></span><br/></td>
<td><span data-ttu-id="95f4b-162">Una interfaz de sombreador de vértices administra un programa ejecutable (un sombreador de vértices) que controla la fase del sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="95f4b-162">A vertex-shader interface manages an executable program (a vertex shader) that controls the vertex-shader stage.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="95f4b-163">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="95f4b-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95f4b-164">Referencia de los sombreadores</span><span class="sxs-lookup"><span data-stu-id="95f4b-164">Shader Reference</span></span>](d3d11-graphics-reference-d3d11-shader.md)
</dt> </dl>

 

