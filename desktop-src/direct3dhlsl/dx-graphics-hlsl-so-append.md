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
ms.openlocfilehash: 19d767f3c501cc42e21bbc44a196ba08cd6f1883
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974704"
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

Este fragmento de código (del ejemplo [CubeMapGS](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)) muestra un ejemplo parcial de anexar primitivas de franjas de triángulo a un objeto de salida de flujo.


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
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objeto Stream-Output](dx-graphics-hlsl-so-type.md)
</dt> </dl>

 

 





