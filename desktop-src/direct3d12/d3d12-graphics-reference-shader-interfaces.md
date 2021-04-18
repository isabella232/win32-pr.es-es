---
title: Interfaces del sombreador (gráficos de Direct3D 12)
description: D3d12shader. h declara las siguientes interfaces.
ms.assetid: 791d2c91-3791-47fe-b887-8117ecc798ba
keywords:
- interfaces, sombreador de Direct3D 12
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16f111572aacca36f12600b0cf334895684064e5
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105720206"
---
# <a name="shader-interfaces-direct3d-12-graphics"></a><span data-ttu-id="ab57a-104">Interfaces del sombreador (gráficos de Direct3D 12)</span><span class="sxs-lookup"><span data-stu-id="ab57a-104">Shader Interfaces (Direct3D 12 Graphics)</span></span>

<span data-ttu-id="ab57a-105">d3d12shader. h declara las siguientes interfaces.</span><span class="sxs-lookup"><span data-stu-id="ab57a-105">d3d12shader.h declares the following interfaces.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ab57a-106">En esta sección</span><span class="sxs-lookup"><span data-stu-id="ab57a-106">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ab57a-107">Tema</span><span class="sxs-lookup"><span data-stu-id="ab57a-107">Topic</span></span></th>
<th><span data-ttu-id="ab57a-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="ab57a-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ab57a-109"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12functionparameterreflection"><strong>ID3D12FunctionParameterReflection</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab57a-109"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12functionparameterreflection"><strong>ID3D12FunctionParameterReflection</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab57a-110">Una interfaz de función-parámetro-reflexión obtiene acceso a la información de parámetros de función.</span><span class="sxs-lookup"><span data-stu-id="ab57a-110">A function-parameter-reflection interface accesses function-parameter info.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="ab57a-111">Esta interfaz forma parte de la tecnología de vinculación del sombreador de HLSL que puede usar en todas las plataformas de Direct3D 12 para crear funciones HLSL precompiladas, empaquetarlas en bibliotecas y vincularlas a los sombreadores completos en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="ab57a-111">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 12 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab57a-112"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12functionreflection"><strong>ID3D12FunctionReflection</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab57a-112"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12functionreflection"><strong>ID3D12FunctionReflection</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab57a-113">Una interfaz de reflexión de funciones obtiene acceso a la información de la función.</span><span class="sxs-lookup"><span data-stu-id="ab57a-113">A function-reflection interface accesses function info.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="ab57a-114">Esta interfaz forma parte de la tecnología de vinculación del sombreador de HLSL que puede usar en todas las plataformas de Direct3D 12 para crear funciones HLSL precompiladas, empaquetarlas en bibliotecas y vincularlas a los sombreadores completos en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="ab57a-114">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 12 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab57a-115"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12libraryreflection"><strong>ID3D12LibraryReflection</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab57a-115"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12libraryreflection"><strong>ID3D12LibraryReflection</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab57a-116">Una interfaz de reflexión de biblioteca obtiene acceso a la información de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="ab57a-116">A library-reflection interface accesses library info.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="ab57a-117">Esta interfaz forma parte de la tecnología de vinculación del sombreador de HLSL que puede usar en todas las plataformas de Direct3D 12 para crear funciones HLSL precompiladas, empaquetarlas en bibliotecas y vincularlas a los sombreadores completos en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="ab57a-117">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 12 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab57a-118"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflection"><strong>ID3D12ShaderReflection</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab57a-118"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflection"><strong>ID3D12ShaderReflection</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab57a-119">Una interfaz de reflexión del sombreador obtiene acceso a la información del sombreador.</span><span class="sxs-lookup"><span data-stu-id="ab57a-119">A shader-reflection interface accesses shader information.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab57a-120"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionconstantbuffer"><strong>ID3D12ShaderReflectionConstantBuffer</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab57a-120"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionconstantbuffer"><strong>ID3D12ShaderReflectionConstantBuffer</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab57a-121">Esta interfaz de reflexión del sombreador proporciona acceso a un búfer de constantes.</span><span class="sxs-lookup"><span data-stu-id="ab57a-121">This shader-reflection interface provides access to a constant buffer.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab57a-122"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectiontype"><strong>ID3D12ShaderReflectionType</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab57a-122"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectiontype"><strong>ID3D12ShaderReflectionType</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab57a-123">Esta interfaz de reflexión del sombreador proporciona acceso al tipo de variable.</span><span class="sxs-lookup"><span data-stu-id="ab57a-123">This shader-reflection interface provides access to variable type.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab57a-124"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionvariable"><strong>ID3D12ShaderReflectionVariable</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab57a-124"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionvariable"><strong>ID3D12ShaderReflectionVariable</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab57a-125">Esta interfaz de reflexión del sombreador proporciona acceso a una variable.</span><span class="sxs-lookup"><span data-stu-id="ab57a-125">This shader-reflection interface provides access to a variable.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="ab57a-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ab57a-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab57a-127">Referencia de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="ab57a-127">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> <dt>

[<span data-ttu-id="ab57a-128">Referencia de los sombreadores</span><span class="sxs-lookup"><span data-stu-id="ab57a-128">Shader Reference</span></span>](d3d12-graphics-reference-shader-reference.md)
</dt> </dl>

 

 





