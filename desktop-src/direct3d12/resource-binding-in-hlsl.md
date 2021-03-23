---
title: Enlace de recursos en HLSL
description: En este tema se describen algunas características específicas del uso del modelo de sombreador del lenguaje HLSL (High Level Shader Language) 5,1 con Direct3D 12.
ms.assetid: 3CD4BDAD-8AE3-4DE0-B3F8-9C9F9E83BBE9
ms.localizationpriority: high
ms.topic: article
ms.date: 08/27/2019
ms.openlocfilehash: 01039550f07de57fb7b2f1e815bced02e549c741
ms.sourcegitcommit: 60120d10c957815d79af566c72e5f4bcfaca4025
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/23/2021
ms.locfileid: "104837493"
---
# <a name="resource-binding-in-hlsl"></a>Enlace de recursos en HLSL

En este tema se describen algunas características específicas del uso del [modelo de sombreador](/windows/desktop/direct3dhlsl/shader-model-5-1) del lenguaje HLSL (High Level Shader Language) 5,1 con Direct3D 12. Todo el hardware de Direct3D 12 admite el modelo de sombreador 5,1, por lo que la compatibilidad con este modelo no depende de cuál sea el nivel de características de hardware.

## <a name="resource-types-and-arrays"></a>Tipos de recursos y matrices

La sintaxis de recursos del modelo de sombreador 5 (SM 5.0) usa la `register` palabra clave para retransmitir información importante sobre el recurso al compilador de HLSL. Por ejemplo, la instrucción siguiente declara una matriz de cuatro texturas enlazadas a las ranuras T3, T4, T5 y T6. T3 es la única ranura de registro que aparece en la instrucción, simplemente siendo la primera en la matriz de cuatro.

``` syntax
Texture2D<float4> tex1[4] : register(t3)
```

La sintaxis de recursos del modelo de sombreador 5,1 (SM 5.1) en HLSL se basa en la sintaxis de recursos de registro existente para permitir una migración más sencilla. Los recursos de Direct3D 12 en HLSL están enlazados a registros virtuales dentro de espacios de registro lógicos:

-   t: para vistas de recursos del sombreador (SRV)
-   s: para muestreadores
-   u: para vistas de acceso desordenado (UAV)
-   b: para las vistas de búfer de constantes (CBV)

La firma raíz que hace referencia al sombreador debe ser compatible con las ranuras de registro declaradas. Por ejemplo, la siguiente parte de una firma raíz sería compatible con el uso de ranuras de textura T3 a través de T6, ya que describe una tabla de descriptores con ranuras de T0 a T98.

``` syntax
DescriptorTable( CBV(b1), SRV(t0,numDescriptors=99), CBV(b2) )
```

Una declaración de recursos puede ser una matriz escalar, 1D o multidimensional:

``` syntax
Texture2D<float4> tex1 : register(t3,  space0)
Texture2D<float4> tex2[4] : register(t10)
Texture2D<float4> tex3[7][5][3] : register(t20, space1)
```

SM 5.1 usa los mismos tipos de recursos y tipos de elemento que el SM 5.0. Los límites de declaración de SM 5.1 son más flexibles y solo están restringidos por los límites de hardware y tiempo de ejecución. La `space` palabra clave especifica el espacio de registro lógico al que está enlazada la variable declarada. Si `space` se omite la palabra clave, el índice de espacio predeterminado de 0 se asigna implícitamente al intervalo (por lo que el `tex2` intervalo anterior reside en `space0` ). `register(t3,  space0)` nunca entrará en conflicto con `register(t3,  space1)` , ni con ninguna matriz en otro espacio que podría incluir T3.

Un recurso de matriz puede tener un tamaño sin enlazar, que se declara especificando la primera dimensión que está vacía, o 0:

``` syntax
Texture2D<float4> tex1[] : register(t0)
```

La tabla del descriptor coincidente podría ser:

``` syntax
DescriptorTable( CBV(b1), UAV(u0, numDescriptors = 4), SRV(t0, numDescriptors=unbounded)
```

Una matriz sin enlazar en HLSL coincide con un número fijo establecido con `numDescriptors` en la tabla de descriptores y un tamaño fijo en HLSL coincide con una declaración sin enlazar en la tabla de descriptores.

Se permiten matrices multidimensionales, incluido un tamaño sin enlazar. Estas matrices multidimensionales se separan en el espacio de registro.

