---
title: Modelo de sombreador 3 (referencia hlsl)
description: Los sombreadores de vértices y los sombreadores de píxeles se simplifican considerablemente a partir de versiones anteriores del sombreador.
ms.assetid: 01ac85cb-b309-4169-acc2-320a929b65cb
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2d87c791694e91de135052b4172e3bd5f55577d7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127573673"
---
# <a name="shader-model-3-hlsl-reference"></a>Modelo de sombreador 3 (referencia hlsl)

Los sombreadores de vértices y los sombreadores de píxeles se simplifican considerablemente a partir de versiones anteriores del sombreador. Si va a implementar sombreadores en hardware, es posible que no use vs \_ 3 0 o \_ ps \_ 3 0 con ninguna otra versión del sombreador, y no puede usar ningún tipo de sombreador con la canalización de función \_ fija. Estos cambios hacen posible simplificar los controladores y el tiempo de ejecución. La única excepción es que se pueden usar sombreadores de solo software frente \_ a 3 0 con cualquier versión del \_ sombreador de píxeles. Además, si usa un sombreador solo de software frente a 3 0 con una versión anterior del sombreador de píxeles, el sombreador de vértices solo puede usar semántica de salida compatible con códigos de formato de vértice \_ \_ flexible (FVF).

La semántica usada en las salidas del sombreador de vértices debe usarse en las entradas del sombreador de píxeles. La semántica se usa para asignar las salidas del sombreador de vértices a las entradas del sombreador de píxeles, de forma similar a la forma en que la declaración de vértice se asigna a los registros de entrada del sombreador de vértices y a los modelos de sombreador anteriores. Consulte Match Semantics on vs 3.0 and ps 3.0 Shaders (Semántica de coincidencias en los sombreadores de vs 3.0 y ps 3.0).

Se han agregado estados de representación de modo de encapsulado adicionales para cubrir la posibilidad de coordenadas de textura adicionales en este nuevo esquema. Los atributos con D3DDECLUSAGE TEXCOORD y el índice de uso de 0 a 15 se interpolan en modo de encapsulado cuando se establece el encapsulado \_ [**D3DRS \_ correspondiente. \***](/windows/desktop/direct3d9/d3drenderstatetype)

