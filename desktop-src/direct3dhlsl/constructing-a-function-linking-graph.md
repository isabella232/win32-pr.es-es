---
title: Construir un grafo de función-vinculación y vincularlo a código compilado
description: Aquí le mostramos cómo construir gráficos de vinculación de funciones (FLGs) para los sombreadores y cómo vincularlos con una biblioteca de sombreador para generar blobs de sombreador que el tiempo de ejecución de Direct3D puede usar.
ms.assetid: 82C3109E-8571-49D2-A8BF-298E30E1281B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c037e7ea111d11d24df173ffba7e56c8f486af82
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904739"
---
# <a name="constructing-a-function-linking-graph-and-linking-it-to-compiled-code"></a><span data-ttu-id="85535-103">Construir un grafo de función-vinculación y vincularlo a código compilado</span><span class="sxs-lookup"><span data-stu-id="85535-103">Constructing a function-linking-graph and linking it to compiled code</span></span>

<span data-ttu-id="85535-104">Aquí le mostramos cómo construir gráficos de vinculación de funciones (FLGs) para los sombreadores y cómo vincularlos con una biblioteca de sombreador para generar blobs de sombreador que el tiempo de ejecución de Direct3D puede usar.</span><span class="sxs-lookup"><span data-stu-id="85535-104">Here we show you how to construct function-linking-graphs (FLGs) for shaders and how to link those shaders with a shader library to produce shader blobs that the Direct3D runtime can use.</span></span>

<span data-ttu-id="85535-105">**Objetivo:** Para construir un grafo de función-vinculación y vincularlo a código compilado.</span><span class="sxs-lookup"><span data-stu-id="85535-105">**Objective:** To construct a function-linking-graph and link it to compiled code.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="85535-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="85535-106">Prerequisites</span></span>

<span data-ttu-id="85535-107">Suponemos que estás familiarizado con C++.</span><span class="sxs-lookup"><span data-stu-id="85535-107">We assume that you are familiar with C++.</span></span> <span data-ttu-id="85535-108">También necesitas tener experiencia básica en los conceptos de programación de elementos gráficos.</span><span class="sxs-lookup"><span data-stu-id="85535-108">You also need basic experience with graphics programming concepts.</span></span>

<span data-ttu-id="85535-109">También se supone que ha pasado por [el empaquetado de una biblioteca de sombreador](pachaging-a-shader-library.md).</span><span class="sxs-lookup"><span data-stu-id="85535-109">We also assume that you went through [Packaging a shader library](pachaging-a-shader-library.md).</span></span>

<span data-ttu-id="85535-110">**Tiempo de finalización:** 30 minutos.</span><span class="sxs-lookup"><span data-stu-id="85535-110">**Time to complete:** 30 minutes.</span></span>

## <a name="instructions"></a><span data-ttu-id="85535-111">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="85535-111">Instructions</span></span>

### <a name="1-construct-a-function-linking-graph-for-the-vertex-shader"></a><span data-ttu-id="85535-112">1. construya un grafo de función-vinculación para el sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="85535-112">1. Construct a function-linking-graph for the vertex shader.</span></span>

<span data-ttu-id="85535-113">Llame a la función [**D3DCreateFunctionLinkingGraph**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph) para crear un gráfico de vinculación de funciones ([**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)) que represente el sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="85535-113">Call the [**D3DCreateFunctionLinkingGraph**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph) function to create a function-linking-graph ([**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)) to represent the vertex shader.</span></span>

<span data-ttu-id="85535-114">Use una matriz de [**estructuras \_ \_ DESC del parámetro D3D11**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) para definir los parámetros de entrada para el sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="85535-114">Use an array of [**D3D11\_PARAMETER\_DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) structures to define the input parameters for the vertex shader.</span></span> <span data-ttu-id="85535-115">La [etapa del ensamblador de entrada](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-input-assembler-stage) alimenta los parámetros de entrada para el sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="85535-115">The [Input-Assembler Stage](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-input-assembler-stage) feeds the input parameters to the vertex shader.</span></span> <span data-ttu-id="85535-116">El diseño de los parámetros de entrada del sombreador de vértices coincide con el diseño del sombreador de vértices en el código compilado.</span><span class="sxs-lookup"><span data-stu-id="85535-116">The layout of the vertex shader’s input parameters matches the layout of the vertex shader in the compiled code.</span></span> <span data-ttu-id="85535-117">Después de definir los parámetros de entrada, llame al método [**ID3D11FunctionLinkingGraph:: SetInputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature) para definir el nodo de entrada ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) para el sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="85535-117">After you define the input parameters, call the [**ID3D11FunctionLinkingGraph::SetInputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature) method to define the input node ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) for the vertex shader.</span></span>


