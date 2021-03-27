---
title: Sintaxis de variables
description: Use las siguientes reglas de sintaxis para declarar variables de HLSL.
ms.assetid: 684c42d1-2dd4-42e1-9cff-580edb5c6bcd
keywords:
- extern, sintaxis de variables (DirectX HLSL)
- nointerpolación, sintaxis de variables (DirectX HLSL)
- Sintaxis de variables compartidas (DirectX HLSL)
- groupshared, sintaxis de variables (DirectX HLSL)
- Sintaxis de variables estáticas (DirectX HLSL)
- Sintaxis de variables uniformes (DirectX HLSL)
- Sintaxis volátil y variable (DirectX HLSL)
- Sintaxis de variables precisa (DirectX HLSL)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f6e63bafa62a9857af678e0848c81237dcd0d585
ms.sourcegitcommit: 4e0bde7dfa48a0b60bca4a5230eb2b05be3778d3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/11/2020
ms.locfileid: "104997189"
---
# <a name="variable-syntax"></a>Sintaxis de variables

Use las siguientes reglas de sintaxis para declarar variables de HLSL.



|                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[*Almacenamiento \_ de* Type ( \] \[ *\_ modificador de tipo* de clase) \]  \[ *index* \] \[ *: Semantic* \] \[ *: Packoffset* \] \[ *: Register* \] ;    \[  \] Anotaciones \[ *= Inicial \_ Valor* de                    \] |



 

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="Storage_Class_"></span><span id="storage_class_"></span><span id="STORAGE_CLASS_"></span>*Clase de almacenamiento \_* 
</dt> <dd>

Modificadores de clase de almacenamiento opcionales que proporcionan sugerencias al compilador sobre el ámbito y la duración de las variables. los modificadores se pueden especificar en cualquier orden.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Value</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>extern</strong></td>
<td>Marque una variable global como entrada externa al sombreador; Este es el marcado predeterminado para todas las variables globales. No se puede combinar con <strong>static</strong>.</td>
</tr>
<tr class="even">
<td><strong>nointerpolación</strong></td>
<td>No interpole las salidas de un sombreador de vértices antes de pasarlas a un sombreador de píxeles.</td>
</tr>
<tr class="odd">
<td><strong>cifras</strong></td>
<td>La palabra clave <strong>precisa</strong> cuando se aplica a una variable restringirá los cálculos utilizados para generar el valor asignado a esa variable de las siguientes maneras:

*   Las operaciones independientes se mantienen separadas. Por ejemplo, en los casos en los que una operación Mul y Add se ha fusionado en una operación de Mad, <strong>precisa</strong> obliga a las operaciones a permanecer separadas. En su lugar, debe utilizar explícitamente la función intrínseca Mad.
*   Se mantiene el orden de las operaciones. Cuando el orden de las instrucciones podría haberse aleatorio para mejorar el rendimiento, es <strong>preciso</strong> asegurarse de que el compilador conserva el orden como escrito.
*   Las operaciones IEEE no seguras están restringidas. En los casos en los que el compilador podría haber usado operaciones matemáticas rápidas que no tienen en cuenta los valores NaN (no un número) e INF (infinito <strong>), se</strong> deben respetar los requisitos de IEEE relativos a los valores Nan y INF. Sin <strong>precisión</strong>, estas optimizaciones y operaciones matemáticas no son seguras para IEEE.
*   La calificación de una variable <strong>precisa</strong> no hace que las operaciones que usan la variable sean <strong>precisas</strong>. Dado que <strong>precise</strong> se propaga solo a las operaciones que contribuyen a los valores que se asignan a la variable calificada con <strong>precisión</strong>, el hecho de que los cálculos deseados sean <strong>precisos</strong> puede ser complicado, por lo que se recomienda marcar <strong>las salidas del</strong> sombreador exactamente donde se declaran, ya sea en un campo de estructura o en un parámetro de salida, o en el tipo de valor

La capacidad de controlar las optimizaciones de este modo mantiene la inestabilidad de resultados para la variable de salida modificada al deshabilitar las optimizaciones que pueden afectar a los resultados finales debido a las diferencias en las diferencias de precisión acumuladas. Resulta útil cuando se desea que los sombreadores de teselación mantengan coincidencias de parches con agua apretada o valores de profundidad de coincidencia en varias fases.

