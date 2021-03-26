---
title: Empaquetado de una biblioteca de sombreador
description: Aquí le mostramos cómo compilar el código del sombreador, cargar el código compilado en una biblioteca de sombras y enlazar recursos de las ranuras de origen a las de destino.
ms.assetid: ED2EB1DE-3C25-4633-BFA7-C535ABBBAD28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90124ca9753a390b924d5ba702e1986e32eee9e5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997145"
---
# <a name="packaging-a-shader-library"></a><span data-ttu-id="e97cd-103">Empaquetado de una biblioteca de sombreador</span><span class="sxs-lookup"><span data-stu-id="e97cd-103">Packaging a shader library</span></span>

<span data-ttu-id="e97cd-104">Aquí le mostramos cómo compilar el código del sombreador, cargar el código compilado en una biblioteca de sombras y enlazar recursos de las ranuras de origen a las de destino.</span><span class="sxs-lookup"><span data-stu-id="e97cd-104">Here we show you how to compile your shader code, load the compiled code into a shader library, and bind resources from source slots to destination slots.</span></span>

<span data-ttu-id="e97cd-105">**Objetivo:** Para empaquetar una biblioteca de sombreador que se usará para la vinculación del sombreador.</span><span class="sxs-lookup"><span data-stu-id="e97cd-105">**Objective:** To package a shader library to use for shader linking.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e97cd-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e97cd-106">Prerequisites</span></span>

<span data-ttu-id="e97cd-107">Suponemos que estás familiarizado con C++.</span><span class="sxs-lookup"><span data-stu-id="e97cd-107">We assume that you are familiar with C++.</span></span> <span data-ttu-id="e97cd-108">También necesitas tener experiencia básica en los conceptos de programación de elementos gráficos.</span><span class="sxs-lookup"><span data-stu-id="e97cd-108">You also need basic experience with graphics programming concepts.</span></span>

<span data-ttu-id="e97cd-109">**Tiempo de finalización:** 30 minutos.</span><span class="sxs-lookup"><span data-stu-id="e97cd-109">**Time to complete:** 30 minutes.</span></span>

## <a name="instructions"></a><span data-ttu-id="e97cd-110">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="e97cd-110">Instructions</span></span>

### <a name="1-compiling-your-shader-code"></a><span data-ttu-id="e97cd-111">1. compilar el código del sombreador</span><span class="sxs-lookup"><span data-stu-id="e97cd-111">1. Compiling your shader code</span></span>

<span data-ttu-id="e97cd-112">Compile el código del sombreador con una de las funciones de compilación.</span><span class="sxs-lookup"><span data-stu-id="e97cd-112">Compile your shader code with one of the compile functions.</span></span> <span data-ttu-id="e97cd-113">Por ejemplo, este fragmento de código usa [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile).</span><span class="sxs-lookup"><span data-stu-id="e97cd-113">For example, this code snippet uses [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile).</span></span>

```cpp
    string source;
 
    ComPtr<ID3DBlob> codeBlob;
    ComPtr<ID3DBlob> errorBlob;
    HRESULT hr = D3DCompile(
        source.c_str(),
        source.size(),
        "ShaderModule",
        NULL,
        NULL,
        NULL,
        ("lib" + m_shaderModelSuffix).c_str(),
        D3DCOMPILE_OPTIMIZATION_LEVEL3,
        0,
        &codeBlob,
        &errorBlob
        );
```

<span data-ttu-id="e97cd-114">La cadena de origen contiene el código HLSL ASCII sin compilar.</span><span class="sxs-lookup"><span data-stu-id="e97cd-114">The source string contains the uncompiled ASCII HLSL code.</span></span>

### <a name="2-load-the-compiled-code-into-a-shader-library"></a><span data-ttu-id="e97cd-115">2. Cargue el código compilado en una biblioteca de sombreador.</span><span class="sxs-lookup"><span data-stu-id="e97cd-115">2. Load the compiled code into a shader library.</span></span>

<span data-ttu-id="e97cd-116">Llame a la función [**D3DLoadModule**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dloadmodule) para cargar el código compilado ([**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))) en un módulo ([**ID3D11Module**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11module)) que representa una biblioteca de sombreador.</span><span class="sxs-lookup"><span data-stu-id="e97cd-116">Call the [**D3DLoadModule**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dloadmodule) function to load the compiled code ([**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))) into a module ([**ID3D11Module**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11module)) that represents a shader library.</span></span>


```C++
    // Load the compiled library code into a module object.
    ComPtr<ID3D11Module> shaderLibrary;
    DX::ThrowIfFailed(D3DLoadModule(codeBlob->GetBufferPointer(), codeBlob->GetBufferSize(), &shaderLibrary));
```



### <a name="3-bind-resources-from-source-slots-to-destination-slots"></a><span data-ttu-id="e97cd-117">3. enlace recursos de las ranuras de origen a las de destino.</span><span class="sxs-lookup"><span data-stu-id="e97cd-117">3. Bind resources from source slots to destination slots.</span></span>

