---
title: Append (objeto de Stream-Output de datos HLSL de DirectX)
description: Anexe los datos de salida del sombreador de geometría a un flujo existente.
ms.assetid: 7df51383-7fc7-4a6f-aaa2-6c929f0443a3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 97ab88961b22529accb4402fc2bd095ede5275c1
ms.sourcegitcommit: 477b1efe7d9c2f91d5f2ac588a20edf348b1c734
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2019
ms.locfileid: "104358556"
---
# <a name="append-directx-hlsl-stream-output-object"></a>Append (objeto de Stream-Output de datos HLSL de DirectX)

Anexe los datos de salida del sombreador de geometría a un flujo existente.



|                            |
|----------------------------|
| Append ( *StreamDataType*); |



 

## <a name="parameters"></a>Parámetros



| Elemento                                                                                                                             | Descripción                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="StreamDataType"></span><span id="streamdatatype"></span><span id="STREAMDATATYPE"></span>**StreamDataType**<br/> | Una descripción de entrada de datos. Esta descripción debe coincidir con el parámetro de plantilla de objeto de secuencia denominado [DataType](dx-graphics-hlsl-so-type.md).<br/> |



 

## <a name="return-value"></a>Valor devuelto

None

## <a name="example"></a>Ejemplo

Este fragmento de código (del [ejemplo CubeMapGS](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)) muestra un ejemplo parcial de cómo anexar los primitivos de franja de triángulo a un objeto de salida de flujo.


```
[maxvertexcount(18)]
void GS_CubeMap( triangle GS_CUBEMAP_IN input[3], 
                 inout TriangleStream<PS_CUBEMAP_IN> CubeMapStream )
{
    for( int f = 0; f < 6; ++f )
    {
        // Compute screen coordinates
        PS_CUBEMAP_IN output;
        output.RTIndex = f;
        for( int v = 0; v < 3; v++ )
        {
            output.Pos = mul( input[v].Pos, g_mViewCM[f] );
            output.Pos = mul( output.Pos, mProj );
            output.Tex = input[v].Tex;
            CubeMapStream.Append( output );
        }
        CubeMapStream.RestartStrip();
    }
}
```



## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Stream: salida de objeto](dx-graphics-hlsl-so-type.md)
</dt> </dl>

 

 