``` syntax
Texture2D<float4> tex2[3000][10] : register(t0, space0); // t0-t29999 in space0
Texture2D<float4> tex3[0][5][3] : register(t5, space1)
```

No se permiten los alias de los intervalos de recursos. En otras palabras, para cada tipo de recurso (t, s, u, b), los intervalos de registro declarados no debe se superponen. Esto incluye también los intervalos sin enlazar. Los rangos declarados en diferentes espacios de registro nunca se superponen. Tenga en cuenta que el modo sin enlazar `tex2` (anterior) reside en `space0` , mientras que sin enlazar `tex3` reside en, de forma `space1` que no se superpongan.

El acceso a los recursos que se han declarado como matrices es tan sencillo como indexarlos.

``` syntax
Texture2D<float4> tex1[400] : register(t3);
sampler samp[7] : register(s0);
tex1[myMaterialID].Sample(samp[samplerID], texCoords);
```

Existe una restricción predeterminada importante en el uso de los índices ( `myMaterialID` y `samplerID` en el código anterior) en que no se les permite variar dentro de una [onda](../direct3dhlsl/hlsl-shader-model-6-0-features-for-direct3d-12.md#terminology). Incluso cambiar el índice basado en la creación de instancias cuenta como variable.

Si se requiere variar el índice, especifique el `NonUniformResourceIndex` calificador en el índice, por ejemplo:

``` syntax
tex1[NonUniformResourceIndex(myMaterialID)].Sample(samp[NonUniformResourceIndex(samplerID)], texCoords);
```

En el hardware, el uso de este calificador genera código adicional para aplicar la corrección (incluidos entre subprocesos), pero con un costo de rendimiento menor. Si se cambia un índice sin este calificador y, dentro de un dibujo o una distribución, los resultados son indefinidos.

## <a name="descriptor-arrays-and-texture-arrays"></a>Matrices de descriptores y matrices de texturas

Las matrices de texturas están disponibles desde DirectX 10. Las matrices de textura requieren un descriptor; sin embargo, todos los segmentos de la matriz deben compartir el mismo formato, el ancho, el alto y el número de MIP. Además, la matriz debe ocupar un intervalo contiguo en el espacio de direcciones virtuales. En el código siguiente se muestra un ejemplo del acceso a una matriz de textura desde un sombreador.

``` syntax
Texture2DArray<float4> myTex2DArray : register(t0); // t0
float3 myCoord(1.0f,1.4f,2.2f); // 2.2f is array index (rounded to int)
color = myTex2DArray.Sample(mySampler, myCoord);
```

En una matriz de textura, el índice se puede variar libremente, sin necesidad de calificadores como `NonUniformResourceIndex` .

La matriz de descriptor equivalente sería:

``` syntax
Texture2D<float4> myArrayOfTex2D[] : register(t0); // t0+
float2 myCoord(1.0f, 1.4f);
color = myArrayOfTex2D[2].Sample(mySampler,myCoord); // 2 is index
```

Tenga en cuenta que el uso poco práctico de un valor Float para el índice de matriz se reemplaza por `myArrayOfTex2D[2]` . Además, las matrices de descriptor ofrecen más flexibilidad con las dimensiones. El tipo, `Texture2D` es este ejemplo, no puede variar, pero el formato, el ancho, el alto y el número de MIP pueden variar con cada descriptor.

Es legítimo tener una matriz de descriptores de matrices de texturas:

``` syntax
Texture2DArray<float4> myArrayOfTex2DArrays[2] : register(t0);
```

No es legítimo declarar una matriz de estructuras, por ejemplo, no se admite cada estructura que contiene descriptores.

``` syntax
struct myStruct {
    Texture2D                    a; 
    Texture2D                    b;
    ConstantBuffer<myConstants>  c;
};
myStruct foo[10000] : register(....);
```

Esto habría permitido el diseño de memoria **abcabcabc...**, pero es una limitación de idioma y no se admite. Un método admitido para hacerlo sería el siguiente, aunque en este caso el diseño de memoria es **AAA... BBB... CCC..**..

``` syntax
Texture2D                     a[10000] : register(t0);
Texture2D                     b[10000] : register(t10000);
ConstantBuffer<myConstants>   c[10000] : register(b0);
```

Para lograr el diseño de memoria **abcabcabc....** , use una tabla de descriptores sin usar la `myStruct` estructura.

## <a name="resource-aliasing"></a>Alias de recursos

Los intervalos de recursos especificados en los sombreadores HLSL son intervalos lógicos. Se enlazan a intervalos de montón concretos en tiempo de ejecución a través del mecanismo de firma raíz. Normalmente, un intervalo lógico se asigna a un intervalo de montón que no se superpone con otros intervalos de montón. Sin embargo, el mecanismo de firma raíz permite el alias (superponer) los intervalos de montones de tipos compatibles. Por ejemplo, `tex2` los `tex3` intervalos del ejemplo anterior pueden estar asignados al mismo intervalo de montones (o superpuestos), lo que tiene el efecto de aplicar alias a las texturas en el programa HLSL. Si se desea usar este tipo de alias, el sombreador se debe compilar con la \_ \_ opción de alias D3D10 de los recursos del sombreador \_ \_ para la [herramienta de compilador de efectos](/windows/win32/direct3dtools/fxc) (FXC). *\_ \_* La opción hace que el compilador genere código correcto mediante la prevención de ciertas optimizaciones de carga y almacenamiento bajo la suposición de que los recursos pueden tener alias.

## <a name="divergence-and-derivatives"></a>Divergencia y derivados

SM 5.1 no impone limitaciones en el índice de recursos; es decir, ` tex2[idx].Sample(…)` : el índ de índice puede ser una constante literal, una constante CBuffer o un valor interpolado. Aunque el modelo de programación proporciona una gran flexibilidad, hay problemas que debe tener en cuenta:

-   Si el índice difiere en un cuádruple, el derivado calculado por hardware y las cantidades derivadas como LOD pueden ser indefinidos. El compilador de HLSL realiza el mejor esfuerzo para emitir una advertencia en este caso, pero no impedirá que se compile un sombreador. Este comportamiento es similar al cálculo de derivados en un flujo de control divergente.
-   Si el índice de recursos es divergente, el rendimiento se reduce en comparación con el caso de un índice uniforme, ya que el hardware necesita realizar operaciones en varios recursos. Los índices de recursos que pueden ser divergentes se deben marcar con la `NonUniformResourceIndex` función en el código HLSL. De lo contrario, los resultados son indefinidos.

## <a name="uavs-in-pixel-shaders"></a>UAVs en sombreadores de píxeles

SM 5.1 no impone restricciones en los intervalos de UAV en los sombreadores de píxeles como era el caso del SM 5.0.

## <a name="constant-buffers"></a>Búferes de constantes

La sintaxis de búferes de constantes de SM 5.1 (CBuffer) ha cambiado desde SM 5.0 para que los desarrolladores puedan indexar búferes de constantes. Para habilitar los búferes de constantes indexables, SM 5.1 presenta la `ConstantBuffer` construcción "template":

``` syntax
struct Foo
{
    float4 a;
    int2 b;
};
ConstantBuffer<Foo> myCB1[2][3] : register(b2, space1);
ConstantBuffer<Foo> myCB2 : register(b0, space1);
```

El código anterior declara una variable de búfer `myCB1` de constantes de tipo `Foo` y tamaño 6, y una variable de búfer escalar constante `myCB2` . Ahora se puede indexar una variable de búfer de constantes en el sombreador como:

``` syntax
myCB1[i][j].a.xyzw
myCB2.b.yy
```

Los campos ' a ' y ' b ' no se convierten en variables globales, sino que deben tratarse como campos. Por compatibilidad con versiones anteriores, SM 5.1 admite el concepto de CBuffer anterior para cbuffers escalar. La instrucción siguiente crea variables globales de solo lectura ' a ' y ' b ' como en SM 5.0. Sin embargo, este tipo de CBuffer de estilo antiguo no se puede indexar.

``` syntax
cbuffer : register(b1)
{
    float4 a;
    int2 b;
};
```

Actualmente, el compilador de sombreador admite la `ConstantBuffer` plantilla solo para estructuras definidas por el usuario.

Por motivos de compatibilidad, el compilador de HLSL puede asignar automáticamente registros de recursos para los intervalos declarados en `space0` . Si se omite ' Space ' en la cláusula Register, se usa el valor predeterminado `space0` . El compilador usa la heurística del primer orificio para asignar los registros. La asignación se puede recuperar a través de la API de reflexión, que se ha ampliado para agregar el campo de *espacio* para el espacio, mientras que el campo *BindPoint* indica el límite inferior del intervalo del registro de recursos.

## <a name="bytecode-changes-in-sm51"></a>Cambios de código de bytes en SM 5.1

SM 5.1 cambia el modo en que se declaran y se hace referencia a los registros de recursos en las instrucciones. La sintaxis implica declarar una "variable" de registro, de forma similar a como se hace para los registros de memoria compartida de Grupo:

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

Esto se desensamblará en:

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

Ahora cada intervalo de recursos del sombreador tiene un identificador (un nombre) que es único para el código de bytes del sombreador. Por ejemplo, la matriz de texturas de Tex1 (T10) se convierte en ' t 1 ' en el código de bytes del sombreador. Asignar identificadores únicos a cada intervalo de recursos permite dos cosas:

-   Identifique de forma inequívoca qué intervalo de recursos (consulte DCL \_ Resource \_ texture2d) se está indizando en una instrucción (vea la instrucción de ejemplo).
-   Asociar un conjunto de atributos a la declaración, por ejemplo, tipo de elemento, tamaño de intervalo, modo de operación de trama, etc.

Tenga en cuenta que el identificador del intervalo no está relacionado con la declaración de límite inferior de HLSL.

El orden de los enlaces de recursos de reflexión (enumeración en la parte superior) y las instrucciones de declaración de sombreador (DCL \_ \* ) es el mismo para ayudar a identificar la correspondencia entre las variables de HLSL y los ID. de código de bytes.

Cada instrucción de declaración en SM 5.1 usa un operando 3D para definir: ID. de intervalo, límites inferior y superior. Se emite un token adicional para especificar el espacio de registro. También se pueden emitir otros tokens para transmitir propiedades adicionales del intervalo; por ejemplo, CBuffer o la instrucción de declaración de búfer estructurado emite el tamaño de la CBuffer o la estructura. Los detalles exactos de la codificación se pueden encontrar en d3d12TokenizedProgramFormat. h y **D3D10ShaderBinary:: CShaderCodeParser**.

Las instrucciones de SM 5.1 no emitirán información adicional del operando de recursos como parte de la instrucción (como en SM 5.0). Esta información está ahora en las instrucciones de declaración. En SM 5.0, instrucciones que indexan los recursos de recursos necesarios para describirse en tokens de código de operación extendidos, ya que la indización ofuscaba la asociación con la declaración. En SM 5.1, cada identificador (como ' t 1 ') está asociado de forma no ambigua a una única declaración que describe la información de recursos necesaria. Por lo tanto, los tokens de código de operación extendidos usados en las instrucciones para describir la información de recursos ya no se emiten.

En las instrucciones que no son de declaración, un operando de recursos para muestreadores, SRVs y UAVs es un operando 2D. El primer índice es una constante literal que especifica el identificador del intervalo. El segundo índice representa el valor de linealización del índice. El valor se calcula en relación con el principio del espacio de registro correspondiente (no con respecto al principio del intervalo lógico) para correlacionar mejor con la firma raíz y reducir la carga del compilador de controladores para ajustar el índice.

Un operando de recurso para CBVs es un operando 3D, que contiene: el identificador de literal del intervalo, el índice del búfer de constantes, el desplazamiento en la instancia concreta de búfer de constantes.

## <a name="example-hlsl-declarations"></a>Declaraciones de ejemplo de HLSL

No es necesario que los programas HLSL sepan nada sobre las firmas raíz. Pueden asignar enlaces al espacio de enlace virtual "Register", t \# para SRVs, u \# para UAVs, b \# para CBVs, s \# para muestras o confiar en el compilador para seleccionar asignaciones (y consultar las asignaciones resultantes mediante la reflexión del sombreador posteriormente). La firma raíz asigna las tablas de descriptores, los descriptores raíz y las constantes raíz a este espacio de registro virtual.

A continuación se muestran algunas declaraciones de ejemplo que puede tener un sombreador HLSL. Tenga en cuenta que no hay ninguna referencia a las tablas de descriptores o firmas de raíz.

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
* [Efecto: herramienta de compilador](/windows/win32/direct3dtools/fxc)
* [Características del modelo de sombreador de HLSL 5,1 para Direct3D 12](/windows/win32/direct3dhlsl/hlsl-shader-model-5-1-features-for-direct3d-12)
* [Vistas ordenadas de rasterizador](rasterizer-order-views.md)
* [Enlace de recursos](resource-binding.md)
* [Firmas raíz](root-signatures.md)
* [Modelo de sombreador 5,1](/windows/win32/direct3dhlsl/shader-model-5-1)
* [Valor de referencia de estarcido del sombreador especificado](shader-specified-stencil-reference-value.md)
* [Especificación de firmas de raíz en HLSL](specifying-root-signatures-in-hlsl.md)