<span data-ttu-id="e97cd-118">Llame al método [**ID3D11Module:: CreateInstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11module-createinstance) para crear una instancia ([**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance)) de la biblioteca, de modo que pueda definir enlaces de recursos para la instancia.</span><span class="sxs-lookup"><span data-stu-id="e97cd-118">Call the [**ID3D11Module::CreateInstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11module-createinstance) method to create an instance ([**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance)) of the library so you can then define resource bindings for the instance.</span></span>

<span data-ttu-id="e97cd-119">Llame a los métodos BIND de [**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance) para enlazar los recursos que necesita de las ranuras de origen a las de destino.</span><span class="sxs-lookup"><span data-stu-id="e97cd-119">Call the bind methods of [**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance) to bind the resources you need from source slots to destination slots.</span></span> <span data-ttu-id="e97cd-120">Los recursos pueden ser texturas, búferes, muestreadores, búferes de constantes o UAVs.</span><span class="sxs-lookup"><span data-stu-id="e97cd-120">The resources can be textures, buffers, samplers, constant buffers, or UAVs.</span></span> <span data-ttu-id="e97cd-121">Normalmente, se usarán las mismas ranuras que la biblioteca de origen.</span><span class="sxs-lookup"><span data-stu-id="e97cd-121">Typically, you will use the same slots as the source library.</span></span>


```C++
    // Create an instance of the library and define resource bindings for it.
    // In this sample we use the same slots as the source library however this is not required.
    ComPtr<ID3D11ModuleInstance> shaderLibraryInstance;
    DX::ThrowIfFailed(shaderLibrary->CreateInstance("", &shaderLibraryInstance));
    // HRESULTs for Bind methods are intentionally ignored as compiler optimizations may eliminate the source
    // bindings. In these cases, the Bind operation will fail, but the final shader will function normally.
    shaderLibraryInstance->BindResource(0, 0, 1);
    shaderLibraryInstance->BindSampler(0, 0, 1);
    shaderLibraryInstance->BindConstantBuffer(0, 0, 0);
    shaderLibraryInstance->BindConstantBuffer(1, 1, 0);
    shaderLibraryInstance->BindConstantBuffer(2, 2, 0);
```



<span data-ttu-id="e97cd-122">Este código HLSL muestra que la biblioteca de origen utiliza las mismas ranuras (T0, S0, b0, B1 y B2) que las ranuras usadas en los métodos BIND anteriores de [**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance).</span><span class="sxs-lookup"><span data-stu-id="e97cd-122">This HLSL code shows that the source library uses the same slots (t0, s0, b0, b1, and b2) as the slots used in the preceding bind methods of [**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance).</span></span>

``` syntax
// This is the default code in the fixed header section.
Texture2D<float3> Texture : register(t0);
SamplerState Anisotropic : register(s0);
cbuffer CameraData : register(b0)
{
    float4x4 Model;
    float4x4 View;
    float4x4 Projection;
};
cbuffer TimeVariantSignals : register(b1)
{
    float SineWave;
    float SquareWave;
    float TriangleWave;
    float SawtoothWave;
};

// This code is not displayed, but is used as part of the linking process.
cbuffer HiddenBuffer : register(b2)
{
    float3 LightDirection;
};
```

## <a name="summary-and-next-steps"></a><span data-ttu-id="e97cd-123">Resumen y pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="e97cd-123">Summary and next steps</span></span>

<span data-ttu-id="e97cd-124">Hemos compilado el código del sombreador, cargado el código compilado en una biblioteca de sombras y los recursos enlazados desde las ranuras de origen a las ranuras de destino.</span><span class="sxs-lookup"><span data-stu-id="e97cd-124">We compiled shader code, loaded the compiled code into a shader library, and bound resources from source slots to destination slots.</span></span>

<span data-ttu-id="e97cd-125">A continuación, creamos los gráficos de vinculación de funciones (FLGs) para los sombreadores, los vinculamos al código compilado y generan los blobs de sombreador que el tiempo de ejecución de Direct3D puede usar.</span><span class="sxs-lookup"><span data-stu-id="e97cd-125">Next we construct function-linking-graphs (FLGs) for shaders, link them to compiled code, and produce shader blobs that the Direct3D runtime can use.</span></span>

[<span data-ttu-id="e97cd-126">Construir un grafo de función-vinculación y vincularlo a código compilado</span><span class="sxs-lookup"><span data-stu-id="e97cd-126">Constructing a function-linking-graph and linking it to compiled code</span></span>](constructing-a-function-linking-graph.md)

## <a name="related-topics"></a><span data-ttu-id="e97cd-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e97cd-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e97cd-128">Usar la vinculación del sombreador</span><span class="sxs-lookup"><span data-stu-id="e97cd-128">Using shader linking</span></span>](using-shader-linking.md)
</dt> </dl>

 

 