```C++
            ComPtr<ID3D11FunctionLinkingGraph> vertexShaderGraph;
            DX::ThrowIfFailed(D3DCreateFunctionLinkingGraph(0, &vertexShaderGraph));

            // Define the main input node which will be fed by the Input Assembler pipeline stage.
            static const D3D11_PARAMETER_DESC vertexShaderInputParameters[] =
            {
                {"inputPos",  "POSITION0", D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 3, D3D_INTERPOLATION_LINEAR, D3D_PF_IN, 0, 0, 0, 0},
                {"inputTex",  "TEXCOORD0", D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 2, D3D_INTERPOLATION_LINEAR, D3D_PF_IN, 0, 0, 0, 0},
                {"inputNorm", "NORMAL0",   D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 3, D3D_INTERPOLATION_LINEAR, D3D_PF_IN, 0, 0, 0, 0}
            };
            ComPtr<ID3D11LinkingNode> vertexShaderInputNode;
            LinkingThrowIfFailed(vertexShaderGraph->SetInputSignature(vertexShaderInputParameters, ARRAYSIZE(vertexShaderInputParameters), 
                &vertexShaderInputNode), vertexShaderGraph.Get());
```



<span data-ttu-id="85535-118">Llame al método [**ID3D11FunctionLinkingGraph:: CallFunction**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-callfunction) para crear un nodo para la función de sombreador de vértices principal y realizar llamadas a [**ID3D11FunctionLinkingGraph::P assvalue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) para pasar valores del nodo de entrada al nodo de la función de sombreador de vértices principal.</span><span class="sxs-lookup"><span data-stu-id="85535-118">Call the [**ID3D11FunctionLinkingGraph::CallFunction**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-callfunction) method to create a node for the main vertex shader function and make calls to [**ID3D11FunctionLinkingGraph::PassValue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) to pass values from the input node to the node for the main vertex shader function.</span></span>


```C++
            // Create a node for the main VertexFunction call using the output of the helper functions.
            ComPtr<ID3D11LinkingNode> vertexFunctionCallNode;
            LinkingThrowIfFailed(vertexShaderGraph->CallFunction("", shaderLibrary.Get(), "VertexFunction", &vertexFunctionCallNode), 
                vertexShaderGraph.Get());

            // Define the graph edges from the input node and helper function nodes.
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(homogenizeCallNodeForPos.Get(), D3D_RETURN_PARAMETER_INDEX, 
                vertexFunctionCallNode.Get(), 0), vertexShaderGraph.Get());
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(vertexShaderInputNode.Get(), 1, vertexFunctionCallNode.Get(), 1), 
                vertexShaderGraph.Get());
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(homogenizeCallNodeForNorm.Get(), D3D_RETURN_PARAMETER_INDEX, 
                vertexFunctionCallNode.Get(), 2), vertexShaderGraph.Get());
```



<span data-ttu-id="85535-119">Use una matriz de [**estructuras \_ \_ DESC del parámetro D3D11**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) para definir los parámetros de salida para el sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="85535-119">Use an array of [**D3D11\_PARAMETER\_DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) structures to define the output parameters for the vertex shader.</span></span> <span data-ttu-id="85535-120">El sombreador de vértices envía sus parámetros de salida al sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="85535-120">The vertex shader feeds its output parameters to the pixel shader.</span></span> <span data-ttu-id="85535-121">El diseño de los parámetros de salida del sombreador de vértices coincide con el diseño del sombreador de píxeles en el código compilado.</span><span class="sxs-lookup"><span data-stu-id="85535-121">The layout of the vertex shader’s output parameters matches the layout of the pixel shader in the compiled code.</span></span> <span data-ttu-id="85535-122">Después de definir los parámetros de salida, llame al método [**ID3D11FunctionLinkingGraph:: SetOutputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature) para definir el nodo de salida ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) para el sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="85535-122">After you define the output parameters, call the [**ID3D11FunctionLinkingGraph::SetOutputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature) method to define the output node ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) for the vertex shader.</span></span>


