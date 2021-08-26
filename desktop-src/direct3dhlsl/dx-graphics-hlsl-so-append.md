---
title: Append (objeto Stream-Output HLSL de DirectX)
description: Anexe los datos de geometry-shader-output a una secuencia existente.
ms.assetid: 7df51383-7fc7-4a6f-aaa2-6c929f0443a3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 956d4b2e37c4430e20fc4b75b2847c096c7832369d036f5224d8c36d86b7c66c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068175"
---
# <a name="append-directx-hlsl-stream-output-object"></a>Append (objeto Stream-Output HLSL de DirectX)

Anexe los datos de geometry-shader-output a una secuencia existente.

Append( *StreamDataType*);



 

## <a name="parameters"></a>Parámetros



| Elemento                                                                                                                             | Descripción                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="StreamDataType"></span><span id="streamdatatype"></span><span id="STREAMDATATYPE"></span>**StreamDataType**<br/> | Descripción de la entrada de datos. Esta descripción debe coincidir con el parámetro de plantilla stream-object denominado [DataType](dx-graphics-hlsl-so-type.md).<br/> |



 

## <a name="return-value"></a>Valor devuelto

None

## <a name="example"></a>Ejemplo

Este fragmento de código (del ejemplo [CubeMapGS)](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)muestra un ejemplo parcial de anexar primitivas de franja de triángulo a un objeto de salida de flujo.


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



## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | Sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objeto Stream-Output](dx-graphics-hlsl-so-type.md)
</dt> </dl>

 

 





