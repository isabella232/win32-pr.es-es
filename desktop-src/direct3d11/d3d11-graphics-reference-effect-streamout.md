---
title: Sintaxis de Stream out
description: Un sombreador de geometría con Stream out se declara con una sintaxis determinada.
ms.assetid: 58cf6503-0dde-4c88-837d-ae0e0eda17d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 535ea78d1b2109e343f01800b3a3d5e1bf6efaba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104996764"
---
# <a name="stream-out-syntax"></a>Sintaxis de Stream out

Un sombreador de geometría con Stream out se declara con una sintaxis determinada. En este tema se describe la sintaxis de. En el tiempo de ejecución del efecto, esta sintaxis se convertirá en una llamada a [**ID3D11Device:: CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput).

## <a name="construct-syntax"></a>Sintaxis de construcción


```
[ StreamingShaderVar = ] ConstructGSWithSO( ShaderVar, "OutputDecl0" )
```





| Nombre                   | Descripción                                                                                                                                                                                                                |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **StreamingShaderVar** | Opcional. Cadena de ASCI que identifica de forma única el nombre de una variable de sombreador de geometría con transmisión por secuencias. Esto es opcional porque ConstructGSWithSO puede colocarse directamente en una llamada a SetGeometryShader o BindInterfaces. |
| **ShaderVar**          | Sombreador de geometría o variable de sombreador de vértices.                                                                                                                                                                               |
| **OutputDecl0**        | Una cadena que define qué salidas del sombreador en el flujo 0 se transmiten por secuencias. Vea a continuación la sintaxis de.                                                                                                                                 |



 

Esta es la sintaxis que se definió \_ en \_ los archivos FX 4 0. Tenga en cuenta que en los \_ \_ sombreadores GS 4 0 y vs \_ x, solo hay un flujo de datos. El sombreador resultante generará un flujo para la unidad de salida de flujo y la unidad de rasterizador.


```
[ StreamingShaderVar = ] ConstructGSWithSO( ShaderVar, "OutputDecl0", "OutputDecl1", "OutputDecl2", 
"OutputDecl3", RasterizedStream )
```





| Nombre                   | Descripción                                                                                                                                                                                                                |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **StreamingShaderVar** | Opcional. Cadena de ASCI que identifica de forma única el nombre de una variable de sombreador de geometría con transmisión por secuencias. Esto es opcional porque ConstructGSWithSO puede colocarse directamente en una llamada a SetGeometryShader o BindInterfaces. |
| **ShaderVar**          | Sombreador de geometría o variable de sombreador de vértices.                                                                                                                                                                               |
| **OutputDecl0**        | Una cadena que define qué salidas del sombreador en el flujo 0 se transmiten por secuencias. Vea a continuación la sintaxis de.                                                                                                                                 |
| **OutputDecl1**        | Una cadena que define qué salidas del sombreador en Stream 1 se transmiten por secuencias. Vea a continuación la sintaxis de.                                                                                                                                 |
| **OutputDecl2**        | Una cadena que define qué salidas del sombreador en Stream 2 se transmiten por secuencias. Vea a continuación la sintaxis de.                                                                                                                                 |
| **OutputDecl3**        | Una cadena que define qué salidas del sombreador en Stream 3 se transmiten por secuencias. Vea a continuación la sintaxis de.                                                                                                                                 |
| **RasterizedStream**   | Entero que especifica la secuencia que se enviará al rasterizador.                                                                                                                                                         |



 

Tenga en cuenta que los \_ \_ sombreadores GS 5 0 pueden definir hasta cuatro flujos de datos. El sombreador resultante generará una secuencia de salida para cada declaración de salida que no sea **null** y una secuencia la unidad de rasterizador.

## <a name="stream-out-declaration-syntax"></a>Sintaxis de la declaración out de Stream


```
" [ Buffer: ] Semantic[ SemanticIndex ] [ .Mask ]; [ ... ; ] ... [ ... ;]"
```





| Nombre              | Descripción                                                                                           |
|-------------------|-------------------------------------------------------------------------------------------------------|
| **Buffer**        | Opcional. Entero, 0 <= búfer < 4, que especifica a qué búfer de salida de flujo se va a pasar el valor. |
| **Semántica**      | Una cadena, junto con SemanticIndex, que especifica el valor que se va a generar.                                 |
| **SemanticIndex** | Opcional. Índice asociado a Semantic.                                                         |
| **Máscara**          | Opcional. Máscara de componente, que indica los componentes del valor que se van a mostrar.                       |



 

Hay una semántica especial, etiquetada como "$SKIP" que indica una semántica vacía, sin tocar la memoria correspondiente en el búfer de flujo de salida. La semántica $SKIP no puede tener un SemanticIndex, pero puede tener una máscara.

La declaración out completa de la secuencia puede ser **null**.

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

 

 




