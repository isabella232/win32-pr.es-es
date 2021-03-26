---
title: Cambios de código de bytes en SM 5.1
description: SM 5.1 cambia el modo en que se declaran y se hace referencia a los registros de recursos en las instrucciones.
ms.assetid: ABECF705-67B8-4419-8D18-74B43B9DC3AF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6d66db788b0012a1c3221e37d4c2dd4e41566c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357800"
---
# <a name="bytecode-changes-in-sm51"></a>Cambios de código de bytes en SM 5.1

SM 5.1 cambia el modo en que se declaran y se hace referencia a los registros de recursos en las instrucciones.

SM 5.1 pasa a declarar una "variable" de registro, de forma similar a como se hace para los registros de memoria compartida del grupo, que se muestra en el ejemplo siguiente:

``` syntax
Texture2D<float4> tex0          : register(t5,  space0);
Texture2D<float4> tex1[][5][3]  : register(t10, space0);
Texture2D<float4> tex2[8]       : register(t0,  space1);
SamplerState samp0              : register(s5, space0);

float4 main(float4 coord : COORD) : SV_TARGET
{
    float4 r = coord;
    r += tex0.Sample(samp0, r.xy);
    r += tex2[r.x].Sample(samp0, r.xy);
    r += tex1[r.x][r.y][r.z].Sample(samp0, r.xy);
    return r;
}
```

A continuación se muestra el desensamblado de este ejemplo:

``` syntax
// Resource Bindings:
//
// Name                                 Type  Format         Dim Space Slot  Elements
// ------------------------------ ---------- ------- ----------- ----- ---- ---------
// samp0                             sampler      NA          NA     0    5         1
// tex0                              texture  float4          2d     0    5         1
// tex1[0][5][3]                     texture  float4          2d     0   10 unbounded
// tex2[8]                           texture  float4          2d     1    0         8
//
//
//
// Input signature:
//
// Name                 Index   Mask Register SysValue  Format   Used
// -------------------- ----- ------ -------- -------- ------- ------
// COORD                    0   xyzw        0     NONE   float   xyzw
//
//
// Output signature:
//
// Name                 Index   Mask Register SysValue  Format   Used
// -------------------- ----- ------ -------- -------- ------- ------
// SV_TARGET                0   xyzw        0   TARGET   float   xyzw
//
ps_5_1
dcl_globalFlags refactoringAllowed
dcl_sampler s0[5:5], mode_default, space=0
dcl_resource_texture2d (float,float,float,float) t0[5:5], space=0
dcl_resource_texture2d (float,float,float,float) t1[10:*], space=0
dcl_resource_texture2d (float,float,float,float) t2[0:7], space=1
dcl_input_ps linear v0.xyzw
dcl_output o0.xyzw
dcl_temps 2
sample r0.xyzw, v0.xyxx, t0[0].xyzw, s0[5]
add r0.xyzw, r0.xyzw, v0.xyzw
ftou r1.x, r0.x
sample r1.xyzw, r0.xyxx, t2[r1.x + 0].xyzw, s0[5]
add r0.xyzw, r0.xyzw, r1.xyzw
ftou r1.xyz, r0.zyxz
imul null, r1.yz, r1.zzyz, l(0, 15, 3, 0)
iadd r1.y, r1.z, r1.y
iadd r1.x, r1.x, r1.y
sample r1.xyzw, r0.xyxx, t1[r1.x + 10].xyzw, s0[5]
add o0.xyzw, r0.xyzw, r1.xyzw
ret
// Approximately 12 instruction slots used
```

Ahora cada intervalo de recursos del sombreador tiene un identificador (un nombre) en el código de bytes del sombreador. Por ejemplo, la matriz de texturas de Tex1 se convierte en ' t 1 ' en el código de bytes del sombreador. Asignar identificadores únicos a cada intervalo de recursos permite dos cosas:

-   Identifique de forma inequívoca qué intervalo de recursos (consulte DCL \_ Resource \_ texture2d) se está indizando en una instrucción (vea la instrucción de ejemplo).
-   Adjunte un conjunto de atributos a la declaración, por ejemplo, tipo de elemento, tamaño de intervalo, modo de operación de trama, etc.

Tenga en cuenta que el identificador del intervalo no está relacionado con la declaración de límite inferior de HLSL.

El orden de los enlaces de recursos de reflexión y las instrucciones de declaración del sombreador es el mismo para ayudar a identificar la correspondencia entre las variables de HLSL y los ID. de código de bytes.

Cada instrucción de declaración en SM 5.1 usa un operando 3D para definir: ID. de intervalo, límites inferior y superior. Se emite un token adicional para especificar el espacio de registro. También se pueden emitir otros tokens para transmitir propiedades adicionales del intervalo; por ejemplo, CBuffer o la instrucción de declaración de búfer estructurado emite el tamaño de la CBuffer o la estructura. Los detalles exactos de la codificación se pueden encontrar en d3d12TokenizedProgramFormat. h y D3D10ShaderBinary:: CShaderCodeParser.

Las instrucciones de SM 5.1 no emitirán información adicional del operando de recursos como parte de la instrucción (como en SM 5.0). Esta información se mueve ahora a las instrucciones de declaración. En SM 5.0, instrucciones que indexan los recursos de recursos necesarios para describirse en tokens de código de operación extendidos, ya que la indización ofuscaba la asociación con la declaración. En SM 5.1, cada identificador (por ejemplo, ' t 1 ') está asociado de forma no ambigua a una única declaración que describe la información de recursos necesaria. Por lo tanto, los tokens de código de operación extendidos usados en las instrucciones para describir la información de recursos ya no se emiten.

En las instrucciones que no son de declaración, un operando de recursos para muestreadores, SRVs y UAVs es un operando 2D. El primer índice es una constante literal que especifica el identificador del intervalo. El segundo índice representa el valor de linealización del índice. El valor se calcula en relación con el principio del espacio de registro correspondiente (no con respecto al principio del intervalo lógico) para correlacionar mejor con la firma raíz y reducir la carga del compilador de controladores para ajustar el índice.

Un operando de recurso para CBVs es un operando 3D: el identificador literal del intervalo, el índice del CBuffer, el desplazamiento en la instancia concreta de CBuffer.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Características del modelo de sombreador de HLSL 5,1 para Direct3D 12](hlsl-shader-model-5-1-features-for-direct3d-12.md)
</dt> <dt>

[Modelo de sombreador 5,1](shader-model-5-1.md)
</dt> </dl>

 

 




