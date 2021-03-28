---
title: Argumentos de la función
description: Una función toma uno o más argumentos de entrada; Use la siguiente sintaxis para declarar cada argumento.
ms.assetid: 80e0dbc8-26b7-4250-bb01-6856fc70f6b8
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3ba35ad04b20b67e45550644e842d69209ca5088
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/11/2020
ms.locfileid: "104420190"
---
# <a name="function-arguments"></a>Argumentos de la función

Una función toma uno o más argumentos de entrada; Use la siguiente sintaxis para declarar cada argumento.



|                                                                                             |
|---------------------------------------------------------------------------------------------|
| **\[InputModifier \] nombre de tipo \[ : semántico \] \[ InterpolationModifier \] \[ = inicializadores\]** |



 

\[Nombre de tipo de modificador \] \[ : semántico \] \[ : modificador de interpolación \] \[ = inicializadores\]

Si hay varios argumentos de función, se separan mediante comas.

## <a name="parameters"></a>Parámetros



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Elemento</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="InputModifier"></span><span id="inputmodifier"></span><span id="INPUTMODIFIER"></span><strong>InputModifier</strong><br/></td>
<td>Término opcional que identifica un argumento como una entrada, una salida o ambas cosas.<br/> 
<table>
<tbody>
<tr class="odd">
<td>Value</td>
<td>Descripción</td>
</tr>
<tr class="even">
<td><strong>in</strong></td>
<td>Solo entrada</td>
</tr>
<tr class="odd">
<td><strong>Inout</strong></td>
<td>Entrada y salida</td>
</tr>
<tr class="even">
<td><strong>out</strong></td>
<td>Solo salida</td>
</tr>
<tr class="odd">
<td><strong>uniforme</strong></td>
<td>Datos constantes de solo entrada</td>
</tr>
</tbody>
</table>

<p> </p>
<p>Los parámetros siempre se pasan por valor. en indica que el valor del parámetro se debe copiar en desde la aplicación que realiza la llamada antes de que comience la función. out indica que el último valor del parámetro debe copiarse y devolverse a la aplicación que realiza la llamada cuando la función devuelve. Inout es una abreviatura para especificar ambos.</p>
<p>Un valor uniforme procede de un registro constante; cada sombreador de vértices o invocación del sombreador de píxeles verá el mismo valor inicial para una variable uniforme. Las variables globales se tratan como si se declararan uniformes. En el caso de las funciones que no son de nivel superior, Uniform es sinónimo de <strong>en</strong>. Si no se especifica ningún uso de parámetro, se supone que el uso del parámetro está <strong>en</strong>.</p></td>
</tr>
<tr class="even">
<td><p><span id="Type"></span><span id="type"></span><span id="TYPE"></span><strong>Automáticamente</strong></p></td>
<td><p>El tipo de argumento; puede ser cualquier <a href="dx-graphics-hlsl-data-types.md">tipo</a>HLSL válido.</p></td>
</tr>
<tr class="odd">
<td><p><span id="Name"></span><span id="name"></span><span id="NAME"></span><strong>Name</strong></p></td>
<td><p>Cadena ASCII que identifica de forma única el nombre de la función de sombreador.</p></td>
</tr>
<tr class="even">
<td><p><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span><strong>Semántica</strong></p></td>
<td><p>Cadena opcional que identifica el uso previsto de los datos (vea <a href="dx-graphics-hlsl-semantics.md">semántica (DirectX HLSL)</a>).</p></td>
</tr>
<tr class="odd">
<td><p><span id="InterpolationModifier"></span><span id="interpolationmodifier"></span><span id="INTERPOLATIONMODIFIER"></span><strong>InterpolationModifier</strong></p></td>
<td><p><a href="dx-graphics-hlsl-struct.md">Modificador de interpolación</a> opcional que permite a un sombreador determinar el método de interpolación. Un modificador de interpolación en un argumento de función solo se aplica a un argumento que se usa como entrada para una función de sombreador de píxeles.</p></td>
</tr>
<tr class="even">
<td><p><span id="Initializers"></span><span id="initializers"></span><span id="INITIALIZERS"></span><strong>Inicializadores</strong></p></td>
<td><p>Valores opcionales para la inicialización; se requieren varios valores para inicializar los tipos de datos de varios componentes.</p></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Observaciones

Los argumentos de función se enumeran en una lista de argumentos separados por comas en una declaración de función. Como en las funciones de C, cada argumento debe tener un nombre de parámetro y un tipo declarados; un argumento para una función HLSL puede incluir opcionalmente una semántica, un valor inicial y una entrada de sombreador de píxeles puede incluir un tipo de interpolación.

El *tipo* de un argumento de función puede ser una estructura, que podría incluir un modificador de interpolación por miembro. Si el argumento de función también tiene un modificador de interpolación, el modificador de argumento de función reemplaza los modificadores de interpolación declarados en el tipo.

## <a name="examples"></a>Ejemplos

En este ejemplo (del [ejemplo BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)) se muestran entradas uniformes y no uniformes para una función de sombreador de vértices.


```
VS_OUTPUT RenderSceneVS( 
  float4 vPos : POSITION,
  float3 vNormal : NORMAL,
  float2 vTexCoord0 : TEXCOORD,
  uniform int nNumLights,
  uniform bool bTexture,
  uniform bool bAnimate )
{
  ...
}
```



Este ejemplo (del [ejemplo ContentStreaming](https://msdn.microsoft.com/library/Ee416397(v=VS.85).aspx)) utiliza una estructura de entrada para pasar argumentos a una función de sombreador de píxeles.


```
VSBasicIn input
struct VSBasicIn
{
  float4 Pos    : POSITION;
  float3 Norm   : NORMAL;
  float2 Tex    : TEXCOORD0;
};

PSBasicIn VSBasic(VSBasicIn input)
{
  ...
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Funciones (DirectX HLSL)](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 





