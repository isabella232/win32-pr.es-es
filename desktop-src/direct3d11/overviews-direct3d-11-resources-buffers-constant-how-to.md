---
title: Cómo crear un búfer de constantes
description: En este tema se muestra cómo inicializar un búfer de constantes como preparación para la representación.
ms.assetid: 78694ac2-e850-402d-8c99-6afb0bd5d660
keywords:
- búfer de constantes, crear
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1abb6718ad223ff389aa0b7ebf10ad1ec8bacd71
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793323"
---
# <a name="how-to-create-a-constant-buffer"></a>Cómo: crear un búfer de constantes

Los [búferes de constantes](overviews-direct3d-11-resources-buffers-intro.md) contienen datos de constantes de sombreador. En este tema se muestra cómo inicializar un [búfer de constantes](overviews-direct3d-11-resources-buffers-intro.md) como preparación para la representación.

**Para inicializar un búfer de constantes**

1.  Defina una estructura que describa los datos constantes del sombreador de vértices.
2.  Asigne memoria para la estructura que definió en el paso uno. Rellene este búfer con datos constantes del sombreador de vértices. Puede usar **malloc** o **New** para asignar la memoria, o puede asignar memoria para la estructura de la pila.
3.  Cree una descripción de búfer rellenando una estructura [**\_ \_ DESC de búfer D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) . Pase la \_ \_ marca de búfer constante de enlace D3D11 \_ al miembro **BindFlags** y pase el tamaño de la estructura de la descripción del búfer de constantes en bytes al miembro **ByteWidth** .

    > [!Note]  
    > La \_ marca de \_ búfer constante de enlace D3D11 no se \_ puede combinar con otras marcas.

     

4.  Cree una descripción de los datos de subrecurso rellenando una estructura de [**\_ \_ datos de subrecurso D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) . El miembro **pSysMem** de la estructura de **\_ \_ datos del subrecurso D3D11** debe apuntar directamente a los datos constantes del sombreador de vértices que creó en el paso dos.
5.  Llame a [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) mientras pasa la estructura de [**\_ \_ DESC del búfer D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) , la estructura de [**\_ \_ datos del subrecurso D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) y la dirección de un puntero a la interfaz [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) que se va a inicializar.

En estos ejemplos de código se muestra cómo crear un búfer de constantes.

En este ejemplo se da por supuesto que **g \_ pd3dDevice** es un objeto [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) válido y que **g \_ pd3dContext** es un objeto [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) válido.


```C++
ID3D11Buffer*   g_pConstantBuffer11 = NULL;

// Define the constant data used to communicate with shaders.
struct VS_CONSTANT_BUFFER
{
    XMFLOAT4X4 mWorldViewProj;                              
    XMFLOAT4 vSomeVectorThatMayBeNeededByASpecificShader;
    float fSomeFloatThatMayBeNeededByASpecificShader;
    float fTime;                                            
    float fSomeFloatThatMayBeNeededByASpecificShader2;
    float fSomeFloatThatMayBeNeededByASpecificShader3;
} VS_CONSTANT_BUFFER;

// Supply the vertex shader constant data.
VS_CONSTANT_BUFFER VsConstData;
VsConstData.mWorldViewProj = {...};
VsConstData.vSomeVectorThatMayBeNeededByASpecificShader = XMFLOAT4(1,2,3,4);
VsConstData.fSomeFloatThatMayBeNeededByASpecificShader = 3.0f;
VsConstData.fTime = 1.0f;
VsConstData.fSomeFloatThatMayBeNeededByASpecificShader2 = 2.0f;
VsConstData.fSomeFloatThatMayBeNeededByASpecificShader3 = 4.0f;

// Fill in a buffer description.
D3D11_BUFFER_DESC cbDesc;
cbDesc.ByteWidth = sizeof( VS_CONSTANT_BUFFER );
cbDesc.Usage = D3D11_USAGE_DYNAMIC;
cbDesc.BindFlags = D3D11_BIND_CONSTANT_BUFFER;
cbDesc.CPUAccessFlags = D3D11_CPU_ACCESS_WRITE;
cbDesc.MiscFlags = 0;
cbDesc.StructureByteStride = 0;

// Fill in the subresource data.
D3D11_SUBRESOURCE_DATA InitData;
InitData.pSysMem = &VsConstData;
InitData.SysMemPitch = 0;
InitData.SysMemSlicePitch = 0;

// Create the buffer.
hr = g_pd3dDevice->CreateBuffer( &cbDesc, &InitData, 
                                 &g_pConstantBuffer11 );

if( FAILED( hr ) )
   return hr;

// Set the buffer.
g_pd3dContext->VSSetConstantBuffers( 0, 1, &g_pConstantBuffer11 );
    
```



En este ejemplo se muestra la definición de CBuffer de HLSL asociada.

``` syntax
cbuffer VS_CONSTANT_BUFFER : register(b0)
{
    matrix mWorldViewProj;
    float4  vSomeVectorThatMayBeNeededByASpecificShader;
    float fSomeFloatThatMayBeNeededByASpecificShader;
    float fTime;
    float fSomeFloatThatMayBeNeededByASpecificShader2;
    float fSomeFloatThatMayBeNeededByASpecificShader3;
};
```

> [!Note]  
> Asegúrese de que coincide con el \_ diseño \_ de memoria del búfer de vs Constant en C++ con el diseño de HLSL. Para obtener información sobre cómo HLSL controla el diseño en memoria, consulte [reglas de empaquetado para variables constantes](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-packing-rules).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Búferes](overviews-direct3d-11-resources-buffers.md)
</dt> <dt>

[Cómo usar Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 