```C++
            // Define the main output node which will feed the Pixel Shader pipeline stage.
            static const D3D11_PARAMETER_DESC vertexShaderOutputParameters[] =
            {
                {"outputTex",  "TEXCOORD0",   D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 2, D3D_INTERPOLATION_UNDEFINED, D3D_PF_OUT, 0, 0, 0, 0},
                {"outputNorm", "NORMAL0",     D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 3, D3D_INTERPOLATION_UNDEFINED, D3D_PF_OUT, 0, 0, 0, 0},
                {"outputPos",  "SV_POSITION", D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 4, D3D_INTERPOLATION_UNDEFINED, D3D_PF_OUT, 0, 0, 0, 0}
            };
            ComPtr<ID3D11LinkingNode> vertexShaderOutputNode;
            LinkingThrowIfFailed(vertexShaderGraph->SetOutputSignature(vertexShaderOutputParameters, ARRAYSIZE(vertexShaderOutputParameters), 
                &vertexShaderOutputNode), vertexShaderGraph.Get());
```



<span data-ttu-id="85535-123">Realice llamadas a [**ID3D11FunctionLinkingGraph::P assvalue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) para pasar valores del nodo de la función de sombreador de vértices principal al nodo de salida.</span><span class="sxs-lookup"><span data-stu-id="85535-123">Make calls to [**ID3D11FunctionLinkingGraph::PassValue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) to pass values from the node for the main vertex shader function to the output node.</span></span>


```C++
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(vertexFunctionCallNode.Get(), 0, vertexShaderOutputNode.Get(), 2), 
                vertexShaderGraph.Get());
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(vertexFunctionCallNode.Get(), 1, vertexShaderOutputNode.Get(), 0), 
                vertexShaderGraph.Get());
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(vertexFunctionCallNode.Get(), 2, vertexShaderOutputNode.Get(), 1), 
                vertexShaderGraph.Get());
```



<span data-ttu-id="85535-124">Llame al método [**ID3D11FunctionLinkingGraph:: CreateModuleInstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-createmoduleinstance) para finalizar el gráfico del sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="85535-124">Call the [**ID3D11FunctionLinkingGraph::CreateModuleInstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-createmoduleinstance) method to finalize the vertex shader graph.</span></span>


```C++
            // Finalize the vertex shader graph.
            ComPtr<ID3D11ModuleInstance> vertexShaderGraphInstance;
            LinkingThrowIfFailed(vertexShaderGraph->CreateModuleInstance(&vertexShaderGraphInstance, nullptr), vertexShaderGraph.Get());
```



### <a name="2-link-the-vertex-shader"></a><span data-ttu-id="85535-125">2. vincular el sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="85535-125">2. Link the vertex shader</span></span>

<span data-ttu-id="85535-126">Llame a la función [**D3DCreateLinker**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker) para crear un vinculador ([**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)) que puede usar para vincular la instancia de la biblioteca de sombreador que creó en el [empaquetado de una biblioteca de sombreador](pachaging-a-shader-library.md) con la instancia del gráfico de sombreador de vértices que creó en el paso anterior.</span><span class="sxs-lookup"><span data-stu-id="85535-126">Call the [**D3DCreateLinker**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker) function to create a linker ([**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)) that you can use to link the instance of the shader library that you created in [Packaging a shader library](pachaging-a-shader-library.md) with the instance of the vertex shader graph that you created in the preceding step.</span></span> <span data-ttu-id="85535-127">Llame al método [**ID3D11Linker:: UseLibrary**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-uselibrary) para especificar la biblioteca de sombreador que se va a usar para la vinculación.</span><span class="sxs-lookup"><span data-stu-id="85535-127">Call the [**ID3D11Linker::UseLibrary**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-uselibrary) method to specify the shader library to use for linking.</span></span> <span data-ttu-id="85535-128">Llame al método [**ID3D11Linker:: Link**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-link) para vincular la biblioteca de sombreador con el gráfico del sombreador de vértices y generar un puntero a la interfaz [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) que puede usar para tener acceso al código del sombreador de vértices compilado.</span><span class="sxs-lookup"><span data-stu-id="85535-128">Call the [**ID3D11Linker::Link**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-link) method to link the shader library with the vertex shader graph and to produce a pointer to the [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) interface that you can use to access the compiled vertex shader code.</span></span> <span data-ttu-id="85535-129">Después, puede pasar este código del sombreador de vértices compilado al método [**ID3D11Device:: CreateVertexShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createvertexshader) para crear el objeto de sombreador de vértices y al método [**ID3D11Device:: CreateInputLayout**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createinputlayout) para crear el objeto de diseño de entrada.</span><span class="sxs-lookup"><span data-stu-id="85535-129">You can then pass this compiled vertex shader code to the [**ID3D11Device::CreateVertexShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createvertexshader) method to create the vertex shader object and to the [**ID3D11Device::CreateInputLayout**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createinputlayout) method to create the input-layout object.</span></span>


