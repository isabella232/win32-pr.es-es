---
title: Cómo compilar un sombreador
description: En este tema se muestra cómo usar la función D3DCompileFromFile en tiempo de ejecución para compilar el código del sombreador.
ms.assetid: A2CE368F-E72A-453D-BA4D-3D1D53DDDEE0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0ccda5ee552ed1c7cb40802d92a4562b85c7f36
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880661"
---
# <a name="how-to-compile-a-shader"></a>Cómo: Compilar un sombreador

Normalmente se usa el [fxc.exe](/windows/desktop/direct3dtools/fxc) de código HLSL como parte del proceso de compilación para compilar el código del sombreador. Para obtener más información sobre esto, vea [Compilar sombreadores](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-part1). En este tema se muestra cómo usar la [**función D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile) en tiempo de ejecución para compilar el código del sombreador.

**Para compilar un sombreador:**

-   Compile el código del sombreador HLSL mediante una llamada [**a D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile).
    ```C++
        UINT flags = D3DCOMPILE_ENABLE_STRICTNESS;
    #if defined( DEBUG ) || defined( _DEBUG )
        flags |= D3DCOMPILE_DEBUG;
    #endif
        // Prefer higher CS shader profile when possible as CS 5.0 provides better performance on 11-class hardware.
        LPCSTR profile = ( device->GetFeatureLevel() >= D3D_FEATURE_LEVEL_11_0 ) ? "cs_5_0" : "cs_4_0";
        const D3D_SHADER_MACRO defines[] = 
        {
            "EXAMPLE_DEFINE", "1",
            NULL, NULL
        };
        ID3DBlob* shaderBlob = nullptr;
        ID3DBlob* errorBlob = nullptr;
        HRESULT hr = D3DCompileFromFile( srcFile, defines, D3D_COMPILE_STANDARD_FILE_INCLUDE,
                                         entryPoint, profile,
                                         flags, 0, &shaderBlob, &errorBlob );
    ```

    

En el ejemplo de código siguiente se muestra cómo compilar varios sombreadores.

> [!Note]  
> Para este código de ejemplo, necesita el SDK de Windows 8.0 y el archivo d3dcompiler44.dll de la carpeta de arqueta \_ \_ D3D %PROGRAM FILE% \\ Windows Kits \\ 8.0 \\ Redist \\ D3D \\ &lt; en &gt; la ruta de acceso. Windows Las aplicaciones de la tienda admiten la compilación en tiempo de ejecución para el desarrollo, pero no para la implementación.

 


```C++
#define _WIN32_WINNT 0x600
#include <stdio.h>

#include <d3dcompiler.h>

#pragma comment(lib,"d3dcompiler.lib")

HRESULT CompileShader( _In_ LPCWSTR srcFile, _In_ LPCSTR entryPoint, _In_ LPCSTR profile, _Outptr_ ID3DBlob** blob )
{
    if ( !srcFile || !entryPoint || !profile || !blob )
       return E_INVALIDARG;

    *blob = nullptr;

    UINT flags = D3DCOMPILE_ENABLE_STRICTNESS;
#if defined( DEBUG ) || defined( _DEBUG )
    flags |= D3DCOMPILE_DEBUG;
#endif

    const D3D_SHADER_MACRO defines[] = 
    {
        "EXAMPLE_DEFINE", "1",
        NULL, NULL
    };

    ID3DBlob* shaderBlob = nullptr;
    ID3DBlob* errorBlob = nullptr;
    HRESULT hr = D3DCompileFromFile( srcFile, defines, D3D_COMPILE_STANDARD_FILE_INCLUDE,
                                     entryPoint, profile,
                                     flags, 0, &shaderBlob, &errorBlob );
    if ( FAILED(hr) )
    {
        if ( errorBlob )
        {
            OutputDebugStringA( (char*)errorBlob->GetBufferPointer() );
            errorBlob->Release();
        }

        if ( shaderBlob )
           shaderBlob->Release();

        return hr;
    }    

    *blob = shaderBlob;

    return hr;
}

int main()
{
    // Compile vertex shader shader
    ID3DBlob *vsBlob = nullptr;
    HRESULT hr = CompileShader( L"BasicHLSL11_VS.hlsl", "VSMain", "vs_4_0_level_9_1", &vsBlob );
    if ( FAILED(hr) )
    {
        printf("Failed compiling vertex shader %08X\n", hr );
        return -1;
    }

    // Compile pixel shader shader
    ID3DBlob *psBlob = nullptr;
    hr = CompileShader( L"BasicHLSL11_PS.hlsl", "PSMain", "ps_4_0_level_9_1", &psBlob );
    if ( FAILED(hr) )
    {
        vsBlob->Release();
        printf("Failed compiling pixel shader %08X\n", hr );
        return -1;
    }

    printf("Success\n");

    // Clean up
    vsBlob->Release();
    psBlob->Release();

    return 0;
}

```