-   [Características del modelo 3 del sombreador de vértices](#vertex-shader-model-3-features)
-   [Características del modelo 3 del sombreador de píxeles](#pixel-shader-model-3-features)
-   [Semántica de coincidencias en \_ sombreadores frente a 3 \_ 0 y ps \_ \_ 3 0](/windows)
-   [Cambios en el modo de sombreado, profundidad y profundidad](#fog-depth-and-shading-mode-changes)
-   [Conversiones de punto flotante y entero](#floating-point-and-integer-conversions)
-   [Especificar precisión completa o parcial](#specifying-full-or-partial-precision)
-   [Sombreadores de vértices y píxeles de software](#software-vertex-and-pixel-shaders)

## <a name="vertex-shader-model-3-features"></a>Características del modelo 3 del sombreador de vértices

Los tipos de registro de salida del sombreador de vértices se han contraído en doce registros (vea [Registros de salida).](dx9-graphics-reference-asm-vs-registers-output.md) Cada registro que se usa debe declararse mediante la instrucción [dcl](dcl-usage---ps.md) y una semántica (por ejemplo, dcl \_ color0 o0.xyzw).

El modelo de sombreador de \_ vértices 3 0 (frente a 3 0) se expande en las características de frente a 2 0 con una indexación de registros más eficaz, un conjunto de registros de salida simplificados, la capacidad de muestrear una textura en un sombreador de vértices y la capacidad de controlar la velocidad a la que se inicializan las entradas del \_ \_ \_ \_ sombreador.

### <a name="index-any-register"></a>Indexar cualquier registro

Todos los registros [(registros de](dx9-graphics-reference-asm-vs-registers-input.md) entrada y de [salida)](dx9-graphics-reference-asm-vs-registers-output.md)se pueden indexar mediante el registro de contadores de [bucles](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (solo los registros constantes se podían indexar en versiones anteriores).

Debe declarar los registros de entrada y salida antes de indexarlos. Sin embargo, no puede indexar ningún registro de salida que se haya declarado con una semántica de posición o tamaño de punto. De hecho, si se usa la indexación, la semántica de la posición y el tamaño psize deben declararse en los registros o0 y o1, respectivamente.

Solo puede indexar un intervalo continuo de registros. es decir, no se puede indexar entre registros que no se han declarado. Aunque esta restricción puede ser inconveniente, permite que se lleve a cabo la optimización del hardware. Si se intenta indexar entre registros no contiguos, se producirán resultados no definidos. La validación del sombreador no aplica esta restricción.

### <a name="simplify-output-registers"></a>Simplificación de los registros de salida

Todos los distintos tipos de registros de salida se han contraído en doce registros de salida: 1 para la posición, 2 para el color, 8 para la textura y 1 para el tamaño de punto o de color. Estos registros interpolarán los datos que contengan para el sombreador de píxeles. Las declaraciones de registro de salida son necesarias y la semántica se asigna a cada registro.

Los registros se pueden desglosar de la siguiente manera:

-   Al menos un registro debe declararse como un registro de posición de cuatro componentes. Este es el único registro de sombreador de vértices necesario.
-   Los diez primeros registros consumidos por un sombreador pueden usar hasta cuatro componentes (xyzw) como máximo.
-   El último registro (o duodécimo) solo puede contener un valor escalar (como el tamaño de punto).

Para obtener una lista de los registros, vea [Registros- frente \_ a \_ 3 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md).

### <a name="texture-sample-in-a-vertex-shader"></a>Muestra de textura en un sombreador de vértices

El sombreador de \_ vértices 3 0 admite la búsqueda de textura en el sombreador de vértices [mediante texldl - frente a](texldl---vs.md).

## <a name="pixel-shader-model-3-features"></a>Características del modelo 3 del sombreador de píxeles

El color del sombreador de píxeles y los registros de textura se han contraído en diez registros de entrada (vea [Input Register Types](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)). Face Register es un registro escalar de punto flotante. Solo el signo de este registro es válido. Si el signo es negativo, la primitiva es una cara posterior. Esto se puede usar dentro de un sombreador de píxeles para lograr una iluminación de dos lados, por ejemplo. El registro de posición hace referencia a los píxeles actuales (x,y).

Los registros constantes del sombreador se pueden establecer mediante:

-   [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb)
-   [**SetPixelShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti)
-   [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf)

## <a name="match-semantics-on-vs_3_0-and-ps_3_0-shaders"></a>Semántica de coincidencias en \_ sombreadores frente a 3 \_ 0 y ps \_ \_ 3 0

Hay algunas restricciones en el uso semántico con frente \_ a 3 \_ 0 y ps \_ 3 \_ 0. En general, debe tener cuidado al usar una semántica para una entrada de sombreador que coincida con una semántica usada en una salida del sombreador.

Por ejemplo, este sombreador de píxeles empaqueta varios nombres en un solo registro:


```
ps_3_0 
dcl_texcoord0 v0.x 
dcl_texcoord1 v0.yz // Valid to pack multiple names into one register 
dcl_texcoord2_centroid v1.w
...
```



Cada registro tiene una semántica diferente. Tenga en cuenta que también puede nombrar v0.x y v0.yz con una semántica diferente (varias) debido al uso de la máscara de escritura.

Dado el sombreador de píxeles, el siguiente sombreador frente \_ a 3 0 no se puede \_ emparejar con él:


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o6.yzw 
...
```



Estos dos sombreadores están en conflicto con su uso de la semántica [**D3DDECLUSAGE \_ TEXCOORD0**](/windows/desktop/direct3d9/d3ddeclusage) y **D3DDECLUSAGE \_ TEXCOORD1.**

Vuelva a escribir el sombreador de vértices de esta forma para evitar la colisión semántica:


```
vs_3_0 
... 
dcl_texcoord2 o3 
dcl_texcoord3 o9 
...
```



Del mismo modo, un nombre semántico declarado en distintos registros de entrada en el sombreador de píxeles (v0 y v1 en el sombreador de píxeles) no se puede usar en un único registro de salida en este sombreador de vértices. Por ejemplo, este sombreador de vértices no se puede emparejar con el sombreador de píxeles porque D3DDECLUSAGE TEXCOORD1 se usa para los registros de entrada del sombreador de píxeles (v0, v1) y el registro de salida del sombreador de \_ vértices o3.


```
vs_3_0 
... 
dcl_texcoord0 o3.x 
dcl_texcoord1 o3.yz 

dcl_texcoord2 o3.w // BAD! Would be valid if this were not o3 
dcl_texcoord3 o9 ... 
```



Por otro lado, este sombreador de vértices no se puede emparejar con el sombreador de píxeles porque la máscara de salida de un parámetro con una semántica determinada no proporciona los datos solicitados por el sombreador de píxeles:


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



## <a name="fog-depth-and-shading-mode-changes"></a>Cambios en el modo de sombreado, profundidad y profundidad

Cuando D3DRS SHADEMODE se establece para sombreado plano durante el recorte y la rasterización de triángulos, los atributos con \_ color D3DDECLUSAGE se interpolan como \_ sombreado plano. Si algún componente de un registro se declara con una semántica de color, pero a otros componentes del mismo registro se les da una semántica diferente, la interpolación de sombreado plano (lineal frente a plana) no se definirá en los componentes de ese registro sin una semántica de color.

Si se desea la representación en forma de nube, frente a \_ 3 \_ 0 y ps \_ 3 \_ 0, los sombreadores deben implementar el sombreador. No se realizan cálculos de cálculo fuera de los sombreadores. No hay ningún registro en comparación con 3 0, y se han agregado semánticas adicionales D3DDECLUSAGE PHP (para el factor de fusión calculado por vértice) y \_ \_ \_ D3DDECLUSAGE \_ DEPTH (para pasar un valor de profundidad al sombreador de píxeles para calcular el factor de fusión).

El estado de la fase de textura D3DTSS \_ TEXCOORDINDEX se omite cuando se usa el sombreador de píxeles 3.0.

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

Las matemáticas de punto flotante se produce con diferentes precisións e intervalos (16 bits, 24 y 32 bits) en diferentes partes de la canalización. Un valor mayor que el intervalo dinámico de la canalización que entra en esa canalización (por ejemplo, un mapa de textura float de 32 bits se muestrea en una canalización float de 24 bits en ps 2 0) crea un resultado \_ indefinido. \_ Para un comportamiento predecible, debe fijar este valor al máximo del intervalo dinámico.

La conversión de un valor de punto flotante a un entero se produce en varios lugares, como:

-   Al encontrar una [mova : vs](mova---vs.md) instrucción.
-   Durante el direccionamiento de textura.
-   Al escribir en un destino de representación de punto no flotante.

## <a name="specifying-full-or-partial-precision"></a>Especificar precisión completa o parcial

Tanto ps \_ 3 \_ 0 como ps \_ 2 \_ x proporcionan compatibilidad con dos niveles de precisión:



| ps \_ 3 \_ 0 | ps \_ 2 \_ 0 | Precisión         | Value                |
|----------|----------|-------------------|----------------------|
| x        |          | Completo              | fp32 o superior       |
| x        |          | Precisión parcial | fp16=s10e5           |
| x        | x        | Completo              | fp24=s16e7 o superior |
| x        | x        | Precisión parcial | fp16=s10e5           |



 

ps \_ 3 \_ 0 admite más precisión que ps \_ 2 \_ 0. De forma predeterminada, todas las operaciones se producen en el nivel de precisión completa.

La precisión parcial (vea [Modificadores de](dx9-graphics-reference-asm-ps-registers-modifiers.md)registro del sombreador de píxeles) se solicita agregando el modificador pp al código del sombreador (siempre que la \_ implementación subyacente lo admita). Las implementaciones siempre son libres de omitir el modificador y realizar las operaciones afectadas con precisión completa.

El \_ modificador pp puede producirse en dos contextos:

-   En una declaración de coordenada de textura para pasar coordenadas de textura de precisión parcial al sombreador de píxeles. Esto se puede usar cuando la textura coordina los datos de color de retransmisión al sombreador de píxeles, que puede ser más rápido con precisión parcial que con precisión completa en algunas implementaciones.
-   En cualquier instrucción para solicitar el uso de precisión parcial, incluidas las instrucciones de carga de textura. Esto indica que la implementación puede ejecutar la instrucción con precisión parcial y almacenar un resultado de precisión parcial. En ausencia de un modificador explícito, la instrucción debe realizarse con precisión completa (independientemente de la precisión de los operandos de entrada).

Una aplicación podría elegir deliberadamente cambiar la precisión por el rendimiento. Hay varios tipos de datos de entrada de sombreador que son candidatos naturales para el procesamiento de precisión parcial:

-   Los iteradores de color están bien representados por valores de precisión parcial.
-   Los valores de textura de la mayoría de los formatos se pueden representar con precisión mediante valores de precisión parcial (los valores muestreados de texturas de formato de punto flotante de 32 bits son una excepción obvia).
-   Las constantes se pueden representar mediante una representación de precisión parcial según corresponda para el sombreador.

En todos estos casos, el desarrollador puede optar por especificar una precisión parcial para procesar los datos, sabiendo que no se pierde ninguna precisión de datos de entrada. En algunos casos, un sombreador puede requerir que los pasos internos de un cálculo se realicen con precisión completa, incluso cuando los valores de entrada y salida final no tengan más de precisión parcial.

## <a name="software-vertex-and-pixel-shaders"></a>Sombreadores de vértices y píxeles de software

Las implementaciones de software (en tiempo de ejecución y referencia para sombreadores de vértices y referencia para sombreadores de píxeles) de los sombreadores de la versión 2 0 y posteriores tienen cierta validación \_ relajada. Esto es útil para fines de depuración y creación de prototipos. La aplicación indica al runtime o ensamblador que necesita parte de la validación relajada mediante la marca sw en el \_ ensamblador (por ejemplo, frente a \_ 2 \_ sw). Un sombreador de software no funcionará con hardware.

vs 2 sw es una relajación a los límites máximos de frente a 2 x; de forma similar, ps 2 sw es una relajación hasta los \_ \_ límites máximos de ps \_ \_ \_ \_ \_ 2 \_ x. En concreto, las validaciones siguientes son relajadas:



| Modelo de sombreador                                           |  Recurso                                    |  Límite                                                                                                                                  |
|--------------------------------------------|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| vs \_ 2 \_ sw, vs \_ 3 \_ sw, ps \_ 2 \_ sw, ps \_ 3 \_ sw | Recuentos de instrucciones                   | Sin límite                                                                                                                         |
| vs \_ 2 \_ sw, vs \_ 3 \_ sw, ps \_ 2 \_ sw, ps \_ 3 \_ sw | Registros de constantes float             | 8192                                                                                                                              |
| vs \_ 2 \_ sw, vs \_ 3 \_ sw, ps \_ 2 \_ sw, ps \_ 3 \_ sw | Registros constantes enteros           | 2048                                                                                                                              |
| vs \_ 2 \_ sw, vs \_ 3 \_ sw, ps \_ 2 \_ sw, ps \_ 3 \_ sw | Registros de constantes booleanos           | 2048                                                                                                                              |
| ps \_ 2 \_ sw                                  | Profundidad de lectura dependiente                 | Sin límite                                                                                                                         |
| vs \_ 2 \_ sw                                  | etiquetas y instrucciones de control de flujo | Sin límite                                                                                                                         |
| vs \_ 2 \_ sw, vs \_ 3 \_ sw, ps \_ 2 \_ sw, ps \_ 3 \_ sw | Inicio,paso/recuentos de bucles               | El tamaño del paso de inicio e iteración de iteración para las instrucciones de repetición y bucle son enteros de 32 bits con signo. El recuento puede ser de hasta MAX \_ INT/64. |
| vs \_ 2 \_ sw, vs \_ 3 \_ sw, ps \_ 2 \_ sw, ps \_ 3 \_ sw | Límites de puerto                          | Los límites de puerto para todos los archivos de registro son relajadas.                                                                                   |
| vs \_ 3 \_ sw                                  | Número de interpoladores              | 16 registros de salida en vs \_ 3 \_ sw.                                                                                                 |
| ps \_ 3 \_ sw                                  | Número de interpoladores              | 14 (16-2) registros de entrada para ps \_ 3 \_ sw.                                                                                           |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)
</dt> </dl>

 

 