```C++
            // Create a linker and hook up the module instance.
            ComPtr<ID3D11Linker> linker;
            DX::ThrowIfFailed(D3DCreateLinker(&linker));
            DX::ThrowIfFailed(linker->UseLibrary(shaderLibraryInstance.Get()));

            // Link the vertex shader.
            ComPtr<ID3DBlob> errorBlob;
            if (FAILED(linker->Link(vertexShaderGraphInstance.Get(), "main", ("vs" + m_shaderModelSuffix).c_str(), 0, &vertexShaderBlob, 
                &errorBlob)))
            {
                throw errorBlob;
            }


    ComPtr<ID3D11VertexShader> vertexShader;
    DX::ThrowIfFailed(
        device->CreateVertexShader(
            vertexShaderBlob->GetBufferPointer(),
            vertexShaderBlob->GetBufferSize(),
            nullptr,
            &vertexShader
            )
        );
    context->VSSetShader(vertexShader.Get(), nullptr, 0);
    D3D11_INPUT_ELEMENT_DESC inputLayoutDesc[] =
    {
        { "POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT, 0, 0,  D3D11_INPUT_PER_VERTEX_DATA, 0 },
        { "TEXCOORD", 0, DXGI_FORMAT_R32G32_FLOAT,    0, 12, D3D11_INPUT_PER_VERTEX_DATA, 0 },
        { "NORMAL",   0, DXGI_FORMAT_R32G32B32_FLOAT, 0, 20, D3D11_INPUT_PER_VERTEX_DATA, 0 }
    };
    ComPtr<ID3D11InputLayout> inputLayout;
    DX::ThrowIfFailed(device->CreateInputLayout(inputLayoutDesc, ARRAYSIZE(inputLayoutDesc), vertexShaderBlob->GetBufferPointer(), vertexShaderBlob->GetBufferSize(), &inputLayout));
    context->IASetInputLayout(inputLayout.Get());
```



### <a name="3-construct-a-function-linking-graph-for-the-pixel-shader"></a><span data-ttu-id="85535-130">3. construir un grafo de función-vinculación para el sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="85535-130">3. Construct a function-linking-graph for the pixel shader.</span></span>

<span data-ttu-id="85535-131">Llame a la función [**D3DCreateFunctionLinkingGraph**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph) para crear un gráfico de vinculación de funciones ([**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)) que represente el sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="85535-131">Call the [**D3DCreateFunctionLinkingGraph**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph) function to create a function-linking-graph ([**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)) to represent the pixel shader.</span></span>

<span data-ttu-id="85535-132">Use una matriz de [**estructuras \_ \_ DESC del parámetro D3D11**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) para definir los parámetros de entrada para el sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="85535-132">Use an array of [**D3D11\_PARAMETER\_DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) structures to define the input parameters for the pixel shader.</span></span> <span data-ttu-id="85535-133">La fase del sombreador de vértices alimenta los parámetros de entrada para el sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="85535-133">The vertex shader stage feeds the input parameters to the pixel shader.</span></span> <span data-ttu-id="85535-134">El diseño de los parámetros de entrada del sombreador de píxeles coincide con el diseño del sombreador de píxeles en el código compilado.</span><span class="sxs-lookup"><span data-stu-id="85535-134">The layout of the pixel shader’s input parameters matches the layout of the pixel shader in the compiled code.</span></span> <span data-ttu-id="85535-135">Después de definir los parámetros de entrada, llame al método [**ID3D11FunctionLinkingGraph:: SetInputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature) para definir el nodo de entrada ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) para el sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="85535-135">After you define the input parameters, call the [**ID3D11FunctionLinkingGraph::SetInputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature) method to define the input node ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) for the pixel shader.</span></span>


