---
title: Prototipos
description: Una firma de sombreador es una lista de los parámetros que son la entrada o la salida de una función de sombreador.
ms.assetid: c73a4f3e-e6fa-4e49-9ee8-4e200269dba7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 37906222ec674c2c1bb5e1cdfea1cb2de2e1df3d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104996796"
---
# <a name="signatures"></a>Prototipos

Una firma de sombreador es una lista de los parámetros que son la entrada o la salida de una función de sombreador. En Direct3D 10, las fases adyacentes comparten eficazmente una matriz de registros, donde el sombreador de salida (o la fase de canalización) escribe datos en ubicaciones específicas de la matriz de registro y el sombreador de entrada debe leer desde las mismas ubicaciones. La API usa firmas de sombreador para enlazar salidas de sombreador con entradas sin la sobrecarga de la resolución semántica.

En Direct3D 10, las firmas de entrada se generan a partir de una declaración de entrada de sombreador y la firma de salida se genera a partir de una declaración de salida de sombreador. Se dice que una firma de entrada es compatible con una firma de salida cuando la firma de salida es un subconjunto estricto (tipo de argumento y coincidencia de orden) de la firma de entrada. La manera más sencilla de lograrlo es vincular las entradas y salidas de sombreador correspondientes con el mismo tipo de estructura.

Este es un ejemplo de firmas compatibles.


```
// Vertex Shader Output Signature
Struct VSOut
{
  float4 Pos: SV_Position;
  float3 MyNormal: Normal;
  float2 MyTex : Texcoord0;
}

// Pixel Shader Input Signature
Struct PSInWorks
{
  float4 Pos: SV_Position;
  float3 MyNormal: Normal;
}
```



A continuación se muestra un ejemplo de firmas incompatibles; el orden de los parámetros en la signatura de entrada no coincide con el orden de la firma de salida.


```
// Vertex Shader Output Signature
Struct VSOut
{
  float4 Pos: SV_Position;
  float3 MyNormal: Normal;
  float2 MyTex : Texcoord0;
}

// Pixel Shader Input Signature
Struct PSInFails
{
  float3 MyNormal: Normal;
  float4 Pos: SV_Position;
}
```



PSInWorks es un subconjunto compatible de VSOut (las dos primeras entradas coinciden con el tipo y el orden con las dos primeras entradas en VSOut). Sin embargo, PSInFails es incompatible porque el orden no coincide con VSOut.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Funciones](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 




