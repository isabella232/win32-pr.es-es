---
title: Sintaxis de variables
description: Use las siguientes reglas de sintaxis para declarar variables HLSL.
ms.assetid: 684c42d1-2dd4-42e1-9cff-580edb5c6bcd
keywords:
- extern, sintaxis de variables (DirectX HLSL)
- nointerpolation, sintaxis de variables (DirectX HLSL)
- shared, Sintaxis de variable (HlsL de DirectX)
- groupshared, sintaxis de variables (DirectX HLSL)
- static, sintaxis de variables (HLSL de DirectX)
- uniforme, sintaxis de variables (Hlsl de DirectX)
- volatile, sintaxis de variables (HLSL de DirectX)
- precisa, sintaxis variable (HLSL de DirectX)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0ce89287d969683b72eb6db6d352300ce5295852
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127573756"
---
# <a name="variable-syntax"></a>Sintaxis de variables

Use las siguientes reglas de sintaxis para declarar variables HLSL.

\[*Storage \_ Class* \] \[ *Type \_ Modifier* \] *Type Name* \[ *Index* \] \[ *: Semantic*: \] \[ *Packoffset*: \] \[ *Register* \] ;    \[  \] Anotaciones \[ *= Inicial \_ Valor*                    \]



 

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="Storage_Class_"></span><span id="storage_class_"></span><span id="STORAGE_CLASS_"></span>*\_Storage Clase* 
</dt> <dd>

Modificadores opcionales de clase de almacenamiento que dan al compilador sugerencias sobre el ámbito y la duración de las variables; los modificadores se pueden especificar en cualquier orden.