```C++
            ComPtr<ID3D11FunctionLinkingGraph> pixelShaderGraph;
            DX::ThrowIfFailed(D3DCreateFunctionLinkingGraph(0, &pixelShaderGraph));

            // Define the main input node which will be fed by the vertex shader pipeline stage.
            static const D3D11_PARAMETER_DESC pixelShaderInputParameters[] =
            {
                {"inputTex",  "TEXCOORD0",   D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 2, D3D_INTERPOLATION_UNDEFINED, D3D_PF_IN, 0, 0, 0, 0},
                {"inputNorm", "NORMAL0",     D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 3, D3D_INTERPOLATION_UNDEFINED, D3D_PF_IN, 0, 0, 0, 0},
                {"inputPos",  "SV_POSITION", D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 4, D3D_INTERPOLATION_UNDEFINED, D3D_PF_IN, 0, 0, 0, 0}
            };
            ComPtr<ID3D11LinkingNode> pixelShaderInputNode;
            LinkingThrowIfFailed(pixelShaderGraph->SetInputSignature(pixelShaderInputParameters, ARRAYSIZE(pixelShaderInputParameters), 
                &pixelShaderInputNode), pixelShaderGraph.Get());
```



<span data-ttu-id="85535-136">Llame al método [**ID3D11FunctionLinkingGraph:: CallFunction**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-callfunction) para crear un nodo para la función de sombreador de píxeles principal y realizar llamadas a [**ID3D11FunctionLinkingGraph::P assvalue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) para pasar valores del nodo de entrada al nodo de la función de sombreador de píxeles principal.</span><span class="sxs-lookup"><span data-stu-id="85535-136">Call the [**ID3D11FunctionLinkingGraph::CallFunction**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-callfunction) method to create a node for the main pixel shader function and make calls to [**ID3D11FunctionLinkingGraph::PassValue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) to pass values from the input node to the node for the main pixel shader function.</span></span>


```C++
            // Create a node for the main ColorFunction call and connect it to the pixel shader inputs.
            ComPtr<ID3D11LinkingNode> colorValueNode;
            LinkingThrowIfFailed(pixelShaderGraph->CallFunction("", shaderLibrary.Get(), "ColorFunction", &colorValueNode), 
                pixelShaderGraph.Get());

            // Define the graph edges from the input node.
            LinkingThrowIfFailed(pixelShaderGraph->PassValue(pixelShaderInputNode.Get(), 0, colorValueNode.Get(), 0), 
                pixelShaderGraph.Get());
            LinkingThrowIfFailed(pixelShaderGraph->PassValue(pixelShaderInputNode.Get(), 1, colorValueNode.Get(), 1), 
                pixelShaderGraph.Get());
```



<span data-ttu-id="85535-137">Use una matriz de [**estructuras \_ \_ DESC del parámetro D3D11**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) para definir los parámetros de salida para el sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="85535-137">Use an array of [**D3D11\_PARAMETER\_DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) structures to define the output parameters for the pixel shader.</span></span> <span data-ttu-id="85535-138">El sombreador de píxeles envía sus parámetros de salida a la [fase de combinación de salida](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage).</span><span class="sxs-lookup"><span data-stu-id="85535-138">The pixel shader feeds its output parameters to the [Output-Merger Stage](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage).</span></span> <span data-ttu-id="85535-139">Después de definir los parámetros de salida, llame al método [**ID3D11FunctionLinkingGraph:: SetOutputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature) para definir el nodo de salida ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) para el sombreador de píxeles y realizar llamadas a [**ID3D11FunctionLinkingGraph::P assvalue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) para pasar valores de un nodo de función de sombreador de píxeles al nodo de salida.</span><span class="sxs-lookup"><span data-stu-id="85535-139">After you define the output parameters, call the [**ID3D11FunctionLinkingGraph::SetOutputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature) method to define the output node ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) for the pixel shader and make calls to [**ID3D11FunctionLinkingGraph::PassValue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) to pass values from a pixel shader function node to the output node.</span></span>


