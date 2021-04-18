---
title: Shader Model 3 (referencia de HLSL)
description: Los sombreadores de vértices y los sombreadores de píxeles se simplifican considerablemente de las versiones anteriores del sombreador.
ms.assetid: 01ac85cb-b309-4169-acc2-320a929b65cb
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c3517266ace77b9235604770d9b42d10cd80e2d5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420897"
---
# <a name="shader-model-3-hlsl-reference"></a>Shader Model 3 (referencia de HLSL)

Los sombreadores de vértices y los sombreadores de píxeles se simplifican considerablemente de las versiones anteriores del sombreador. Si está implementando sombreadores en hardware, no puede usar vs \_ 3 \_ 0 o PS \_ 3 \_ 0 con ninguna otra versión del sombreador, y no puede usar ninguno de los tipos de sombreador con la canalización de función fija. Estos cambios permiten simplificar los controladores y el tiempo de ejecución. La única excepción es que los sombreadores de solo software vs \_ 3 \_ 0 se pueden usar con cualquier versión de sombreador de píxeles. Además, si usa un sombreador de solo software vs \_ 3 \_ 0 con una versión de sombreador de píxeles anterior, el sombreador de vértices solo puede utilizar la semántica de salida que sea compatible con los códigos de formato de vértice flexible (FVF).

La semántica que se usa en las salidas del sombreador de vértices se debe usar en entradas del sombreador de píxeles. La semántica se usa para asignar las salidas del sombreador de vértices a las entradas del sombreador de píxeles, similar a la forma en que se asigna la declaración de vértices a los registros de entrada del sombreador de vértices y los modelos de sombreador anteriores. Consulte semántica de coincidencia en los sombreadores de vs 3,0 y PS 3,0.

Se han agregado Estados de representación del modo de ajuste adicionales para cubrir la posibilidad de coordenadas de textura adicionales en este nuevo esquema. Los atributos con D3DDECLUSAGE \_ TEXCOORD y el índice de uso de 0 a 15 se interpolan en el modo de ajuste cuando se establece el [**\_ ajuste \* de D3DRS**](/windows/desktop/direct3d9/d3drenderstatetype) correspondiente.

