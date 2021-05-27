---
title: Enlace de recursos en HLSL
description: En este tema se describen algunas características específicas del uso del modelo de sombreador hlsl (lenguaje de sombreador de alto nivel) 5.1 con Direct3D 12.
ms.assetid: 3CD4BDAD-8AE3-4DE0-B3F8-9C9F9E83BBE9
ms.localizationpriority: high
ms.topic: article
ms.date: 08/27/2019
ms.openlocfilehash: 711ccdee71ff916445be68d03b84b7621aa04cf3
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550390"
---
# <a name="resource-binding-in-hlsl"></a>Enlace de recursos en HLSL

En este tema se describen algunas características específicas del uso del modelo de sombreador hlsl (lenguaje de sombreador de alto nivel) [5.1](/windows/desktop/direct3dhlsl/shader-model-5-1) con Direct3D 12. Todo el hardware de Direct3D 12 admite el modelo de sombreador 5.1, por lo que la compatibilidad con este modelo no depende del nivel de característica de hardware.

## <a name="resource-types-and-arrays"></a>Tipos de recursos y matrices

La sintaxis de recursos del modelo de sombreador 5 (SM5.0) usa la palabra clave para retransmitir información importante sobre el recurso `register` al compilador HLSL. Por ejemplo, la siguiente instrucción declara una matriz de cuatro texturas enlazadas en las ranuras t3, t4, t5 y t6. t3 es la única ranura de registro que aparece en la instrucción , siendo simplemente la primera de la matriz de cuatro.

``` syntax
Texture2D<float4> tex1[4] : register(t3)
```

La sintaxis de recursos del Modelo de sombreador 5.1 (SM5.1) en HLSL se basa en la sintaxis de recursos de registro existente, para permitir una porción más sencilla. Los recursos de Direct3D 12 en HLSL están enlazados a registros virtuales dentro de espacios de registro lógicos:

-   t: para vistas de recursos de sombreador (SRV)
-   s: para muestreadores
-   u: para vistas de acceso no ordenado (UAV)
-   b: para vistas de búfer constante (CBV)

La firma raíz que hace referencia al sombreador debe ser compatible con las ranuras de registro declaradas. Por ejemplo, la siguiente parte de una firma raíz sería compatible con el uso de ranuras de textura t3 a t6, ya que describe una tabla de descriptores con ranuras de t0 a t98.

``` syntax
DescriptorTable( CBV(b1), SRV(t0,numDescriptors=99), CBV(b2) )
```

Una declaración de recursos puede ser escalar, matriz 1D o matriz multidimensional:

``` syntax
Texture2D<float4> tex1 : register(t3,  space0)
Texture2D<float4> tex2[4] : register(t10)
Texture2D<float4> tex3[7][5][3] : register(t20, space1)
```

SM5.1 usa los mismos tipos de recursos y tipos de elemento que SM5.0. Los límites de declaración SM5.1 son más flexibles y solo están restringidos por los límites de tiempo de ejecución o hardware. La `space` palabra clave especifica a qué espacio de registro lógico está enlazada la variable declarada. Si se omite la palabra clave , el índice de espacio predeterminado de 0 se asigna implícitamente al intervalo (por lo que el intervalo anterior `space` `tex2` reside en `space0` ). `register(t3,  space0)` nunca entra en conflicto con `register(t3,  space1)` , ni con ninguna matriz en otro espacio que pueda incluir t3.

Un recurso de matriz puede tener un tamaño sin enlazar, que se declara especificando que la primera dimensión esté vacía, o 0:

``` syntax
Texture2D<float4> tex1[] : register(t0)
```

La tabla de descriptores correspondiente podría ser:

``` syntax
DescriptorTable( CBV(b1), UAV(u0, numDescriptors = 4), SRV(t0, numDescriptors=unbounded)
```

Una matriz sin enlazar en HLSL coincide con un número fijo establecido con en la tabla de descriptores y un tamaño fijo en hlsl coincide con una declaración sin enlazar en la tabla `numDescriptors` de descriptores.

Se permiten matrices multidimensionales, incluidas las de un tamaño sin enlazar. Estas matrices multidimensionales se aplana en el espacio de registro.

``` syntax
Texture2D<float4> tex2[3000][10] : register(t0, space0); // t0-t29999 in space0
Texture2D<float4> tex3[0][5][3] : register(t5, space1)
```

No se permite la asignación de alias de intervalos de recursos. En otras palabras, para cada tipo de recurso (t, s, u, b), los intervalos de registro declarados no deben superponerse. Esto también incluye intervalos sin enlazar. Los intervalos declarados en distintos espacios de registro nunca se superponen. Tenga en cuenta que unbounded (arriba) reside en , mientras que unbounded reside en , de forma que no `tex2` `space0` se `tex3` `space1` superponen.

