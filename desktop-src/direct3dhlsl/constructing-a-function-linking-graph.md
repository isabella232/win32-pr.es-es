---
title: Crear un gráfico de vinculación de función y vincularlo al código compilado
description: Aquí se muestra cómo construir gráficos de vinculación de funciones (FLG) para sombreadores y cómo vincular esos sombreadores con una biblioteca de sombreadores para generar blobs de sombreador que el tiempo de ejecución de Direct3D puede usar.
ms.assetid: 82C3109E-8571-49D2-A8BF-298E30E1281B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c037e7ea111d11d24df173ffba7e56c8f486af82
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127264364"
---
# <a name="constructing-a-function-linking-graph-and-linking-it-to-compiled-code"></a>Crear un gráfico de vinculación de función y vincularlo al código compilado

Aquí se muestra cómo construir gráficos de vinculación de funciones (FLG) para sombreadores y cómo vincular esos sombreadores con una biblioteca de sombreadores para generar blobs de sombreador que el tiempo de ejecución de Direct3D puede usar.

**Objetivo:** Para construir un gráfico de vinculación de función y vincularlo al código compilado.

## <a name="prerequisites"></a>Prerrequisitos

Suponemos que estás familiarizado con C++. También necesitas tener experiencia básica en los conceptos de programación de elementos gráficos.

También se supone que ha pasado por [Empaquetado de una biblioteca de sombreadores.](pachaging-a-shader-library.md)

**Tiempo de ejecución:** 30 minutos.

## <a name="instructions"></a>Instructions

### <a name="1-construct-a-function-linking-graph-for-the-vertex-shader"></a>1. Cree un gráfico de vinculación de función para el sombreador de vértices.

Llame a la [**función D3DCreateFunctionLinkingGraph**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph) para crear una función-linking-graph ([**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)) para representar el sombreador de vértices.

Use una matriz de [**estructuras D3D11 \_ PARAMETER \_ DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) para definir los parámetros de entrada para el sombreador de vértices. La [fase Input-Assembler alimenta](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-input-assembler-stage) los parámetros de entrada al sombreador de vértices. El diseño de los parámetros de entrada del sombreador de vértices coincide con el diseño del sombreador de vértices en el código compilado. Después de definir los parámetros de entrada, llame al método [**ID3D11FunctionLinkingGraph::SetInputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature) para definir el nodo de entrada ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) para el sombreador de vértices.


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



Llame al método [**ID3D11FunctionLinkingGraph::CallFunction**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-callfunction) para crear un nodo para la función principal del sombreador de vértices y realizar llamadas a [**ID3D11FunctionLinkingGraph::P assValue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) para pasar valores del nodo de entrada al nodo de la función principal del sombreador de vértices.


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



Use una matriz de [**estructuras D3D11 \_ PARAMETER \_ DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) para definir los parámetros de salida para el sombreador de vértices. El sombreador de vértices alimenta sus parámetros de salida al sombreador de píxeles. El diseño de los parámetros de salida del sombreador de vértices coincide con el diseño del sombreador de píxeles en el código compilado. Después de definir los parámetros de salida, llame al método [**ID3D11FunctionLinkingGraph::SetOutputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature) para definir el nodo de salida ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) para el sombreador de vértices.


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



Realice llamadas a [**ID3D11FunctionLinkingGraph::P assValue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) para pasar valores del nodo para la función principal del sombreador de vértices al nodo de salida.


```C++
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(vertexFunctionCallNode.Get(), 0, vertexShaderOutputNode.Get(), 2), 
                vertexShaderGraph.Get());
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(vertexFunctionCallNode.Get(), 1, vertexShaderOutputNode.Get(), 0), 
                vertexShaderGraph.Get());
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(vertexFunctionCallNode.Get(), 2, vertexShaderOutputNode.Get(), 1), 
                vertexShaderGraph.Get());
```



Llame al [**método ID3D11FunctionLinkingGraph::CreateModuleInstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-createmoduleinstance) para finalizar el gráfico del sombreador de vértices.


```C++
            // Finalize the vertex shader graph.
            ComPtr<ID3D11ModuleInstance> vertexShaderGraphInstance;
            LinkingThrowIfFailed(vertexShaderGraph->CreateModuleInstance(&vertexShaderGraphInstance, nullptr), vertexShaderGraph.Get());
```



### <a name="2-link-the-vertex-shader"></a>2. Vincular el sombreador de vértices

Llame a la función [**D3DCreateLinker**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker) para crear un vinculador [**(ID3D11Linker)**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)que puede usar [](pachaging-a-shader-library.md) para vincular la instancia de la biblioteca de sombreadores que creó en Empaquetado de una biblioteca de sombreadores con la instancia del gráfico del sombreador de vértices que creó en el paso anterior. Llame al [**método ID3D11Linker::UseLibrary**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-uselibrary) para especificar la biblioteca de sombreadores que se usará para la vinculación. Llame al [**método ID3D11Linker::Link**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-link) para vincular la biblioteca de sombreadores con el gráfico del sombreador de vértices y generar un puntero a la interfaz [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) que puede usar para acceder al código compilado del sombreador de vértices. Después, puede pasar este código compilado del sombreador de vértices al método [**ID3D11Device::CreateVertexShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createvertexshader) para crear el objeto de sombreador de vértices y al método [**ID3D11Device::CreateInputLayout para**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createinputlayout) crear el objeto de diseño de entrada.


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



