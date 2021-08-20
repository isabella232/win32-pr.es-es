---
title: Empaquetado de una biblioteca de sombreadores
description: Aquí se muestra cómo compilar el código del sombreador, cargar el código compilado en una biblioteca de sombreadores y enlazar recursos desde ranuras de origen a ranuras de destino.
ms.assetid: ED2EB1DE-3C25-4633-BFA7-C535ABBBAD28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afb0f16d226357aca63259a9cc014a3c149d84b87d1b9340b1452b802e0df410
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117906443"
---
# <a name="packaging-a-shader-library"></a>Empaquetado de una biblioteca de sombreadores

Aquí se muestra cómo compilar el código del sombreador, cargar el código compilado en una biblioteca de sombreadores y enlazar recursos desde ranuras de origen a ranuras de destino.

**Objetivo:** Para empaquetar una biblioteca de sombreador que se usará para la vinculación del sombreador.

## <a name="prerequisites"></a>Requisitos previos

Suponemos que estás familiarizado con C++. También necesitas tener experiencia básica en los conceptos de programación de elementos gráficos.

**Tiempo de ejecución:** 30 minutos.

## <a name="instructions"></a>Instructions

### <a name="1-compiling-your-shader-code"></a>1. Compilación del código del sombreador

Compile el código del sombreador con una de las funciones de compilación. Por ejemplo, este fragmento de código [**usa D3DCompile.**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile)

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

La cadena de origen contiene el código HLSL ASCII nocompilado.

### <a name="2-load-the-compiled-code-into-a-shader-library"></a>2. Cargue el código compilado en una biblioteca de sombreadores.

Llame a la función [**D3DLoadModule**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dloadmodule) para cargar el código compilado ([**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))) en un módulo ([**ID3D11Module**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11module)) que representa una biblioteca de sombreadores.


```C++
    // Load the compiled library code into a module object.
    ComPtr<ID3D11Module> shaderLibrary;
    DX::ThrowIfFailed(D3DLoadModule(codeBlob->GetBufferPointer(), codeBlob->GetBufferSize(), &shaderLibrary));
```



### <a name="3-bind-resources-from-source-slots-to-destination-slots"></a>3. Enlace recursos de ranuras de origen a ranuras de destino.

Llame al [**método ID3D11Module::CreateInstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11module-createinstance) para crear una instancia ([**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance)) de la biblioteca para que pueda definir enlaces de recursos para la instancia.

Llame a los métodos de enlace [**de ID3D11ModuleInstance para**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance) enlazar los recursos que necesita desde las ranuras de origen a las ranuras de destino. Los recursos pueden ser texturas, búferes, muestreadores, búferes constantes o UAV. Normalmente, usará las mismas ranuras que la biblioteca de origen.


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



Este código HLSL muestra que la biblioteca de origen usa las mismas ranuras (t0, s0, b0, b1 y b2) que las ranuras usadas en los métodos de enlace anteriores de [**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance).

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

## <a name="summary-and-next-steps"></a>Resumen y pasos siguientes

Compilamos código de sombreador, cargamos el código compilado en una biblioteca de sombreadores y enlazamos recursos de ranuras de origen a ranuras de destino.

A continuación, creamos gráficos de vinculación de funciones (FLG) para sombreadores, los vinculamos al código compilado y generamos blobs de sombreador que el tiempo de ejecución de Direct3D puede usar.

[Crear un gráfico de vinculación de función y vincularlo al código compilado](constructing-a-function-linking-graph.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de la vinculación de sombreador](using-shader-linking.md)
</dt> </dl>

 

 