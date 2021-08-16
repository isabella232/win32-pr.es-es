---
title: Cambios en el código de bytes en SM5.1
description: SM5.1 cambia la forma en que se declaran los registros de recursos y se hace referencia a ellos en las instrucciones.
ms.assetid: ABECF705-67B8-4419-8D18-74B43B9DC3AF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e93d7d8533bac3750e743166a9d64b687fc06f0fbf21931d44e7d83d462cf15a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118794563"
---
# <a name="bytecode-changes-in-sm51"></a>Cambios en el código de bytes en SM5.1

SM5.1 cambia la forma en que se declaran los registros de recursos y se hace referencia a ellos en las instrucciones.

SM5.1 avanza hacia la declaración de una "variable" de registro, similar a cómo se hace para los registros de memoria compartida de grupo, como se muestra en el ejemplo siguiente:

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

El desensamblado de este ejemplo es el siguiente:

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

Ahora, cada intervalo de recursos del sombreador tiene un identificador (un nombre) en el código de bytes del sombreador. Por ejemplo, la matriz de texturas tex1 se convierte en "t1" en el código de bytes del sombreador. La asignación de identificadores únicos a cada intervalo de recursos permite dos cosas:

-   Identifique de forma inequívoca qué intervalo de recursos (consulte dcl resource texture2d) que se indexa en una instrucción \_ \_ (consulte la instrucción de ejemplo).
-   Adjunte un conjunto de atributos a la declaración, por ejemplo, tipo de elemento, tamaño de paso, modo de operación de trama, etc.

Tenga en cuenta que el identificador del intervalo no está relacionado con la declaración de límite inferior HLSL.

El orden de los enlaces de recursos de reflexión y las instrucciones de declaración del sombreador es el mismo para ayudar a identificar la correspondencia entre variables HLSL e identificadores de código de bytes.

Cada instrucción de declaración de SM5.1 usa un operando 3D para definir: id. de intervalo, límites inferiores y superiores. Se emite un token adicional para especificar el espacio de registro. También se pueden emitir otros tokens para transmitir propiedades adicionales del intervalo, por ejemplo, la instrucción de declaración de búfer estructurado o de cbuffer emite el tamaño del cbuffer o la estructura. Los detalles exactos de la codificación se pueden encontrar en d3d12TokenizedProgramFormat.h y D3D10ShaderBinary::CShaderCodeParser.

Las instrucciones SM5.1 no emitirán información adicional sobre operandos de recursos como parte de la instrucción (como en SM5.0). Esta información se mueve ahora a las instrucciones de declaración. En SM5.0, las instrucciones de indexación de recursos requerían que los atributos de recursos se describieron en tokens de código de operación extendidos, ya que la indexación ofuscaba la asociación a la declaración. En SM5.1, cada identificador (como "t1") está asociado inequívocamente a una única declaración que describe la información de recursos necesaria. Por lo tanto, ya no se emiten los tokens de código de operación extendidos que se usan en las instrucciones para describir la información de recursos.

En las instrucciones que no son de declaración, un operando de recurso para muestreadores, SRV y UAV es un operando 2D. El primer índice es una constante literal que especifica el identificador de intervalo. El segundo índice representa el valor linealizado del índice. El valor se calcula con respecto al principio del espacio de registro correspondiente (no relativo al principio del intervalo lógico) para correlacionar mejor con la firma raíz y reducir la carga del compilador del controlador de ajustar el índice.

Un operando de recurso para CBV es un operando 3D: identificador literal del intervalo, índice del búfer de búfer, desplazamiento en la instancia concreta de cbuffer.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Características del modelo de sombreador HLSL 5.1 para Direct3D 12](hlsl-shader-model-5-1-features-for-direct3d-12.md)
</dt> <dt>

[Modelo de sombreador 5.1](shader-model-5-1.md)
</dt> </dl>

 

 