### <a name="3-construct-a-function-linking-graph-for-the-pixel-shader"></a>3. Cree un gráfico de vinculación de función para el sombreador de píxeles.

Llame a la [**función D3DCreateFunctionLinkingGraph**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph) para crear una función-linking-graph ([**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)) para representar el sombreador de píxeles.

Use una matriz de [**estructuras D3D11 \_ PARAMETER \_ DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) para definir los parámetros de entrada para el sombreador de píxeles. La fase del sombreador de vértices alimenta los parámetros de entrada al sombreador de píxeles. El diseño de los parámetros de entrada del sombreador de píxeles coincide con el diseño del sombreador de píxeles en el código compilado. Después de definir los parámetros de entrada, llame al método [**ID3D11FunctionLinkingGraph::SetInputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature) para definir el nodo de entrada ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) para el sombreador de píxeles.


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



Llame al método [**ID3D11FunctionLinkingGraph::CallFunction**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-callfunction) para crear un nodo para la función principal del sombreador de píxeles y realizar llamadas a [**ID3D11FunctionLinkingGraph::P assValue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) para pasar valores del nodo de entrada al nodo de la función principal del sombreador de píxeles.


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



Use una matriz de [**estructuras D3D11 \_ PARAMETER \_ DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) para definir los parámetros de salida para el sombreador de píxeles. El sombreador de píxeles alimenta sus parámetros de salida a [la fase output-merger](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage). Después de definir los parámetros de salida, llame al método [**ID3D11FunctionLinkingGraph::SetOutputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature) para definir el nodo de salida ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) para el sombreador de píxeles y realice llamadas a [**ID3D11FunctionLinkingGraph::P assValue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) para pasar valores de un nodo de función de sombreador de píxeles al nodo de salida.


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



Llame al [**método ID3D11FunctionLinkingGraph::CreateModuleInstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-createmoduleinstance) para finalizar el gráfico del sombreador de píxeles.


```C++
            // Finalize the pixel shader graph.
            ComPtr<ID3D11ModuleInstance> pixelShaderGraphInstance;
            LinkingThrowIfFailed(pixelShaderGraph->CreateModuleInstance(&pixelShaderGraphInstance, nullptr), pixelShaderGraph.Get());
```



### <a name="4-link-the-pixel-shader"></a>4. Vincular el sombreador de píxeles

Llame a la función [**D3DCreateLinker**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker) para crear un vinculador [**(ID3D11Linker)**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)que puede usar [](pachaging-a-shader-library.md) para vincular la instancia de la biblioteca de sombreadores que creó en Empaquetado de una biblioteca de sombreadores con la instancia del gráfico de sombreador de píxeles que creó en el paso anterior. Llame al [**método ID3D11Linker::UseLibrary**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-uselibrary) para especificar la biblioteca de sombreadores que se usará para la vinculación. Llame al [**método ID3D11Linker::Link**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-link) para vincular la biblioteca de sombreadores con el gráfico de sombreador de píxeles y generar un puntero a la interfaz [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) que puede usar para tener acceso al código del sombreador de píxeles compilado. A continuación, puede pasar este código de sombreador de píxeles compilado al [**método ID3D11Device::CreatePixelShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createpixelshader) para crear el objeto de sombreador de píxeles.


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



## <a name="summary"></a>Resumen

Hemos usado los [**métodos ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph) para construir los gráficos de sombreador de vértices y píxeles y para especificar la estructura del sombreador mediante programación.

Estas construcciones de grafo constan de secuencias de llamadas de función precompiladas que pasan valores entre sí. Los nodos FLG [**(ID3D11LinkingNode)**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)representan nodos de sombreador de entrada y salida e invocaciones de funciones de biblioteca precompiladas. El orden en el que se registran los nodos de llamada de función define la secuencia de invocaciones. Debe especificar primero el nodo de entrada ([**ID3D11FunctionLinkingGraph::SetInputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature)) y el nodo de salida en último lugar ([**ID3D11FunctionLinkingGraph::SetOutputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature)). Los bordes flg definen cómo se pasan los valores de un nodo a otro. Los tipos de datos de los valores pasados deben ser los mismos; no hay ninguna conversión implícita de tipos. Las reglas de forma y desdobada siguen el comportamiento hlsl. Los valores solo se pueden pasar hacia delante en esta secuencia.

También usamos [**métodos ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker) para vincular la biblioteca de sombreadores con los gráficos de sombreador y para generar blobs de sombreador para que los use el entorno de ejecución de Direct3D.

Felicidades. Ya está listo para usar la vinculación de sombreador en sus propias aplicaciones.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de la vinculación de sombreador](using-shader-linking.md)
</dt> </dl>

 

 