```C++
            // Define the main output node which will feed the Output Merger pipeline stage.
            D3D11_PARAMETER_DESC pixelShaderOutputParameters[] =
            {
                {"outputColor", "SV_TARGET", D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 4, D3D_INTERPOLATION_UNDEFINED, D3D_PF_OUT, 0, 0, 0, 0}
            };
            ComPtr<ID3D11LinkingNode> pixelShaderOutputNode;
            LinkingThrowIfFailed(pixelShaderGraph->SetOutputSignature(pixelShaderOutputParameters, ARRAYSIZE(pixelShaderOutputParameters), 
                &pixelShaderOutputNode), pixelShaderGraph.Get());
            LinkingThrowIfFailed(pixelShaderGraph->PassValue(fillAlphaCallNode.Get(), D3D_RETURN_PARAMETER_INDEX, pixelShaderOutputNode.Get(), 0), 
                pixelShaderGraph.Get());
```



<span data-ttu-id="85535-140">Llame al método [**ID3D11FunctionLinkingGraph:: CreateModuleInstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-createmoduleinstance) para finalizar el gráfico del sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="85535-140">Call the [**ID3D11FunctionLinkingGraph::CreateModuleInstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-createmoduleinstance) method to finalize the pixel shader graph.</span></span>


```C++
            // Finalize the pixel shader graph.
            ComPtr<ID3D11ModuleInstance> pixelShaderGraphInstance;
            LinkingThrowIfFailed(pixelShaderGraph->CreateModuleInstance(&pixelShaderGraphInstance, nullptr), pixelShaderGraph.Get());
```



### <a name="4-link-the-pixel-shader"></a><span data-ttu-id="85535-141">4. vincular el sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="85535-141">4. Link the pixel shader</span></span>

<span data-ttu-id="85535-142">Llame a la función [**D3DCreateLinker**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker) para crear un vinculador ([**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)) que puede usar para vincular la instancia de la biblioteca de sombreador que creó en el [empaquetado de una biblioteca de sombreador](pachaging-a-shader-library.md) con la instancia del gráfico de sombreador de píxeles que creó en el paso anterior.</span><span class="sxs-lookup"><span data-stu-id="85535-142">Call the [**D3DCreateLinker**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker) function to create a linker ([**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)) that you can use to link the instance of the shader library that you created in [Packaging a shader library](pachaging-a-shader-library.md) with the instance of the pixel shader graph that you created in the preceding step.</span></span> <span data-ttu-id="85535-143">Llame al método [**ID3D11Linker:: UseLibrary**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-uselibrary) para especificar la biblioteca de sombreador que se va a usar para la vinculación.</span><span class="sxs-lookup"><span data-stu-id="85535-143">Call the [**ID3D11Linker::UseLibrary**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-uselibrary) method to specify the shader library to use for linking.</span></span> <span data-ttu-id="85535-144">Llame al método [**ID3D11Linker:: Link**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-link) para vincular la biblioteca de sombreador con el gráfico del sombreador de píxeles y generar un puntero a la interfaz [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) que puede usar para tener acceso al código del sombreador de píxeles compilado.</span><span class="sxs-lookup"><span data-stu-id="85535-144">Call the [**ID3D11Linker::Link**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-link) method to link the shader library with the pixel shader graph and to produce a pointer to the [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) interface that you can use to access the compiled pixel shader code.</span></span> <span data-ttu-id="85535-145">Después, puede pasar este código de sombreador de píxeles compilado al método [**ID3D11Device:: CreatePixelShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createpixelshader) para crear el objeto de sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="85535-145">You can then pass this compiled pixel shader code to the [**ID3D11Device::CreatePixelShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createpixelshader) method to create the pixel shader object.</span></span>


```C++
            // Create a linker and hook up the module instance.
            ComPtr<ID3D11Linker> linker;
            DX::ThrowIfFailed(D3DCreateLinker(&linker));
            DX::ThrowIfFailed(linker->UseLibrary(shaderLibraryInstance.Get()));

            // Link the pixel shader.
            ComPtr<ID3DBlob> errorBlob;
            if (FAILED(linker->Link(pixelShaderGraphInstance.Get(), "main", ("ps" + m_shaderModelSuffix).c_str(), 0, &pixelShaderBlob, &errorBlob)))
            {
                throw errorBlob;
            }


    ComPtr<ID3D11PixelShader> pixelShader;
    DX::ThrowIfFailed(
        device->CreatePixelShader(
            pixelShaderBlob->GetBufferPointer(),
            pixelShaderBlob->GetBufferSize(),
            nullptr,
            &pixelShader
            )
        );
    context->PSSetShader(pixelShader.Get(), nullptr, 0);
```