El acceso a los recursos que se han declarado como matrices es tan sencillo como indexarlos.

``` syntax
Texture2D<float4> tex1[400] : register(t3);
sampler samp[7] : register(s0);
tex1[myMaterialID].Sample(samp[samplerID], texCoords);
```

Hay una restricción predeterminada importante en el uso de los índices ( y en el código anterior) en que no pueden variar dentro de `myMaterialID` `samplerID` una [ola](../direct3dhlsl/hlsl-shader-model-6-0-features-for-direct3d-12.md#terminology). Incluso el cambio del índice en función de los recuentos de creación de instancias varía.

Si es necesario variar el índice, especifique el `NonUniformResourceIndex` calificador en el índice, por ejemplo:

``` syntax
tex1[NonUniformResourceIndex(myMaterialID)].Sample(samp[NonUniformResourceIndex(samplerID)], texCoords);
```

En algún hardware, el uso de este calificador genera código adicional para aplicar la corrección (incluidos los subprocesos), pero con un costo de rendimiento menor. Si se cambia un índice sin este calificador y dentro de un draw/dispatch, los resultados no están definidos.

## <a name="descriptor-arrays-and-texture-arrays"></a>Matrices de descriptores y matrices de textura

Las matrices de texturas están disponibles desde DirectX 10. Las matrices de textura requieren un descriptor, pero todos los segmentos de matriz deben compartir el mismo formato, ancho, alto y recuento de mip. Además, la matriz debe ocupar un intervalo contiguo en el espacio de direcciones virtuales. En el código siguiente se muestra un ejemplo de acceso a una matriz de textura desde un sombreador.

``` syntax
Texture2DArray<float4> myTex2DArray : register(t0); // t0
float3 myCoord(1.0f,1.4f,2.2f); // 2.2f is array index (rounded to int)
color = myTex2DArray.Sample(mySampler, myCoord);
```

En una matriz de texturas, el índice puede variar libremente, sin necesidad de calificadores como `NonUniformResourceIndex` .

La matriz de descriptores equivalente sería:

``` syntax
Texture2D<float4> myArrayOfTex2D[] : register(t0); // t0+
float2 myCoord(1.0f, 1.4f);
color = myArrayOfTex2D[2].Sample(mySampler,myCoord); // 2 is index
```

Tenga en cuenta que el uso extraño de un elemento float para el índice de la matriz se reemplaza por `myArrayOfTex2D[2]` . Además, las matrices de descriptores ofrecen más flexibilidad con las dimensiones. El tipo, en este ejemplo, no puede variar, pero el formato, el ancho, el alto y el recuento de mip pueden variar `Texture2D` con cada descriptor.

Es legítimo tener una matriz de descriptores de matrices de textura:

``` syntax
Texture2DArray<float4> myArrayOfTex2DArrays[2] : register(t0);
```

No es legítimo declarar una matriz de estructuras, cada estructura que contiene descriptores, por ejemplo, no se admite el código siguiente.

``` syntax
struct myStruct {
    Texture2D                    a; 
    Texture2D                    b;
    ConstantBuffer<myConstants>  c;
};
myStruct foo[10000] : register(....);
```

Esto habría permitido el diseño de memoria **abcabcabc...**, pero es una limitación del lenguaje y no se admite. Un método admitido para hacerlo sería el siguiente, aunque el diseño de memoria en este caso es **aaa... Bbb... y...**.

``` syntax
Texture2D                     a[10000] : register(t0);
Texture2D                     b[10000] : register(t10000);
ConstantBuffer<myConstants>   c[10000] : register(b0);
```

Para lograr el diseño de memoria **abcabcabc...,** use una tabla de descriptores sin usar la `myStruct` estructura .

## <a name="resource-aliasing"></a>Alias de recursos

Los intervalos de recursos especificados en los sombreadores HLSL son intervalos lógicos. Se enlazan a intervalos de montón concretos en tiempo de ejecución mediante el mecanismo de firma raíz. Normalmente, un intervalo lógico se asigna a un intervalo de montón que no se superpone con otros intervalos del montón. Sin embargo, el mecanismo de firma raíz permite crear alias (superponerse) intervalos de montones de tipos compatibles. Por ejemplo, los intervalos y del ejemplo anterior se pueden asignar al mismo intervalo de montón (o superpuesto), lo que tiene el efecto de crear alias de texturas en el programa `tex2` `tex3` HLSL. Si se desea este tipo de alias, el sombreador debe compilarse con la opción DE ALIAS MAY SHADER RESOURCES (RECURSOS DE SOMBREADOR) D3D10, que se establece mediante la opción \_ \_ de alias \_ \_ */res \_ may \_ para* la herramienta [Effect-Compiler](../direct3dtools/fxc.md) Tool (FXC). La opción hace que el compilador produzca código correcto al impedir ciertas optimizaciones de carga y almacenamiento bajo la suposición de que los recursos pueden crear alias.

## <a name="divergence-and-derivatives"></a>Diferencias y derivados

SM5.1 no impone limitaciones en el índice de recursos; Es decir, el índice idx puede ser una constante literal, una ` tex2[idx].Sample(…)` constante cbuffer o un valor interpolado. Aunque el modelo de programación proporciona una flexibilidad tan grande, hay problemas que debe tener en cuenta:

-   Si el índice difiere en un cuadrándice, es posible que las cantidades derivadas y derivadas calculadas por hardware, como LOD, no se definan. El compilador HLSL hace todo lo posible para emitir una advertencia en este caso, pero no impedirá que se compila un sombreador. Este comportamiento es similar a la computación de derivados en un flujo de control divergente.
-   Si el índice de recursos es divergente, el rendimiento se reduce en comparación con el caso de un índice uniforme, ya que el hardware necesita realizar operaciones en varios recursos. Los índices de recursos que pueden ser divergentes deben marcarse con la `NonUniformResourceIndex` función en código HLSL. De lo contrario, los resultados no están definidos.

## <a name="uavs-in-pixel-shaders"></a>UAV en sombreadores de píxeles

SM5.1 no impone restricciones en los intervalos UAV en sombreadores de píxeles, como era el caso de SM5.0.

## <a name="constant-buffers"></a>Búferes constantes

La sintaxis de los búferes constantes (cbuffer) de SM5.1 ha cambiado de SM5.0 para permitir a los desarrolladores indexar búferes constantes. Para habilitar búferes constantes indexables, SM5.1 presenta la `ConstantBuffer` construcción "template":

``` syntax
struct Foo
{
    float4 a;
    int2 b;
};
ConstantBuffer<Foo> myCB1[2][3] : register(b2, space1);
ConstantBuffer<Foo> myCB2 : register(b0, space1);
```

El código anterior declara una variable de búfer constante de tipo y tamaño 6, y una variable de búfer `myCB1` `Foo` constante `myCB2` escalar. Ahora se puede indexar una variable de búfer constante en el sombreador como:

``` syntax
myCB1[i][j].a.xyzw
myCB2.b.yy
```

Los campos "a" y "b" no se convierten en variables globales, sino que deben tratarse como campos. Por compatibilidad con versiones anteriores, SM5.1 admite el concepto anterior de cbuffer para los búferes escalares. La siguiente instrucción hace que las variables globales "a" y "b" de solo lectura, como en SM5.0. Sin embargo, este tipo de cbuffer de estilo antiguo no puede ser indexable.

``` syntax
cbuffer : register(b1)
{
    float4 a;
    int2 b;
};
```

Actualmente, el compilador del sombreador solo admite `ConstantBuffer` la plantilla para estructuras definidas por el usuario.

Por motivos de compatibilidad, el compilador HLSL puede asignar automáticamente registros de recursos para los intervalos declarados en `space0` . Si se omite "space" en la cláusula register, se usa el `space0` valor predeterminado. El compilador usa la heurística de primer ajuste para asignar los registros. La asignación se puede recuperar a través de la API de reflexión, que se ha ampliado para agregar el campo *Espacio* para el espacio, mientras que el campo *BindPoint* indica el límite inferior del intervalo de registro de recursos.

## <a name="bytecode-changes-in-sm51"></a>Cambios en el código de bytes en SM5.1

SM5.1 cambia la forma en que se declaran los registros de recursos y se hace referencia a ellos en las instrucciones. La sintaxis implica declarar una "variable" de registro, de forma similar a como se hace para los registros de memoria compartida de grupo:

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

Esto se desensamblará para:

``` syntax
// Resource Bindings:
//
// Name                                 Type  Format         Dim    ID   HLSL Bind     Count
// ------------------------------ ---------- ------- ----------- -----   --------- ---------
// samp0                             sampler      NA          NA     S0    a5            1
// tex0                              texture  float4          2d     T0    t5            1
// tex1[0][5][3]                     texture  float4          2d     T1   t10        unbounded
// tex2[8]                           texture  float4          2d     T2    t0.space1     8
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
// Approximately 12 instruction slots are used.
```

Ahora, cada intervalo de recursos de sombreador tiene un identificador (un nombre) que es único para el código de bytes del sombreador. Por ejemplo, la matriz de texturas texas1 (t10) se convierte en "T1" en el código de bytes del sombreador. La asignación de identificadores únicos a cada intervalo de recursos permite dos cosas:

-   Identifique de forma inequívoca qué intervalo de recursos (consulte dcl resource texture2d) que se indexa en una instrucción \_ \_ (consulte la instrucción de ejemplo).
-   Adjuntar un conjunto de atributos a la declaración, por ejemplo, tipo de elemento, tamaño de paso, modo de operación de trama, etc.

Tenga en cuenta que el identificador del intervalo no está relacionado con la declaración de límite inferior HLSL.

El orden de los enlaces de recursos de reflexión (lista en la parte superior) y las instrucciones de declaración de sombreador (dcl) es el mismo para ayudar a identificar la correspondencia entre variables HLSL e identificadores de código \_ \* de bytes.

Cada instrucción de declaración de SM5.1 usa un operando 3D para definir: id. de intervalo, límites inferior y superior. Se emite un token adicional para especificar el espacio de registro. También se pueden emitir otros tokens para transmitir propiedades adicionales del intervalo, por ejemplo, la instrucción de declaración de búfer estructurado o de cbuffer emite el tamaño del búfer o la estructura. Los detalles exactos de la codificación se pueden encontrar en d3d12TokenizedProgramFormat.h y **D3D10ShaderBinary::CShaderCodeParser**.

Las instrucciones SM5.1 no emitirán información adicional sobre operandos de recursos como parte de la instrucción (como en SM5.0). Esta información se encuentra ahora en las instrucciones de declaración. En SM5.0, las instrucciones de indexación de recursos requerían que los atributos de recursos se describieron en tokens de código de operación extendidos, ya que la indexación ofuscaba la asociación a la declaración. En SM5.1, cada identificador (como "t1") está asociado inequívocamente a una única declaración que describe la información de recursos necesaria. Por lo tanto, ya no se emiten los tokens de código de operación extendidos que se usan en las instrucciones para describir la información de recursos.

En las instrucciones que no son de declaración, un operando de recurso para muestreadores, SRV y UAV es un operando 2D. El primer índice es una constante literal que especifica el identificador de intervalo. El segundo índice representa el valor linealizado del índice. El valor se calcula con respecto al principio del espacio de registro correspondiente (no relativo al principio del intervalo lógico) para correlacionar mejor con la firma raíz y reducir la carga del compilador del controlador de ajustar el índice.

Un operando de recurso para CBV es un operando 3D que contiene: identificador literal del intervalo, índice del búfer constante, desplazamiento en la instancia concreta del búfer constante.

## <a name="example-hlsl-declarations"></a>Declaraciones HLSL de ejemplo

Los programas HLSL no necesitan saber nada sobre las firmas raíz. Pueden asignar enlaces al espacio de enlace "registrar" virtual, t para SRV, u para UAV, b para CBV, s para muestreadores o confiar en el compilador para elegir asignaciones (y consultar las asignaciones resultantes mediante la reflexión del \# \# \# \# sombreador más adelante). La firma raíz asigna tablas de descriptores, descriptores raíz y constantes raíz a este espacio de registro virtual.

Las siguientes son algunas declaraciones de ejemplo que podría tener un sombreador HLSL. Tenga en cuenta que no hay referencias a las firmas raíz ni a las tablas de descriptores.

``` syntax
Texture2D foo[5] : register(t2);
Buffer bar : register(t7);
RWBuffer dataLog : register(u1);

Sampler samp : register(s0);

struct Data
{
    UINT index;
    float4 color;
};
ConstantBuffer<Data> myData : register(b0);

Texture2D terrain[] : register(t8); // Unbounded array
Texture2D misc[] : register(t0,space1); // Another unbounded array 
                                        // space1 avoids overlap with above t#

struct MoreData
{
    float4x4 xform;
};
ConstantBuffer<MoreData> myMoreData : register(b1);

struct Stuff
{
    float2 factor;
    UINT drawID;
};
ConstantBuffer<Stuff> myStuff[][3][8]  : register(b2, space3)
```

## <a name="related-topics"></a>Temas relacionados

* [Indexado dinámico mediante HLSL 5.1](dynamic-indexing-using-hlsl-5-1.md)
* [Herramienta Effect-Compiler](../direct3dtools/fxc.md)
* [Características del modelo de sombreador HLSL 5.1 para Direct3D 12](../direct3dhlsl/hlsl-shader-model-5-1-features-for-direct3d-12.md)
* [Vistas ordenadas por el rasterizador](rasterizer-order-views.md)
* [Enlace de recursos](resource-binding.md)
* [Firmas raíz](root-signatures.md)
* [Modelo de sombreador 5.1](../direct3dhlsl/shader-model-5-1.md)
* [Valor de la referencia de galería de símbolos especificado por el sombreador](shader-specified-stencil-reference-value.md)
* [Especificación de firmas de raíz en HLSL](specifying-root-signatures-in-hlsl.md)