[Código de ejemplo](https://github.com/microsoft/DirectXShaderCompiler/blob/master/tools/clang/test/HLSLFileCheck/hlsl/types/modifiers/precise/precise4.hlsl): 
```HLSL
matrix g_mWorldViewProjection;
void main(in float3 InPos : Position, out precise float4 OutPos : SV_Position)
{
  // operation is precise because it contributes to the precise parameter OutPos
  OutPos = mul( float4( InPos, 1.0 ), g_mWorldViewProjection );
}
```
</td>
</tr>
<tr class="even">
<td><strong>recurso</strong></td>
<td>Marcar una variable para compartir entre efectos; Esta es una sugerencia para el compilador.</td>
</tr>
<tr class="odd">
<td><strong>groupshared</strong></td>
<td>Marque una variable para la memoria compartida por el grupo de subprocesos para los sombreadores de cálculo. En D3D10, el tamaño total máximo de todas las variables con la clase de almacenamiento groupshared es 16 KB, en D3D11 el tamaño máximo es 32 KB. Vea los ejemplos.</td>
</tr>
<tr class="even">
<td><strong>static</strong></td>
<td>Marque una variable local para que se inicialice una vez y se conserve entre las llamadas de función. Si la declaración no incluye un inicializador, el valor se establece en cero. Una variable global marcada como <strong>static</strong> no es visible para una aplicación.</td>
</tr>
<tr class="odd">
<td><strong>uniforme</strong></td>
<td>Marque una variable cuyos datos sean constantes a lo largo de la ejecución de un sombreador (por ejemplo, un color material en un sombreador de vértices). de forma predeterminada, las variables globales se consideran <strong>uniformes</strong> .</td>
</tr>
<tr class="even">
<td><strong>volatile</strong></td>
<td>Marque una variable que cambie con frecuencia; Esta es una sugerencia para el compilador. Este modificador de clase de almacenamiento solo se aplica a una variable local.<br/>
<blockquote>
[!Note]<br />
El compilador de HLSL actualmente omite este modificador de clase de almacenamiento.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span id="Type_Modifier"></span><span id="type_modifier"></span><span id="TYPE_MODIFIER"></span>*\_Modificador de tipo*
</dt> <dd>

Modificador de tipo variable opcional.



| Value             | Descripción                                                                                                                                                                                                                                  |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **const**         | Marque una variable que un sombreador no pueda cambiar; por lo tanto, debe inicializarse en la declaración de la variable. Las variables globales se consideran **const** de forma predeterminada (suprima este comportamiento mediante la especificación de la marca/GEC en el compilador). |
| **fila \_ principal**    | Marque una variable que almacene cuatro componentes en una sola fila para que puedan almacenarse en un solo registro de constante.                                                                                                                             |
| **columna \_ principal** | Marque una variable que almacene 4 componentes en una sola columna para optimizar la aritmética de la matriz.                                                                                                                                                         |



 

> [!Note]  
> Si no se especifica un valor de modificador de tipo, el compilador utiliza la **columna \_ major** como valor predeterminado.

 

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>*Automáticamente*
</dt> <dd>

Cualquier tipo HLSL mostrado en [tipos de datos (DirectX HLSL)](dx-graphics-hlsl-data-types.md).

</dd> <dt>

<span id="Name_Index_"></span><span id="name_index_"></span><span id="NAME_INDEX_"></span>*Nombre* \[ de *Índice* de\]
</dt> <dd>

Cadena ASCII que identifica de forma única una variable de sombreador. Para definir una matriz opcional, utilice **index** para el tamaño de la matriz, que es un entero positivo = 1.

</dd> <dt>

<span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Semántica*
</dt> <dd>

Información de uso de parámetros opcional utilizada por el compilador para vincular entradas y salidas del sombreador. Hay varias [semánticas](dx-graphics-hlsl-semantics.md) predefinidas para los sombreadores de vértices y píxeles. El compilador omite la semántica a menos que se declaren en una variable global o un parámetro pasado a un sombreador.

</dd> <dt>

<span id="Packoffset"></span><span id="packoffset"></span><span id="PACKOFFSET"></span>*Packoffset*
</dt> <dd>

Palabra clave opcional para empaquetar manualmente las constantes de sombreador. Consulte [packoffset (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md).

</dd> <dt>

<span id="Register"></span><span id="register"></span><span id="REGISTER"></span>*El*
</dt> <dd>

Palabra clave opcional para asignar manualmente una variable de sombreador a un registro determinado. Consulte [Register (DirectX HLSL)](dx-graphics-hlsl-variable-register.md).

</dd> <dt>

<span id="Annotation_s_"></span><span id="annotation_s_"></span><span id="ANNOTATION_S_"></span>*Anotación (s)*
</dt> <dd>

Metadatos opcionales, en forma de cadena, adjuntos a una variable global. El marco de trabajo usa una anotación y la omite HLSL. para ver una sintaxis más detallada, vea [Sintaxis de anotación](/windows/desktop/direct3d10/d3d10-effect-annotation-syntax).

</dd> <dt>

<span id="Initial_Value"></span><span id="initial_value"></span><span id="INITIAL_VALUE"></span>*\_Valor inicial*
</dt> <dd>

Valores iniciales opcionales; el número de valores debe coincidir con el número de componentes de *tipo*. Cada variable global marcada como **extern** debe inicializarse con un valor literal; cada variable marcada como **static** debe inicializarse con una constante.

Las variables globales que no están marcadas como **static** o **extern** no se compilan en el sombreador. El compilador no establece automáticamente los valores predeterminados para las variables globales y no puede utilizarlos en las optimizaciones. Para inicializar este tipo de variable global, utilice la reflexión para obtener su valor y, a continuación, copie el valor en un búfer de constantes. Por ejemplo, puede usar el método [**ID3D11ShaderReflection:: GetVariableByName**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname) para obtener la variable, usar el método [**ID3D11ShaderReflectionVariable:: GetDesc**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getdesc) para obtener la descripción de la variable de sombreador y obtener el valor inicial del miembro **DefaultValue** de la estructura de la [**\_ \_ variable de \_ sombreador D3D11**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_shader_variable_desc) . Para copiar el valor en el búfer de constantes, debe asegurarse de que el búfer se creó con acceso de escritura de CPU ([**D3D11 de \_ acceso de CPU \_ \_**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_cpu_access_flag)). Para obtener más información sobre cómo crear un búfer de constantes, vea [Cómo: crear un búfer de constantes](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to).

También puede usar el [marco de trabajo de efectos](../direct3d11/d3d11-graphics-programming-guide-effects.md) para procesar automáticamente el reflejo y establecer el valor inicial. Por ejemplo, puede usar el método [**ID3DX11EffectPass:: Apply**](/windows/desktop/direct3d11/id3dx11effectpass-apply) .

</dd> </dl>

## <a name="examples"></a>Ejemplos

Estos son algunos ejemplos de declaraciones de variables de sombreador.


```
float fVar;
```




```
float4 color;
float fVar = 3.1f;

int iVar[3];

int iVar[3] = {1,2,3};

uniform float4 position : SV_POSITION; 
const float4 lightDirection = {0,0,1};
      
```



### <a name="group-shared"></a>Grupo compartido

HLSL permite a los subprocesos de un sombreador de cálculo intercambiar valores a través de la memoria compartida. HLSL proporciona primitivas de barrera como [**GroupMemoryBarrierWithGroupSync**](groupmemorybarrierwithgroupsync.md), y así sucesivamente para garantizar el orden correcto de las lecturas y escrituras en la memoria compartida del sombreador y para evitar carreras de datos.

> [!Note]  
> El hardware ejecuta subprocesos en grupos (alabeos o frontales) y la sincronización de barrera a veces se puede omitir para aumentar el rendimiento cuando solo se sincronizan los subprocesos que pertenecen al mismo grupo. Pero se desaconseja encarecidamente esta omisión por estos motivos:
>
> -   Esta omisión produce código no portable, que podría no funcionar en algún hardware y no funciona en rasterizadores de software que normalmente ejecutan subprocesos en grupos más pequeños.
> -   Las mejoras de rendimiento que puede lograr con esta omisión serán menores en comparación con el uso de la barrera de todos los subprocesos.

 

En Direct3D 10 no hay ninguna sincronización de subprocesos al escribir en **groupshared**, por lo que cada subproceso se limita a una única ubicación en una matriz para su escritura. Use el valor del sistema [VP \_ GroupIndex](dx-graphics-hlsl-semantics.md) para indexar en esta matriz al escribir para asegurarse de que no haya dos subprocesos que puedan entrar en conflicto. En cuanto a la lectura, todos los subprocesos tienen acceso a toda la matriz para su lectura.


```
struct GSData
{
    float4 Color;
    float Factor;
}

groupshared GSData data[5*5*1];

[numthreads(5,5,1)]
void main( uint index : SV_GroupIndex )
{
    data[index].Color = (float4)0;
    data[index].Factor = 2.0f;
    GroupMemoryBarrierWithGroupSync();
    ...
}
```



### <a name="packing"></a>Envase

Empaquete subcomponentes de vectores y escalares cuyo tamaño sea lo suficientemente grande como para evitar límites de registro de cruce. Por ejemplo, todos son válidos:


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c1);
    float1 Element3 : packoffset(c1.y);
}
        
```



No se pueden mezclar tipos de empaquetado.

Al igual que la palabra clave Register, un packoffset puede ser específico del destino. El empaquetado de subcomponentes solo está disponible con la palabra clave packoffset, no con la palabra clave Register. Dentro de una declaración de CBuffer, la palabra clave Register se omite para los destinos de Direct3D 10, ya que se supone que es para la compatibilidad entre plataformas.

Los elementos empaquetados se pueden superponer y el compilador no proporcionará ningún error o advertencia. En este ejemplo, Elemento2 y Element3 se superpondrán con Element1. x y Element1. y.


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c0);
    float1 Element3 : packoffset(c0.y);
}
        
```



Un ejemplo que usa packoffset es: [HLSLWithoutFX10 Sample](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Variables (DirectX HLSL)](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