En el ejemplo de código anterior se compilan los bloques de código del sombreador de píxeles y vértices en los archivos BASICHLSL11 \_ PS.hlsl y BasicHLSL11 \_ VS.hlsl. Este es el código de BasicHLSL11 \_ PS.hlsl:


```hlsl
//--------------------------------------------------------------------------------------
// File: BasicHLSL11_PS.hlsl
//
// The pixel shader file for the BasicHLSL11 sample.  
// 
// Copyright (c) Microsoft Corporation. All rights reserved.
//--------------------------------------------------------------------------------------

//--------------------------------------------------------------------------------------
// Globals
//--------------------------------------------------------------------------------------
cbuffer cbPerObject : register( b0 )
{
    float4        g_vObjectColor            : packoffset( c0 );
};

cbuffer cbPerFrame : register( b1 )
{
    float3        g_vLightDir                : packoffset( c0 );
    float        g_fAmbient                : packoffset( c0.w );
};

//--------------------------------------------------------------------------------------
// Textures and Samplers
//--------------------------------------------------------------------------------------
Texture2D    g_txDiffuse : register( t0 );
SamplerState g_samLinear : register( s0 );

//--------------------------------------------------------------------------------------
// Input / Output structures
//--------------------------------------------------------------------------------------
struct PS_INPUT
{
    float3 vNormal        : NORMAL;
    float2 vTexcoord    : TEXCOORD0;
};

//--------------------------------------------------------------------------------------
// Pixel Shader
//--------------------------------------------------------------------------------------
float4 PSMain( PS_INPUT Input ) : SV_TARGET
{
    float4 vDiffuse = g_txDiffuse.Sample( g_samLinear, Input.vTexcoord );
    
    float fLighting = saturate( dot( g_vLightDir, Input.vNormal ) );
    fLighting = max( fLighting, g_fAmbient );
    
    return vDiffuse * fLighting;
}
```



Este es el código de BasicHLSL11 \_ VS.hlsl:


```hlsl
//--------------------------------------------------------------------------------------
// File: BasicHLSL11_VS.hlsl
//
// The vertex shader file for the BasicHLSL11 sample.  
// 
// Copyright (c) Microsoft Corporation. All rights reserved.
//--------------------------------------------------------------------------------------

//--------------------------------------------------------------------------------------
// Globals
//--------------------------------------------------------------------------------------
cbuffer cbPerObject : register( b0 )
{
    matrix        g_mWorldViewProjection    : packoffset( c0 );
    matrix        g_mWorld                : packoffset( c4 );
};

//--------------------------------------------------------------------------------------
// Input / Output structures
//--------------------------------------------------------------------------------------
struct VS_INPUT
{
    float4 vPosition    : POSITION;
    float3 vNormal        : NORMAL;
    float2 vTexcoord    : TEXCOORD0;
};

struct VS_OUTPUT
{
    float3 vNormal        : NORMAL;
    float2 vTexcoord    : TEXCOORD0;
    float4 vPosition    : SV_POSITION;
};

//--------------------------------------------------------------------------------------
// Vertex Shader
//--------------------------------------------------------------------------------------
VS_OUTPUT VSMain( VS_INPUT Input )
{
    VS_OUTPUT Output;
    
    Output.vPosition = mul( Input.vPosition, g_mWorldViewProjection );
    Output.vNormal = mul( Input.vNormal, (float3x3)g_mWorld );
    Output.vTexcoord = Input.vTexcoord;
    
    return Output;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 
