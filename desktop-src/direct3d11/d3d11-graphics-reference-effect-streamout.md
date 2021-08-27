---
title: Sintaxis de stream-out
description: Un sombreador de geometría con salida de flujo se declara con una sintaxis determinada.
ms.assetid: 58cf6503-0dde-4c88-837d-ae0e0eda17d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43980d79d9c338a965d7ab2f2ceb008411d9713dec935d953dd5a1854c40465b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096395"
---
# <a name="stream-out-syntax"></a>Sintaxis de stream-out

Un sombreador de geometría con salida de flujo se declara con una sintaxis determinada. En este tema se describe la sintaxis. En el tiempo de ejecución del efecto, esta sintaxis se convertirá en una llamada a [**ID3D11Device::CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput).

## <a name="construct-syntax"></a>Sintaxis de construcción


```
[ StreamingShaderVar = ] ConstructGSWithSO( ShaderVar, "OutputDecl0" )
```





| Nombre                   | Descripción                                                                                                                                                                                                                |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **StreamingShaderVar** | Opcional. Cadena ASCI que identifica de forma única el nombre de una variable de sombreador de geometría con secuencia. Esto es opcional porque ConstructGSWithSO se puede colocar directamente en una llamada a SetGeometryShader o BindInterfaces. |
| **ShaderVar**          | Un sombreador de geometría o una variable de sombreador de vértices.                                                                                                                                                                               |
| **OutputDecl0**        | Cadena que define qué salidas de sombreador del flujo 0 se transmiten. Consulte a continuación la sintaxis.                                                                                                                                 |



 

Esta es la sintaxis que se definió en los archivos fx \_ 4 \_ 0. Tenga en cuenta que en los sombreadores gs \_ \_ 4 0 y \_ x, solo hay un flujo de datos. El sombreador resultante dará como resultado una secuencia a la unidad de salida de secuencia y a la unidad rasterizadora.


```
[ StreamingShaderVar = ] ConstructGSWithSO( ShaderVar, "OutputDecl0", "OutputDecl1", "OutputDecl2", 
"OutputDecl3", RasterizedStream )
```





| Nombre                   | Descripción                                                                                                                                                                                                                |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **StreamingShaderVar** | Opcional. Cadena ASCI que identifica de forma única el nombre de una variable de sombreador de geometría con secuencia. Esto es opcional porque ConstructGSWithSO se puede colocar directamente en una llamada a SetGeometryShader o BindInterfaces. |
| **ShaderVar**          | Un sombreador de geometría o una variable de sombreador de vértices.                                                                                                                                                                               |
| **OutputDecl0**        | Cadena que define qué salidas de sombreador del flujo 0 se transmiten. Consulte a continuación la sintaxis.                                                                                                                                 |
| **OutputDecl1**        | Cadena que define qué salidas de sombreador del flujo 1 se transmiten. Consulte a continuación la sintaxis.                                                                                                                                 |
| **OutputDecl2**        | Cadena que define qué salidas de sombreador del flujo 2 se transmiten. Consulte a continuación la sintaxis.                                                                                                                                 |
| **OutputDecl3**        | Cadena que define qué salidas de sombreador del flujo 3 se transmiten. Consulte a continuación la sintaxis.                                                                                                                                 |
| **RasterizedStream**   | Entero que especifica qué secuencia se enviará al rasterizador.                                                                                                                                                         |



 

Tenga en cuenta que los \_ sombreadores \_ gs 5 0 pueden definir hasta cuatro flujos de datos. El sombreador resultante dará como resultado una secuencia a la unidad de salida de secuencia para cada declaración de salida que no sea **NULL** y una secuencia la unidad rasterizadora.

## <a name="stream-out-declaration-syntax"></a>Sintaxis de declaración de stream-out


```
" [ Buffer: ] Semantic[ SemanticIndex ] [ .Mask ]; [ ... ; ] ... [ ... ;]"
```





| Nombre              | Descripción                                                                                           |
|-------------------|-------------------------------------------------------------------------------------------------------|
| **Buffer**        | Opcional. Un entero, 0 <= Buffer < 4, que especifica a qué búfer de secuencias se va a ir el valor. |
| **Semántica**      | Cadena, junto con SemanticIndex, que especifica el valor que se va a generar.                                 |
| **SemanticIndex** | Opcional. Índice asociado a Semantic.                                                         |
| **Máscara**          | Opcional. Máscara de componente, que indica qué componentes del valor se va a generar.                       |



 

Hay una semántica especial, etiquetada como "$SKIP", que indica una semántica vacía, lo que deja intacta la memoria correspondiente en el búfer de salida de secuencia. La $SKIP semántica no puede tener semanticIndex, pero puede tener una máscara.

Toda la declaración de stream out puede ser **NULL.**

## <a name="example"></a>Ejemplo


```
struct GSOutput
{
int4 Pos : Position;
int4 Color : Color;
int4 Texcoord : Texcoord;
};

[maxvertexcount(1)]
void gsBase (inout PointStream<GSOutput> OutputStream, inout PointStream<GSOutput> OutputStream1)
{
GSOutput output;
output.Pos = int4(1,2,3,4);
output.Color = int4(5,6,7,8);
output.Texcoord = int4(9,10,11,12);
OutputStream.Append(output);

output.Pos = int4(1,2,3,4);
    output.Color = int4(5,6,7,8);
output.Texcoord = int4(9,10,11,12);
OutputStream1.Append(output);
};


GeometryShader pGSComp = CompileShader(gs_5_0, gsBase());
GeometryShader pGSwSO = ConstructGSWithSO(pGSComp, "0:Position.xy; 1:Position.zw; 2:Color.xy", 
                                                   "3:Texcoord.xyzw; 3:$SKIP.x;", NULL, NULL, 1);

// The following two passes perform the same operation
technique11 SOPoints
{
    pass 
    {
        SetGeometryShader(ConstructGSWithSO(pGSComp, "0:Position.xy; 1:Position.zw; 2:Color.xy", 
                                                     "3:Texcoord.xyzw; 3:$SKIP.x;", NULL, NULL, 1));
    }
    pass 
    {
        SetGeometryShader(pGSwSO);
    }
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Efectos (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 