## <a name="summary"></a><span data-ttu-id="85535-146">Resumen</span><span class="sxs-lookup"><span data-stu-id="85535-146">Summary</span></span>

<span data-ttu-id="85535-147">Usamos los métodos [**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph) para construir los gráficos de sombreador de vértices y píxeles y para especificar la estructura del sombreador mediante programación.</span><span class="sxs-lookup"><span data-stu-id="85535-147">We used the [**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph) methods to construct the vertex and pixel shader graphs and to specify the shader structure programmatically.</span></span>

<span data-ttu-id="85535-148">Estas construcciones de grafos están formadas por secuencias de llamadas a funciones precompiladas que pasan valores entre sí.</span><span class="sxs-lookup"><span data-stu-id="85535-148">These graph constructions consist of sequences of precompiled function calls that pass values to each other.</span></span> <span data-ttu-id="85535-149">Los nodos FLG ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) representan los nodos del sombreador de entrada y salida y las invocaciones de las funciones de biblioteca precompiladas.</span><span class="sxs-lookup"><span data-stu-id="85535-149">FLG nodes ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) represent input and output shader nodes and invocations of precompiled library functions.</span></span> <span data-ttu-id="85535-150">El orden en el que se registran los nodos de llamada de función define la secuencia de invocaciones.</span><span class="sxs-lookup"><span data-stu-id="85535-150">The order in which you register the function-call nodes defines the sequence of invocations.</span></span> <span data-ttu-id="85535-151">Debe especificar primero el nodo de entrada ([**ID3D11FunctionLinkingGraph:: SetInputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature)) y el nodo de salida en último lugar ([**ID3D11FunctionLinkingGraph:: SetOutputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature)).</span><span class="sxs-lookup"><span data-stu-id="85535-151">You must specify the input node ([**ID3D11FunctionLinkingGraph::SetInputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature)) first and the output node last ([**ID3D11FunctionLinkingGraph::SetOutputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature)).</span></span> <span data-ttu-id="85535-152">Los bordes de FLG definen cómo se pasan los valores de un nodo a otro.</span><span class="sxs-lookup"><span data-stu-id="85535-152">FLG edges define how values are passed from one node to another.</span></span> <span data-ttu-id="85535-153">Los tipos de datos de los valores pasados deben ser iguales; no hay ninguna conversión de tipo implícita.</span><span class="sxs-lookup"><span data-stu-id="85535-153">The data types of passed values must be the same; there is no implicit type conversion.</span></span> <span data-ttu-id="85535-154">Las reglas de forma y permutación siguen el comportamiento de HLSL.</span><span class="sxs-lookup"><span data-stu-id="85535-154">Shape and swizzling rules follow the HLSL behavior.</span></span> <span data-ttu-id="85535-155">Los valores solo se pueden pasar hacia delante en esta secuencia.</span><span class="sxs-lookup"><span data-stu-id="85535-155">Values can only be passed forward in this sequence.</span></span>

<span data-ttu-id="85535-156">También usamos métodos [**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker) para vincular la biblioteca de sombreador con los gráficos del sombreador y generar blobs de sombreador para que los use el tiempo de ejecución de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="85535-156">We also used [**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker) methods to link the shader library with the shader graphs and to produce shader blobs for the Direct3D runtime to use.</span></span>

<span data-ttu-id="85535-157">¡Enhorabuena!</span><span class="sxs-lookup"><span data-stu-id="85535-157">Congratulations!</span></span> <span data-ttu-id="85535-158">Ahora está listo para usar la vinculación del sombreador en sus propias aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="85535-158">You are now ready to use shader linking in your own apps.</span></span>

## <a name="related-topics"></a><span data-ttu-id="85535-159">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="85535-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85535-160">Usar la vinculación del sombreador</span><span class="sxs-lookup"><span data-stu-id="85535-160">Using shader linking</span></span>](using-shader-linking.md)
</dt> </dl>

 

 