| Value | Descripción | 
|-------|-------------|
| <strong>extern</strong> | Marcar una variable global como entrada externa al sombreador; este es el marcado predeterminado para todas las variables globales. No se puede combinar con <strong>estáticos.</strong> | 
| <strong>nointerpolation</strong> | No interpola las salidas de un sombreador de vértices antes de pasarlas a un sombreador de píxeles. | 
| <strong>Precisa</strong> | La <strong>palabra</strong> clave precisa cuando se aplica a una variable restringirá los cálculos usados para generar el valor asignado a esa variable de las maneras siguientes:* Las operaciones independientes se mantienen independientes. Por ejemplo, cuando una operación de suma y mulas se podría haber fusionado en una operación <strong>loca,</strong> la precisión obliga a que las operaciones permanezcan independientes. En su lugar, debe usar explícitamente la función intrínseca loca.* Se mantiene el orden de las operaciones. Cuando el orden de las instrucciones podría haber sido aleatorio para mejorar el <strong>rendimiento,</strong> con precisión se garantiza que el compilador conserva el orden tal y como se ha escrito.* Las operaciones no seguras de IEEE están restringidas. Cuando el compilador podría haber usado operaciones matemáticas rápidas que no tienen en cuenta <strong></strong> los valores NaN (no un número) e INF (infinito), la precisión obliga a respetar los requisitos ieee relativos a los valores NaN e INF. Sin <strong>precisión,</strong>estas optimizaciones y operaciones matemáticas no son seguras para IEEE.* Calificar una <strong>variable</strong> precisa no hace que las operaciones que usan la variable sean <strong>precisas.</strong> Dado <strong></strong> que la precisión se propaga solo a las <strong></strong>operaciones que contribuyen a los valores asignados a la variable precisa, hacer correctamente los <strong>cálculos</strong> deseados con precisión puede ser complicado, por lo que se recomienda marcar las <strong>salidas</strong> del sombreador directamente donde se declaran, ya sea en un campo de estructura, en un parámetro de salida o en el tipo de valor devuelto de la función de entrada. La capacidad de controlar las optimizaciones de esta manera mantiene la invariable de resultados para la variable de salida modificada deshabilitando las optimizaciones que podrían afectar a los resultados finales debido a diferencias en las diferencias de precisión acumuladas. Es útil cuando se desea que los sombreadores para teselación mantengan las juntas de revisión estrechas o coincidan con los valores de profundidad en varios pases. [Código de ejemplo:](https://github.com/microsoft/DirectXShaderCompiler/blob/master/tools/clang/test/HLSLFileCheck/hlsl/types/modifiers/precise/precise4.hlsl)```HLSLmatrix g_mWorldViewProjection;void main(in float3 InPos : Position, out precise float4 OutPos : SV_Position){  // operation is precise because it contributes to the precise parameter OutPos  OutPos = mul( float4( InPos, 1.0 ), g_mWorldViewProjection );}``` | 
| <strong>Compartido</strong> | Marcar una variable para compartir entre efectos; se trata de una sugerencia para el compilador. | 
| <strong>groupshared</strong> | Marque una variable para la memoria compartida de grupo de subprocesos para sombreadores de proceso. En D3D10, el tamaño total máximo de todas las variables con la clase de almacenamiento groupshared es de 16 kb, en D3D11 el tamaño máximo es de 32 kb. Vea ejemplos. | 
| <strong>static</strong> | Marque una variable local para que se inicialice una vez y persista entre las llamadas de función. Si la declaración no incluye un inicializador, el valor se establece en cero. Una variable global marcada <strong>como estática</strong> no es visible para una aplicación. | 
| <strong>uniforme</strong> | Marcar una variable cuyos datos son constantes durante la ejecución de un sombreador (por ejemplo, un color de material en un sombreador de vértices); Las variables globales se consideran <strong>uniformes</strong> de forma predeterminada. | 
| <strong>volatile</strong> | Marque una variable que cambie con frecuencia; se trata de una sugerencia para el compilador. Este modificador de clase de almacenamiento solo se aplica a una variable local.<br /><blockquote>[!Note]<br />El compilador HLSL omite actualmente este modificador de clase de almacenamiento.</blockquote><br /> | 




 

</dd> <dt>

<span id="Type_Modifier"></span><span id="type_modifier"></span><span id="TYPE_MODIFIER"></span>*Modificador de \_ tipo*
</dt> <dd>

Modificador de tipo variable opcional.



| Value             | Descripción                                                                                                                                                                                                                                  |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **const**         | Marque una variable que un sombreador no pueda cambiar, por lo que debe inicializarse en la declaración de variable. Las variables globales se consideran **const** de forma predeterminada (para suprimir este comportamiento, proporcione la marca /Gec al compilador). |
| **fila \_ principal**    | Marque una variable que almacene cuatro componentes en una sola fila para que se puedan almacenar en un único registro constante.                                                                                                                             |
| **columna \_ principal** | Marque una variable que almacena 4 componentes en una sola columna para optimizar las matemáticas de matriz.                                                                                                                                                         |



 

> [!Note]  
> Si no especifica un valor modificador de tipo, el compilador usa **la columna \_ principal** como valor predeterminado.

 

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>*Tipo*
</dt> <dd>

Cualquier tipo HLSL enumerado en [Tipos de datos (DirectX HLSL)](dx-graphics-hlsl-data-types.md).

</dd> <dt>

<span id="Name_Index_"></span><span id="name_index_"></span><span id="NAME_INDEX_"></span>*Nombre* \[ *Índice*\]
</dt> <dd>

Cadena ASCII que identifica de forma única una variable de sombreador. Para definir una matriz opcional, use **index para** el tamaño de la matriz, que es un entero positivo = 1.

</dd> <dt>

<span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Semántica*
</dt> <dd>

Información opcional sobre el uso de parámetros, que usa el compilador para vincular las entradas y salidas del sombreador. Hay varias semánticas [predefinidas para sombreadores](dx-graphics-hlsl-semantics.md) de vértices y píxeles. El compilador omite la semántica a menos que se declaren en una variable global o un parámetro pasado a un sombreador.

</dd> <dt>

<span id="Packoffset"></span><span id="packoffset"></span><span id="PACKOFFSET"></span>*Packoffset*
</dt> <dd>

Palabra clave opcional para empaquetar manualmente las constantes del sombreador. Consulte [packoffset (DirectX HLSL).](dx-graphics-hlsl-variable-packoffset.md)

</dd> <dt>

<span id="Register"></span><span id="register"></span><span id="REGISTER"></span>*Registro*
</dt> <dd>

Palabra clave opcional para asignar manualmente una variable de sombreador a un registro determinado. Vea [register (DirectX HLSL).](dx-graphics-hlsl-variable-register.md)

</dd> <dt>

<span id="Annotation_s_"></span><span id="annotation_s_"></span><span id="ANNOTATION_S_"></span>*Anotaciones*
</dt> <dd>

Metadatos opcionales, en forma de cadena, asociados a una variable global. La plataforma de efectos usa una anotación y HLSL la omite; Para ver una sintaxis más detallada, vea [sintaxis de anotación](/windows/desktop/direct3d10/d3d10-effect-annotation-syntax).

</dd> <dt>

<span id="Initial_Value"></span><span id="initial_value"></span><span id="INITIAL_VALUE"></span>*Valor \_ inicial*
</dt> <dd>

Valores iniciales opcionales; el número de valores debe coincidir con el número de componentes de *Tipo*. Cada variable global marcada **como extern** debe inicializarse con un valor literal; Cada variable marcada **como estática** debe inicializarse con una constante.

Las variables globales que no están **marcadas como estáticas** o **extern** no se compilan en el sombreador. El compilador no establece automáticamente los valores predeterminados para las variables globales y no puede usarlos en las optimizaciones. Para inicializar este tipo de variable global, use la reflexión para obtener su valor y, a continuación, copie el valor en un búfer constante. Por ejemplo, puede usar el método [**ID3D11ShaderReflection::GetVariableByName**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname) para obtener la variable, usar el método [**ID3D11ShaderReflectionVariable::GetDesc**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getdesc) para obtener la descripción de la variable de sombreador y obtener el valor inicial del miembro **DefaultValue** de la estructura [**\_ \_ \_ DESC DESC DE3D11 SHADER VARIABLE.**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_shader_variable_desc) Para copiar el valor en el búfer constante, debe asegurarse de que el búfer se creó con acceso de escritura de CPU [**(D3D11 \_ CPU \_ ACCESS \_ WRITE**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_cpu_access_flag)). Para obtener más información sobre cómo crear un búfer constante, [vea How to: Create a Constant Buffer](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to).

También puede usar el marco [de efectos](../direct3d11/d3d11-graphics-programming-guide-effects.md) para procesar automáticamente el reflejo y establecer el valor inicial. Por ejemplo, puede usar el [**método ID3DX11EffectPass::Apply.**](/windows/desktop/direct3d11/id3dx11effectpass-apply)

</dd> </dl>

## <a name="examples"></a>Ejemplos

Estos son varios ejemplos de declaraciones de variable de sombreador.


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

HLSL permite a los subprocesos de un sombreador de proceso intercambiar valores a través de la memoria compartida. HLSL proporciona primitivas de barrera como [**GroupMemoryBarradWithGroupSync,**](groupmemorybarrierwithgroupsync.md)y así sucesivamente para garantizar el orden correcto de las lecturas y escrituras en la memoria compartida en el sombreador y evitar carreras de datos.

> [!Note]  
> El hardware ejecuta subprocesos en grupos (deformes o frentes de onda), y la sincronización de barreras a veces se puede omitir para aumentar el rendimiento cuando solo la sincronización de subprocesos que pertenecen al mismo grupo es correcta. Pero se desaconseja esta omisión por estos motivos:
>
> -   Esta omisión da como resultado código no portátil, que podría no funcionar en algún hardware y no funciona en rasterizadores de software que normalmente ejecutan subprocesos en grupos más pequeños.
> -   Las mejoras de rendimiento que podría lograr con esta omisión serán menores en comparación con el uso de la barrera de todos los subprocesos.

 

En Direct3D 10 no hay ninguna sincronización de subprocesos al escribir en **groupshared,** por lo que esto significa que cada subproceso se limita a una sola ubicación en una matriz para escribir. Use el [valor del \_ sistema GroupIndex](dx-graphics-hlsl-semantics.md) de SV para indexar en esta matriz al escribir para asegurarse de que no pueden colisionar dos subprocesos. En términos de lectura, todos los subprocesos tienen acceso a toda la matriz para la lectura.


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



### <a name="packing"></a>Embalaje

Empaquetar subcomponentes de vectores y escalares cuyo tamaño es lo suficientemente grande como para evitar cruzar los límites del registro. Por ejemplo, todos estos son válidos:


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c1);
    float1 Element3 : packoffset(c1.y);
}
        
```



No se pueden mezclar tipos de empaquetado.

Al igual que la palabra clave register, un packoffset puede ser específico del destino. El empaquetado de subcomponentes solo está disponible con la palabra clave packoffset, no con la palabra clave register. Dentro de una declaración de cbuffer, la palabra clave register se omite para los destinos de Direct3D 10, ya que se supone que es para la compatibilidad multiplataforma.

Los elementos empaquetados pueden superponerse y el compilador no producirá ningún error ni advertencia. En este ejemplo, Element2 y Element3 se superponerán con Element1.x y Element1.y.


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

[Variables (HLSL de DirectX)](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