-   [Características del modelo de sombreador de vértice 3](#vertex-shader-model-3-features)
-   [Características del modelo de sombreador de píxeles 3](#pixel-shader-model-3-features)
-   [Coincidencia de la semántica en \_ los \_ sombreadores de vs 3 0 y PS \_ 3 \_ 0](/windows)
-   [Cambios en el modo de niebla, profundidad y sombreado](#fog-depth-and-shading-mode-changes)
-   [Conversiones de punto flotante y entero](#floating-point-and-integer-conversions)
-   [Especificar una precisión completa o parcial](#specifying-full-or-partial-precision)
-   [Sombreadores de píxeles y vértices de software](#software-vertex-and-pixel-shaders)

## <a name="vertex-shader-model-3-features"></a>Características del modelo de sombreador de vértice 3

Los tipos de registro de salida del sombreador de vértices se han contraído en doce registros (consulte [registros de salida](dx9-graphics-reference-asm-vs-registers-output.md)). Cada registro que se usa debe declararse mediante la instrucción [DCL](dcl-usage---ps.md) y una semántica (por ejemplo, DCL \_ color0 O0. xyzw).

El \_ modelo de sombreador de vértices 3 0 (vs \_ 3 \_ 0) amplía las características de vs \_ 2 \_ 0 con indexación de registros más eficaz, un conjunto de registros de salida simplificados, la capacidad de muestrear una textura en un sombreador de vértices y la capacidad de controlar la velocidad a la que se inicializan las entradas del sombreador.

### <a name="index-any-register"></a>Indexar cualquier registro

Todos los registros (registros de [entrada](dx9-graphics-reference-asm-vs-registers-input.md) y registro de [salida](dx9-graphics-reference-asm-vs-registers-output.md)) se pueden indexar mediante [el registro de contadores de bucle](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (solo los registros de constantes se pueden indizar en versiones anteriores).

Debe declarar los registros de entrada y salida antes de indizarlos. Sin embargo, no puede indexar ningún registro de salida que se haya declarado con una posición o una semántica de tamaño de punto. De hecho, si se usa la indexación, la semántica de posición y psize debe declararse en los registros O0 y O1, respectivamente.

Solo se permite indexar un intervalo continuo de registros; es decir, no se puede indexar entre los registros que no se han declarado. Aunque esta restricción puede ser inadecuada, permite que se lleve a cabo la optimización del hardware. Si se intenta indexar en registros no contiguos, se producirán resultados indefinidos. La validación del sombreador no aplica esta restricción.

### <a name="simplify-output-registers"></a>Simplificar registros de salida

Todos los distintos tipos de registros de salida se han contraído en doce registros de salida: 1 para la posición, 2 para el color, 8 para la textura y 1 para la niebla o el tamaño del punto. Estos registros interpolarán los datos que contengan para el sombreador de píxeles. Las declaraciones de registro de salida son obligatorias y las semánticas se asignan a cada registro.

Los registros se pueden dividir de la siguiente manera:

-   Al menos un registro debe declararse como un registro de posición de cuatro componentes. Este es el único registro del sombreador de vértices necesario.
-   Los diez primeros registros utilizados por un sombreador pueden usar hasta cuatro componentes (xyzw) como máximo.
-   El último (o duodécimo) registro solo puede contener un valor escalar (por ejemplo, un tamaño de punto).

Para obtener una lista de los registros, consulte [registros-vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md).

### <a name="texture-sample-in-a-vertex-shader"></a>Ejemplo de textura en un sombreador de vértices

Vertex Shader 3 \_ 0 admite la búsqueda de texturas en el sombreador de vértices mediante [texldl-vs](texldl---vs.md).

## <a name="pixel-shader-model-3-features"></a>Características del modelo de sombreador de píxeles 3

Los registros de color y textura del sombreador de píxeles se han contraído en diez registros de entrada (consulte [tipos de registro de entrada](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)). El registro facial es un registro escalar de punto flotante. Solo el signo de este registro es válido. Si el signo es negativo, el primitivo es una parte posterior. Se puede usar dentro de un sombreador de píxeles para lograr la iluminación de dos caras, por ejemplo. El registro de posición hace referencia a los píxeles actuales (x, y).

Los registros de constantes del sombreador se pueden establecer mediante:

-   [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb)
-   [**SetPixelShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti)
-   [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf)

## <a name="match-semantics-on-vs_3_0-and-ps_3_0-shaders"></a>Coincidencia de la semántica en \_ los \_ sombreadores de vs 3 0 y PS \_ 3 \_ 0

Existen algunas restricciones en el uso semántico con vs \_ 3 \_ 0 y PS \_ 3 \_ 0. En general, debe tener cuidado al usar una semántica para una entrada de sombreador que coincida con una semántica usada en una salida de sombreador.

Por ejemplo, este sombreador de píxeles empaqueta varios nombres en un registro:


```
ps_3_0 
dcl_texcoord0 v0.x 
dcl_texcoord1 v0.yz // Valid to pack multiple names into one register 
dcl_texcoord2_centroid v1.w
...
```



Cada registro tiene una semántica diferente. Tenga en cuenta que también puede denominar v0. x y v0. YZ con una semántica diferente (varias) debido al uso de la máscara de escritura.

Dado el sombreador de píxeles, el siguiente \_ sombreador de vs 3 \_ 0 no puede emparejarse con él:


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o6.yzw 
...
```



Estos dos sombreadores entran en conflicto con el uso de la semántica de [**D3DDECLUSAGE \_ TEXCOORD0**](/windows/desktop/direct3d9/d3ddeclusage) y **D3DDECLUSAGE \_ TEXCOORD1** .

Vuelva a escribir el sombreador de vértices como este para evitar la colisión semántica:


```
vs_3_0 
... 
dcl_texcoord2 o3 
dcl_texcoord3 o9 
...
```



Del mismo modo, no se puede usar un nombre semántico declarado en registros de entrada diferentes en el sombreador de píxeles (V0 y V1 en el sombreador de píxeles) en un registro de salida único en este sombreador de vértices. Por ejemplo, este sombreador de vértices no se puede emparejar con el sombreador de píxeles porque D3DDECLUSAGE \_ TEXCOORD1 se usa para los registros de entrada del sombreador de píxeles (V0, V1) y el registro de salida del sombreador de vértices O3.


```
vs_3_0 
... 
dcl_texcoord0 o3.x 
dcl_texcoord1 o3.yz 

dcl_texcoord2 o3.w // BAD! Would be valid if this were not o3 
dcl_texcoord3 o9 ... 
```



Por otro lado, este sombreador de vértices no se puede emparejar con el sombreador de píxeles porque la máscara de salida de un parámetro con una semántica determinada no proporciona los datos que el sombreador de píxeles solicita:


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o5.yzw 
dcl_texcoord2 o7.yz // BAD! Would be valid if w were included 
dcl_texcoord3 o9 
... 
```



Este sombreador de vértices no proporciona una salida con uno de los nombres semánticos solicitados por el sombreador de píxeles, por lo que el emparejamiento del sombreador no es válido:


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o5.yzw 
dcl_texcoord3 o9 
// The pixel shader wants texcoord2, with a w component, 
// but it isn't output by this vertex shader at all! 
... 
```



## <a name="fog-depth-and-shading-mode-changes"></a>Cambios en el modo de niebla, profundidad y sombreado

Cuando \_ se establece D3DRS SHADEMODE para el sombreado plano durante la rasterización de recorte y triángulos, los atributos con \_ color D3DDECLUSAGE se interpolan como sombreados planos. Si los componentes de un registro se declaran con una semántica de color, pero otros componentes del mismo registro tienen una semántica diferente, la interpolación de sombreado plano (lineal y plana) no se definirá en los componentes de que se registran sin una semántica de color.

Si se desea la representación de niebla, \_ los \_ sombreadores de vs 3 0 y PS \_ 3 \_ 0 deben implementar la niebla. No se realizan cálculos de niebla fuera de los sombreadores. No hay ningún registro de niebla en vs \_ 3 \_ 0, y la niebla adicional D3DDECLUSAGE \_ (para el factor de mezcla de niebla calculada por vértice) y la profundidad de D3DDECLUSAGE \_ (para pasar un valor de profundidad al sombreador de píxeles para calcular el factor de mezcla de niebla) se han agregado.

El estado de fase de textura D3DTSS \_ TEXCOORDINDEX se omite cuando se usa el sombreador de píxeles 3,0.

Se han agregado los siguientes valores para dar cabida a estos cambios:


```
// Fog and Depth usages
D3DDECLUSAGE_FOG 
D3DDECLUSAGE_DEPTH 

// Additional wrap states for vs_3_0 attributes with D3DDECLUSAGE_TEXCOORD 
D3DRS_WRAP8 
D3DRS_WRAP9 
D3DRS_WRAP10 
D3DRS_WRAP11 
D3DRS_WRAP12 
D3DRS_WRAP13 
D3DRS_WRAP14 
D3DRS_WRAP15
```



## <a name="floating-point-and-integer-conversions"></a>Conversiones de punto flotante y entero

Los cálculos matemáticos de punto flotante se producen en diferentes precisión y rangos (16 bits, 24 bits y 32 bits) en diferentes partes de la canalización. Un valor mayor que el intervalo dinámico de la canalización que entra en esa canalización (por ejemplo, un mapa de textura flotante de 32 bits se muestrea en una canalización Float de 24 bits en PS \_ 2 \_ 0) crea un resultado no definido. En el caso del comportamiento predecible, debe fijar este valor en el máximo del intervalo dinámico.

La conversión de un valor de punto flotante a un entero se produce en varios lugares, como:

-   Al encontrar una instrucción [mova-vs](mova---vs.md) .
-   Durante el direccionamiento de textura.
-   Al escribir en un destino de representación de punto no flotante.

## <a name="specifying-full-or-partial-precision"></a>Especificar una precisión completa o parcial

Tanto el PS \_ 3 \_ como el PS \_ 2 \_ x proporcionan compatibilidad con dos niveles de precisión:



|          |          |                   |                      |
|----------|----------|-------------------|----------------------|
| PS \_ 3 \_ 0 | PS \_ 2 \_ 0 | Precisión         | Value                |
| x        |          | Completo              | fp32 o superior       |
| x        |          | Precisión parcial | FP16 = s10e5           |
| x        | x        | Completo              | fp24 = s16e7 o superior |
| x        | x        | Precisión parcial | FP16 = s10e5           |



 

PS \_ 3 \_ 0 admite más precisión que PS \_ 2 \_ 0. De forma predeterminada, todas las operaciones se producen en el nivel de precisión completa.

La precisión parcial (vea [modificadores de registro del sombreador de píxeles](dx9-graphics-reference-asm-ps-registers-modifiers.md)) se solicita agregando el \_ modificador PP al código del sombreador (siempre que la implementación subyacente lo admita). Las implementaciones siempre son gratuitas para omitir el modificador y realizar las operaciones afectadas con precisión completa.

El \_ modificador PP puede producirse en dos contextos:

-   En una declaración de coordenadas de textura para pasar coordenadas de textura de precisión parcial al sombreador de píxeles. Esto se podría usar cuando las coordenadas de textura retransmiten los datos de color al sombreador de píxeles, que puede ser más rápido con una precisión parcial que con precisión completa en algunas implementaciones.
-   En cualquier instrucción para solicitar el uso de precisión parcial, incluidas las instrucciones de carga de textura. Esto indica que la implementación puede ejecutar la instrucción con precisión parcial y almacenar un resultado de precisión parcial. En ausencia de un modificador explícito, la instrucción se debe realizar a plena precisión (independientemente de la precisión de los operandos de entrada).

Una aplicación podría elegir deliberadamente la precisión para el rendimiento. Hay varios tipos de datos de entrada de sombreador que son candidatos naturales para el procesamiento de precisión parcial:

-   Los iteradores de color están bien representados por valores de precisión parcial.
-   Los valores de las texturas de la mayoría de los formatos se pueden representar con precisión mediante valores de precisión parcial (los valores muestreados desde 32 bits, las texturas de formato de punto flotante son una excepción obvia).
-   Las constantes se pueden representar mediante una representación de precisión parcial, según corresponda al sombreador.

En todos estos casos, el desarrollador puede elegir especificar la precisión parcial para procesar los datos, sabiendo que no se pierde la precisión de los datos de entrada. En algunos casos, es posible que un sombreador requiera que los pasos internos de un cálculo se realicen con precisión completa, incluso cuando los valores de entrada y salida finales no tengan más de una precisión parcial.

## <a name="software-vertex-and-pixel-shaders"></a>Sombreadores de píxeles y vértices de software

Las implementaciones de software (tiempo de ejecución y referencia para los sombreadores de vértices y referencia para los sombreadores de píxeles) de los sombreadores de la versión 2 \_ 0 y versiones posteriores tienen una validación relajada. Esto resulta útil para la depuración y la generación de prototipos. La aplicación indica al tiempo de ejecución o ensamblador que necesita parte de la validación relajada mediante la \_ marca SW en el ensamblador (por ejemplo, vs \_ 2 \_ SW). Un sombreador de software no funcionará con el hardware.

vs \_ 2 \_ SW es una flexibilización de los límites máximos de vs \_ 2 \_ x; de forma similar, PS \_ 2 \_ SW es una flexibilización de los límites máximos de PS \_ 2 \_ x. En concreto, se relajan las validaciones siguientes:



|                                            |                                      |                                                                                                                                   |
|--------------------------------------------|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Modelo de sombreador                               | Resource                             | Límite                                                                                                                             |
| vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW | Recuentos de instrucciones                   | Sin límite                                                                                                                         |
| vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW | Registros de constantes Float             | 8192                                                                                                                              |
| vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW | Registros de constantes de tipo entero           | 2048                                                                                                                              |
| vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW | Registros de constantes booleanas           | 2048                                                                                                                              |
| PS \_ 2 \_ SW                                  | Dependiente: profundidad de lectura                 | Sin límite                                                                                                                         |
| vs \_ 2 \_ SW                                  | instrucciones y etiquetas de control de flujo | Sin límite                                                                                                                         |
| vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW | Inicio de bucle/pasos/recuentos               | El tamaño de paso de iteración y de inicio de la iteración para las instrucciones REP y Loop son enteros de 32 bits con signo. Count puede ser hasta MAX \_ int/64. |
| vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW | Límites de Puerto                          | Los límites de puerto para todos los archivos de registro son relajados.                                                                                   |
| vs \_ 3 \_ SW                                  | Número de interpoladores              | 16 registros de salida en vs \_ 3 \_ SW.                                                                                                 |
| PS \_ 3 \_ SW                                  | Número de interpoladores              | 14 (16-2) registros de entrada para el \_ SW PS 3 \_ .                                                                                           |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)
</dt> </dl>

 

 