---
title: Escribir sombreadores HLSL en Direct3D 9
description: Escribir sombreadores HLSL en Direct3D 9
ms.assetid: 7db6b264-c96c-4298-9b8a-d0c488390e4e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 504a1d9ff5a2aa2b37227f0016cdc97d28d967fe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078140"
---
# <a name="writing-hlsl-shaders-in-direct3d-9"></a>Escribir sombreadores HLSL en Direct3D 9

-   [Conceptos básicos del sombreador de vértices](#vertex-shader-basics)
-   [Conceptos básicos del sombreador de píxeles](#pixel-shader-basics)
    -   [Estados de muestra y fase de textura](#texture-stage-and-sampler-states)
    -   [Entradas del sombreador de píxeles](#pixel-shader-inputs)
    -   [Salidas del sombreador de píxeles](#pixel-shader-outputs)
-   [Entradas de sombreador y variables de sombreador](#shader-inputs-and-shader-variables)
    -   [Declarar variables de sombreador](#declaring-shader-variables)
    -   [Entradas uniformes del sombreador](#uniform-shader-inputs)
    -   [Variables y semánticas de sombreador variables](#varying-shader-inputs-and-semantics)
    -   [Muestras y objetos de textura](#samplers-and-texture-objects)
-   [Escribir funciones](#writing-functions)
-   [Control de flujo](#flow-control)
-   [Temas relacionados](#related-topics)

## <a name="vertex-shader-basics"></a>Aspectos básicos de Vertex-Shader

Cuando está en funcionamiento, un sombreador de vértices programable reemplaza el procesamiento de vértices realizado por la canalización de gráficos de Microsoft Direct3D. Al usar un sombreador de vértices, la canalización de funciones fijas omite la información de estado relativa a las operaciones de transformación e iluminación. Cuando se deshabilita el sombreador de vértices y se devuelve el procesamiento de funciones fijas, se aplican todos los valores de estado actuales.

La teselación de primitivas de orden superior debe realizarse antes de que se ejecute el sombreador de vértices. Las implementaciones que realizan la teselación superficial después del procesamiento del sombreador deben hacerlo de una manera que no es aparente en el código del sombreador y la aplicación.

Como mínimo, un sombreador de vértices debe generar la posición del vértice en el espacio de recorte homogéneo. Opcionalmente, el sombreador de vértices puede generar coordenadas de textura, color de vértice, iluminación de vértices, factores de niebla, etc.

## <a name="pixel-shader-basics"></a>Aspectos básicos de Pixel-Shader

El procesamiento de píxeles se realiza mediante sombreadores de píxeles en píxeles individuales. Los sombreadores de píxeles funcionan en conjunto con los sombreadores de vértices; la salida de un sombreador de vértices proporciona las entradas para un sombreador de píxeles. Otras operaciones de píxeles (mezcla de niebla, operaciones de estarcido y mezcla de destino de representación) se producen después de la ejecución del sombreador.

### <a name="texture-stage-and-sampler-states"></a>Estados de muestra y fase de textura

Un sombreador de píxeles reemplaza completamente la funcionalidad de combinación de píxeles especificada por el mezclador de varias texturas, incluidas las operaciones definidas previamente por los Estados de la fase de textura. Las operaciones de filtrado y muestreo de textura que se controlan mediante los Estados de fase de textura estándar para minificación, la ampliación, el filtrado de MIP y los modos de direccionamiento de encapsulado se pueden inicializar en sombreadores. La aplicación es gratuita para cambiar estos Estados sin necesidad de la regeneración del sombreador enlazado actualmente. El establecimiento del estado puede ser más fácil si los sombreadores están diseñados dentro de un efecto.

### <a name="pixel-shader-inputs"></a>Entradas del sombreador de píxeles

En el caso de las versiones de sombreador de píxeles PS \_ 1 \_ 1-PS \_ 2 \_ 0, los colores difusos y especulares se saturan (se fijan) en el intervalo de 0 a 1 antes de que los use el sombreador.

Los valores de color especificados para el sombreador de píxeles son correctos para la perspectiva, pero esto no se garantiza (para todo el hardware). Los colores muestreados a partir de coordenadas de textura se repiten de manera correcta y se fijan en el intervalo de 0 a 1 durante la iteración.

### <a name="pixel-shader-outputs"></a>Salidas del sombreador de píxeles

En el caso de las versiones del sombreador de píxeles PS \_ 1 \_ 1-PS \_ 1 \_ 4, el resultado emitido por el sombreador de píxeles es el contenido de Register R0. Lo que contenga cuando el sombreador complete el procesamiento se envía a la fase de niebla y a la mezcla de destino de representación.

En el caso de las versiones de sombreador de píxeles PS \_ 2 \_ 0 y superiores, el color de salida se emite desde OC0-oC4.

## <a name="shader-inputs-and-shader-variables"></a>Entradas de sombreador y variables de sombreador

-   [Declarar variables de sombreador](#declaring-shader-variables)
-   [Entradas uniformes del sombreador](#uniform-shader-inputs)
-   [Variables y semánticas de sombreador variables](#varying-shader-inputs-and-semantics)
-   [Muestras y objetos de textura](#samplers-and-texture-objects)

### <a name="declaring-shader-variables"></a>Declarar variables de sombreador

La declaración de variable más sencilla incluye un tipo y un nombre de variable, como esta declaración de punto flotante:


```
float fVar;
```



Puede inicializar una variable en la misma instrucción.


```
float fVar = 3.1f;
```



Se puede declarar una matriz de variables,


```
int iVar[3];
```



o se declaran e inicializan en la misma instrucción.


```
int iVar[3] = {1,2,3};
```



Estas son algunas declaraciones que muestran muchas de las características de las variables del lenguaje de sombreado de alto nivel (HLSL):


```
float4 color;
uniform float4 position : POSITION; 
const float4 lightDirection = {0,0,1};
```



Las declaraciones de datos pueden usar cualquier tipo válido, entre los que se incluyen:

-   [Tipos de datos (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
-   [Tipo de vector (DirectX HLSL)](dx-graphics-hlsl-vector.md)
-   [Tipo de matriz (DirectX HLSL)](dx-graphics-hlsl-matrix.md)
-   [Tipo de sombreador (DirectX HLSL)](dx-graphics-hlsl-shader.md)
-   [Tipo de muestra (DirectX HLSL)](dx-graphics-hlsl-sampler.md)
-   [Tipo definido por el usuario (DirectX HLSL)](dx-graphics-hlsl-user-defined.md)

Un sombreador puede tener variables, argumentos y funciones de nivel superior.


```
// top-level variable
float globalShaderVariable; 

// top-level function
void function(
in float4 position: POSITION0 // top-level argument
              )
{
  float localShaderVariable; // local variable
  function2(...)
}

void function2()
{
  ...
}
```



Las variables de nivel superior se declaran fuera de todas las funciones. Los argumentos de nivel superior son parámetros para una función de nivel superior. Una función de nivel superior es cualquier función a la que llama la aplicación (en lugar de una función a la que llama otra función).

### <a name="uniform-shader-inputs"></a>Entradas uniformes del sombreador

Los sombreadores de vértices y píxeles aceptan dos tipos de datos de entrada: variables y uniformes. La entrada variable son los datos que son únicos para cada ejecución del sombreador. En el caso de un sombreador de vértices, los datos variables (por ejemplo: Position, normal, etc.) proceden de las secuencias de vértices. Los datos uniformes (por ejemplo: color del material, transformación del mundo, etc.) son constantes para varias ejecuciones de un sombreador. Para aquellos que estén familiarizados con los modelos de sombreador de ensamblado, los datos uniformes se especifican mediante registros constantes y datos variables por los registros v y t.

Los datos uniformes pueden especificarse mediante dos métodos. El método más común consiste en declarar las variables globales y usarlas en un sombreador. Cualquier uso de variables globales dentro de un sombreador producirá la adición de esa variable a la lista de variables uniformes que requiere ese sombreador. El segundo método consiste en marcar un parámetro de entrada de la función de sombreador de nivel superior como uniforme. Este marcado especifica que la variable especificada debe agregarse a la lista de variables uniformes.

Las variables uniformes usadas por un sombreador se comunican de nuevo a la aplicación a través de la tabla de constantes. La tabla Constant es el nombre de la tabla de símbolos que define cómo se ajustan las variables uniformes usadas por un sombreador en los registros de constantes. Los parámetros de función uniformes aparecen en la tabla de constantes antepuesto con un signo de dólar ($), a diferencia de las variables globales. El signo de dólar es necesario para evitar colisiones de nombres entre las entradas uniformes locales y las variables globales del mismo nombre.

La tabla Constant contiene las ubicaciones de registro constantes de todas las variables uniformes utilizadas por el sombreador. La tabla también incluye la información de tipo y el valor predeterminado, si se especifica.

### <a name="varying-shader-inputs-and-semantics"></a>Variables y semánticas de sombreador variables

Los distintos parámetros de entrada (de una función de sombreador de nivel superior) se deben marcar con una palabra clave semántica o uniforme que indique que el valor es constante para la ejecución del sombreador. Si una entrada de sombreador de nivel superior no está marcada con una palabra clave semántica o uniforme, el sombreador no se compilará.

La semántica de entrada es un nombre que se usa para vincular la entrada especificada a una salida de la parte anterior de la canalización de gráficos. Por ejemplo, los sombreadores de vértices usan la semántica de entrada POSITION0 para especificar dónde se deben vincular los datos de posición del búfer de vértices.

Los sombreadores de píxeles y vértices tienen diferentes conjuntos de semántica de entrada debido a las distintas partes de la canalización de gráficos que se alimentan en cada unidad de sombreador. La semántica de entrada del sombreador de vértices describe la información por vértice (por ejemplo: posición, normal, coordenadas de textura, color, tangente, binormalización, etc.) que se va a cargar desde un búfer de vértices en un formato que el sombreador de vértices puede consumir. La semántica de entrada se asigna directamente al uso de la declaración de vértices y al índice de uso.

La semántica de entrada del sombreador de píxeles describe la información que la unidad de rasterización proporciona por píxel. Los datos se generan mediante la interpolación entre las salidas del sombreador de vértices para cada vértice de la primitiva actual. La semántica de entrada del sombreador de píxeles básico vincula el color de salida y la información de coordenadas de textura con los parámetros de entrada.

La semántica de entrada se puede asignar a la entrada del sombreador mediante dos métodos:

-   Anexar un signo de dos puntos y el nombre semántico a la declaración del parámetro.
-   Definir una estructura de entrada con semántica de entrada asignada a cada miembro de la estructura.

Los sombreadores de vértices y píxeles proporcionan datos de salida a la siguiente fase de canalización de gráficos. La semántica de salida se usa para especificar cómo se deben vincular los datos generados por el sombreador a las entradas de la siguiente fase. Por ejemplo, la semántica de salida de un sombreador de vértices se usa para vincular las salidas de los interpoladores en el rasterizador para generar los datos de entrada para el sombreador de píxeles. Las salidas del sombreador de píxeles son los valores proporcionados a la unidad de combinación alfa para cada uno de los destinos de representación o el valor de profundidad escrito en el búfer de profundidad.

La semántica de salida del sombreador de vértices se usa para vincular el sombreador con el sombreador de píxeles y con la fase de rasterizador. Un sombreador de vértices utilizado por el rasterizador y no expuesto al sombreador de píxeles debe generar los datos de la posición como mínimo. Los sombreadores de vértices que generan datos de color y coordenada de textura proporcionan los datos a un sombreador de píxeles una vez realizada la interpolación.

La semántica de salida del sombreador de píxeles enlaza los colores de salida de un sombreador de píxeles con el destino de representación correcto. El color de salida del sombreador de píxeles se vincula a la fase de mezcla alfa, que determina cómo se modifican los destinos de representación de destino. La salida de profundidad del sombreador de píxeles se puede usar para cambiar los valores de profundidad de destino en la ubicación de la cuadrícula actual. La salida de profundidad y varios destinos de representación solo se admiten con algunos modelos de sombreador.

La sintaxis de la semántica de salida es idéntica a la sintaxis para especificar la semántica de entrada. La semántica se puede especificar directamente en los parámetros declarados como parámetros "out" o asignados durante la definición de una estructura que se devuelve como un parámetro "out" o el valor devuelto de una función.

La semántica identifica de dónde proceden los datos. La semántica son identificadores opcionales que identifican las entradas y salidas del sombreador. La semántica aparece en una de tres ubicaciones:

-   Después de un miembro de estructura.
-   Después de un argumento de la lista de argumentos de entrada de una función.
-   Después de la lista de argumentos de entrada de la función.

En este ejemplo se usa una estructura para proporcionar una o más entradas del sombreador de vértices y otra estructura para proporcionar una o más salidas del sombreador de vértices. Cada uno de los miembros de la estructura utiliza una semántica.


```
vector vClr;

struct VS_INPUT
{
    float4 vPosition : POSITION;
    float3 vNormal : NORMAL;
    float4 vBlendWeights : BLENDWEIGHT;
};

struct VS_OUTPUT
{
    float4  vPosition : POSITION;
    float4  vDiffuse : COLOR;

};

float4x4 mWld1;
float4x4 mWld2;
float4x4 mWld3;
float4x4 mWld4;

float Len;
float4 vLight;

float4x4 mTot;

VS_OUTPUT VS_Skinning_Example(const VS_INPUT v, uniform float len=100)
{
    VS_OUTPUT out;

    // Skin position (to world space)
    float3 vPosition = 
        mul(v.vPosition, (float4x3) mWld1) * v.vBlendWeights.x +
        mul(v.vPosition, (float4x3) mWld2) * v.vBlendWeights.y +
        mul(v.vPosition, (float4x3) mWld3) * v.vBlendWeights.z +
        mul(v.vPosition, (float4x3) mWld4) * v.vBlendWeights.w;
    // Skin normal (to world space)
    float3 vNormal =
        mul(v.vNormal, (float3x3) mWld1) * v.vBlendWeights.x + 
        mul(v.vNormal, (float3x3) mWld2) * v.vBlendWeights.y + 
        mul(v.vNormal, (float3x3) mWld3) * v.vBlendWeights.z + 
        mul(v.vNormal, (float3x3) mWld4) * v.vBlendWeights.w;
    
    // Output stuff
    out.vPosition    = mul(float4(vPosition + vNormal * Len, 1), mTot);
    out.vDiffuse  = dot(vLight,vNormal);

    return out;
}
```



La estructura de entrada identifica los datos del búfer de vértice que proporcionará las entradas del sombreador. Este sombreador asigna los datos de los elementos Position, normal y blendweight del búfer de vértices en los registros del sombreador de vértices. El tipo de datos de entrada no tiene que coincidir exactamente con el tipo de datos de declaración de vértices. Si no coincide exactamente, los datos del vértice se convertirán automáticamente al tipo de datos de HLSL cuando se escriban en los registros del sombreador. Por ejemplo, si los datos normales se definieron como de tipo UINT por la aplicación, se convertiría en un float3 cuando lo leyó el sombreador.

Si los datos de la secuencia de vértices contienen menos componentes que el tipo de datos del sombreador correspondiente, los componentes que faltan se inicializarán en 0 (excepto en w, que se inicializa en 1).

La semántica de entrada es similar a los valores de [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage).

La estructura de salida identifica los parámetros de salida del sombreador de vértices de posición y color. La canalización usará estas salidas para la rasterización del triángulo (en el procesamiento primitivo). La salida marcada como datos de posición denota la posición de un vértice en un espacio homogéneo. Como mínimo, un sombreador de vértices debe generar datos de posición. La posición del espacio de la pantalla se calcula una vez que se completa el sombreador de vértices dividiendo la coordenada (x, y, z) entre w. En el espacio de pantalla,-1 y 1 son los valores x e y máximo y mínimo de los límites de la ventanilla, mientras que z se usa para las pruebas de búfer z.

La semántica de salida también es similar a los valores de [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage). En general, una estructura de salida de un sombreador de vértices también se puede usar como la estructura de entrada de un sombreador de píxeles, siempre que el sombreador de píxeles no lea las variables marcadas con la posición, el tamaño del punto o la semántica de niebla. Estas semánticas están asociadas a valores escalares por vértice que no se utilizan en un sombreador de píxeles. Si estos valores son necesarios para el sombreador de píxeles, se pueden copiar en otra variable de salida que utiliza una semántica de sombreador de píxeles.

El compilador asigna automáticamente las variables globales a los registros. Las variables globales también se denominan parámetros uniformes porque el contenido de la variable es el mismo para todos los píxeles procesados cada vez que se llama al sombreador. Los registros se encuentran en la tabla de constantes, que se puede leer mediante la interfaz [**ID3DXConstantTable**](/windows/desktop/direct3d9/id3dxconstanttable) .

La semántica de entrada para los sombreadores de píxeles asigna valores en registros de hardware específicos para el transporte entre los sombreadores de vértices y los sombreadores de píxeles. Cada tipo de registro tiene propiedades específicas. Dado que actualmente solo hay dos semánticas para las coordenadas de color y de textura, es habitual que la mayoría de los datos se marquen como una coordenada de textura aunque no lo sea.

Tenga en cuenta que la estructura de salida del sombreador de vértices usó una entrada con datos de posición, que no se usa en el sombreador de píxeles. HLSL permite datos de salida válidos de un sombreador de vértices que no son datos de entrada válidos para un sombreador de píxeles, siempre que no se haga referencia a ellos en el sombreador de píxeles.

Los argumentos de entrada también pueden ser matrices. El compilador incrementa automáticamente la semántica para cada elemento de la matriz. Por ejemplo, considere la siguiente declaración explícita:


```
struct VS_OUTPUT
{
    float4 Position   : POSITION;
    float3 Diffuse    : COLOR0;
    float3 Specular   : COLOR1;               
    float3 HalfVector : TEXCOORD3;
    float3 Fresnel    : TEXCOORD2;               
    float3 Reflection : TEXCOORD0;               
    float3 NoiseCoord : TEXCOORD1;               
};

float4 Sparkle(VS_OUTPUT In) : COLOR
```



La declaración explícita que se indicó anteriormente es equivalente a la declaración siguiente que tendrá la semántica automáticamente incrementada por el compilador:


```
float4 Sparkle(float4 Position : POSITION,
                 float3 Col[2] : COLOR0,
                 float3 Tex[4] : TEXCOORD0) : COLOR0
{
   // shader statements
   ...
```



Al igual que la semántica de entrada, la semántica de salida identifica el uso de datos para los datos de salida del sombreador de píxeles. Muchos sombreadores de píxeles escriben en un solo color de salida. Los sombreadores de píxeles también pueden escribir un valor de profundidad en uno o varios destinos de representación al mismo tiempo (hasta cuatro). Al igual que los sombreadores de vértices, los sombreadores de píxeles usan una estructura para devolver más de una salida. Este sombreador escribe 0 en los componentes de color, así como en el componente de profundidad.


```
struct PS_OUTPUT
{
    float4 Color[4] : COLOR0;
    float  Depth  : DEPTH;
};

PS_OUTPUT main(void)
{
    PS_OUTPUT out;

   // Shader statements
   ...

  // Write up to four pixel shader output colors
  out.Color[0] =  ...
  out.Color[1] =  ...
  out.Color[2] =  ...
  out.Color[3] =  ...

  // Write pixel depth 
  out.Depth =  ...

    return out;
}
```



Los colores de salida del sombreador de píxeles deben ser del tipo FLOAT4. Al escribir varios colores, todos los colores de salida deben usarse de forma contigua. En otras palabras, [COLOR1](dx-graphics-hlsl-semantics.md) no puede ser una salida a menos que ya se haya escrito [COLOR0](dx-graphics-hlsl-semantics.md) . La salida de profundidad del sombreador de píxeles debe ser de tipo float1.

### <a name="samplers-and-texture-objects"></a>Muestras y objetos de textura

Una muestra contiene el estado de muestra. Estado de muestra especifica la textura que se va a muestrear y controla el filtrado que se realiza durante el muestreo. Se requieren tres cosas para muestrear una textura:

-   Una textura
-   Una muestra (con el estado de muestra)
-   Una instrucción de muestreo

Los muestreadores se pueden inicializar con las texturas y el estado de muestra como se muestra aquí:


```
sampler s = sampler_state 
{ 
  texture = NULL; 
  mipfilter = LINEAR; 
};
```



Este es un ejemplo del código para muestrear una textura 2D:


```
texture tex0;
sampler2D s_2D;

float2 sample_2D(float2 tex : TEXCOORD0) : COLOR
{
  return tex2D(s_2D, tex);
}
```



La textura se declara con una variable de textura tex0.

En este ejemplo, se declara una variable de muestra denominada s \_ 2D. El muestreador contiene el estado de muestra dentro de las llaves. Esto incluye la textura que se muestreará y, opcionalmente, el estado del filtro (es decir, modos de ajuste, modos de filtro, etc.). Si se omite el estado de muestra, se aplica un estado de muestra predeterminado que especifica el filtrado lineal y un modo de ajuste para las coordenadas de textura. La función de muestra toma una coordenada de textura de punto flotante de dos componentes y devuelve un color de dos componentes. Esto se representa con el tipo de valor devuelto float2 y representa los datos en los componentes rojo y verde.

Se definen cuatro tipos de muestreadores (vea [palabras clave](dx-graphics-hlsl-appendix.md)) y las búsquedas de textura las realizan las funciones intrínsecas: [**tex1D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md), [**tex2D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex2d.md), [**Tex3D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex3d.md), [**texCUBE (s, t) (DirectX HLSL)**](dx-graphics-hlsl-texcube.md). Este es un ejemplo de muestreo 3D:


```
texture tex0;
sampler3D s_3D;

float3 sample_3D(float3 tex : TEXCOORD0) : COLOR
{
  return tex3D(s_3D, tex);
}
```



Esta declaración de muestra usa el estado de muestra predeterminado para la configuración de filtro y el modo de dirección.

Este es el ejemplo de muestreo del cubo correspondiente:


```
texture tex0;
samplerCUBE s_CUBE;

float3 sample_CUBE(float3 tex : TEXCOORD0) : COLOR
{
  return texCUBE(s_CUBE, tex);
}
```



Y, por último, este es el ejemplo de muestreo 1D:


```
texture tex0;
sampler1D s_1D;

float sample_1D(float tex : TEXCOORD0) : COLOR
{
  return tex1D(s_1D, tex);
}
```



Dado que el tiempo de ejecución no admite las texturas 1D, el compilador usará una textura 2D con el conocimiento de que la coordenada y no es importante. Dado que [**tex1D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md) se implementa como una búsqueda de textura 2D, el compilador es libre de elegir el componente y de una manera eficaz. En algunos escenarios poco frecuentes, el compilador no puede elegir un componente y eficaz, en cuyo caso emitirá una advertencia.


```
texture tex0;
sampler s_1D_float;

float4 main(float texCoords : TEXCOORD) : COLOR
{
    return tex1D(s_1D_float, texCoords);
}
```



Este ejemplo concreto es ineficaz porque el compilador debe trasladar la coordenada de entrada a otro registro (porque una búsqueda 1D se implementa como una búsqueda en 2D y la coordenada de textura se declara como float1). Si el código se reescribe con una entrada float2 en lugar de un float1, el compilador puede usar la coordenada de textura de entrada porque sabe que y se inicializa en algo.


```
texture tex0;
sampler s_1D_float2;

float4 main(float2 texCoords : TEXCOORD) : COLOR
{
    return tex1D(s_1D_float2, texCoords);
}
```



Todas las búsquedas de textura se pueden anexar con "bias" o "proj" (es decir, [**tex2Dbias (DirectX HLSL)**](dx-graphics-hlsl-tex2dbias.md), [**TEXCUBEPROJ (DirectX HLSL)**](dx-graphics-hlsl-texcubeproj.md)). Con el sufijo "proj", la coordenada de textura se divide por el componente w. Con "bias", el nivel de MIP se desplaza por el componente w-. Por lo tanto, todas las búsquedas de textura con un sufijo siempre toman una entrada FLOAT4. [**tex1D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md) y [**tex2D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex2d.md) omiten los componentes YZ y z, respectivamente.

Los muestreadores también se pueden usar en una matriz, aunque ningún back-end admite actualmente el acceso a matrices dinámicas de los muestreadores. Por lo tanto, el siguiente código es válido porque puede resolverse en tiempo de compilación:


```
tex2D(s[0],tex)
```



Sin embargo, este ejemplo no es válido.


```
tex2D(s[a],tex)
```



El acceso dinámico de los muestreadores es principalmente útil para escribir programas con bucles literales. El código siguiente muestra el acceso a la matriz de muestra:


```
sampler sm[4];

float4 main(float4 tex[4] : TEXCOORD) : COLOR
{
    float4 retColor = 1;

    for(int i = 0; i < 4;i++)
    {
        retColor *= tex2D(sm[i],tex[i]);
    }

    return retColor;
}
```



> [!Note]
>
> El uso del tiempo de ejecución de depuración de Microsoft Direct3D puede ayudarle a detectar discrepancias entre el número de componentes de una textura y una muestra.

 

## <a name="writing-functions"></a>Escribir funciones

Las funciones dividen las tareas grandes en otras más pequeñas. Las tareas pequeñas son más fáciles de depurar y se pueden volver a usar, una vez probadas. Las funciones se pueden usar para ocultar detalles de otras funciones, lo que hace que un programa compuesto por funciones sea más fácil de seguir.

Las funciones de HLSL son similares a las funciones de C de varias maneras: ambas contienen una definición y un cuerpo de función y ambos declaran tipos de valor devuelto y listas de argumentos. Al igual que las funciones de C, la validación de HLSL realiza la comprobación de tipos en los argumentos, los tipos de argumento y el valor devuelto durante la compilación del sombreador.

A diferencia de las funciones de C, las funciones de punto de entrada de HLSL usan la semántica para enlazar argumentos de función a entradas y salidas del sombreador (las funciones de HLSL llaman internamente omitir semántica). Esto hace que sea más fácil enlazar los datos del búfer a un sombreador y enlazar las salidas del sombreador a las entradas del sombreador.

Una función contiene una declaración y un cuerpo, y la declaración debe preceder al cuerpo.


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
{
    return mul(inPos, WorldViewProj );
};
```



La declaración de función incluye todo lo delante de las llaves:


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
```



Una declaración de función contiene:

-   Un tipo de valor devuelto
-   Un nombre de función
-   Una lista de argumentos (opcional)
-   Una semántica de salida (opcional)
-   Una anotación (opcional)

El tipo de valor devuelto puede ser cualquiera de los tipos de datos básicos de HLSL, como FLOAT4:


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
{
   ...
}
```



El tipo de valor devuelto puede ser una estructura que ya se ha definido:


```
struct VS_OUTPUT
{
    float4  vPosition        : POSITION;
    float4  vDiffuse         : COLOR;
}; 

VS_OUTPUT VertexShader_Tutorial_1(float4 inPos : POSITION )
{
   ...
}
```



Si la función no devuelve un valor, se puede usar void como tipo de valor devuelto.


```
void VertexShader_Tutorial_1(float4 inPos : POSITION )
{
   ...
}
```



El tipo de valor devuelto siempre aparece primero en una declaración de función.


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
```



Una lista de argumentos declara los argumentos de entrada de una función. También puede declarar valores que se devolverán. Algunos argumentos son los argumentos de entrada y de salida. Este es un ejemplo de un sombreador que toma cuatro argumentos de entrada.


```
float4 Light(float3 LightDir : TEXCOORD1, 
             uniform float4 LightColor,  
             float2 texcrd : TEXCOORD0, 
             uniform sampler samp) : COLOR 
{
    float3 Normal = tex2D(samp,texcrd);

    return dot((Normal*2 - 1), LightDir)*LightColor;
}
```



Esta función devuelve un color final, que es una combinación de una muestra de textura y el color claro. La función toma cuatro entradas. Dos entradas tienen semántica: LightDir tiene la semántica [TEXCOORD1](dx-graphics-hlsl-semantics.md) y texcrd tiene la semántica [TEXCOORD0](dx-graphics-hlsl-semantics.md) . La semántica significa que los datos de estas variables procederán del búfer de vértices. Aunque la variable LightDir tiene una semántica [TEXCOORD1](dx-graphics-hlsl-semantics.md) , es probable que el parámetro no sea una coordenada de textura. El tipo semántico TEXCOORDn se usa a menudo para proporcionar una semántica para un tipo que no está predefinido (no hay ninguna semántica de entrada del sombreador de vértices para una dirección clara).

Las otras dos entradas LightColor y samp se etiquetan con la palabra clave [Uniform](dx-graphics-hlsl-appendix.md) . Son constantes uniformes que no cambiarán entre las llamadas a Draw. Los valores de estos parámetros proceden de variables globales de sombreador.

Los argumentos se pueden etiquetar como entradas con la palabra clave in y argumentos output con la palabra clave out. Los argumentos no se pueden pasar por referencia; sin embargo, un argumento puede ser una entrada y una salida si se declara con la palabra clave INOUT. Los argumentos pasados a una función que están marcados con la palabra clave INOUT se consideran copias del original hasta que la función devuelve y se copian de nuevo. A continuación se muestra un ejemplo del uso de INOUT:


```
void Increment_ByVal(inout float A, inout float B) 
{ 
    A++; B++;
}
```



Esta función incrementa los valores en A y B, y los devuelve.

El cuerpo de la función es todo el código después de la declaración de función.


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
{
    return mul(inPos, WorldViewProj );
};
```



El cuerpo consta de instrucciones que están entre llaves. El cuerpo de la función implementa toda la funcionalidad mediante variables, literales, expresiones e instrucciones.

El cuerpo del sombreador hace dos cosas: realiza una multiplicación de la matriz y devuelve un resultado de FLOAT4. La multiplicación de la matriz se realiza con la función [**mul (DirectX HLSL)**](dx-graphics-hlsl-mul.md) , que realiza multiplicaciones de matriz 4x4. **mul (DirectX HLSL)** se denomina función intrínseca porque ya está integrada en la biblioteca HLSL de funciones. Las funciones intrínsecas se tratarán con más detalle en la sección siguiente.

La matriz multiplica una combinación de vectores de entrada y una WorldViewProj de matriz compuesta. El resultado es colocar los datos transformados en el espacio de la pantalla. Este es el procesamiento del sombreador de vértices mínimo que se puede hacer. Si usamos la canalización de función fija en lugar de un sombreador de vértices, los datos de vértices podrían dibujarse después de realizar esta transformación.

La última instrucción de un cuerpo de función es una instrucción return. Al igual que C, esta instrucción devuelve el control de la función a la instrucción que llamó a la función.

Los tipos de valor devueltos de función pueden ser cualquiera de los tipos de datos simples definidos en HLSL, incluidos bool, int Half, float y Double. Los tipos devueltos pueden ser uno de los tipos de datos complejos como vectores y matrices. Los tipos HLSL que hacen referencia a objetos no se pueden usar como tipos de valor devuelto. Esto incluye u, Vertexshader, Texture y muestreador.

Este es un ejemplo de una función que usa una estructura para un tipo de valor devuelto.


```
float4x4 WorldViewProj : WORLDVIEWPROJ;

struct VS_OUTPUT
{
    float4 Pos  : POSITION;
};

VS_OUTPUT VS_HLL_Example(float4 inPos : POSITION )
{
    VS_OUTPUT Out;

    Out.Pos = mul(inPos,  WorldViewProj );

    return Out;
};
```



El tipo de valor devuelto FLOAT4 se ha reemplazado por la estructura VS \_ Output, que ahora contiene un solo miembro FLOAT4.

Una instrucción return indica el final de una función. Esta es la instrucción return más sencilla. Devuelve el control de la función al programa que realiza la llamada. No devuelve ningún valor.


```
void main()
{
    return ;
}
```



Una instrucción return puede devolver uno o más valores. Este ejemplo devuelve un valor literal:


```
float main( float input : COLOR0) : COLOR0
{
    return 0;
}
```



En este ejemplo se devuelve el resultado escalar de una expresión:


```
return  light.enabled = true ;
```



Este ejemplo devuelve un FLOAT4 construido a partir de una variable local y un literal:


```
return  float4(color.rgb, 1) ;
```



Este ejemplo devuelve un FLOAT4 que se construye a partir del resultado devuelto de una función intrínseca y algunos valores literales:


```
float4 func(float2 a: POSITION): COLOR
{
    return float4(sin(length(a) * 100.0) * 0.5 + 0.5, sin(a.y * 50.0), 0, 1);
}
```



En este ejemplo se devuelve una estructura que contiene uno o más miembros:


```
float4x4 WorldViewProj;

struct VS_OUTPUT
{
    float4 Pos  : POSITION;
};

VS_OUTPUT VertexShader_Tutorial_1(float4 inPos : POSITION )
{
    VS_OUTPUT out;
    out.Pos = mul(inPos, WorldViewProj );
    return out;
};
```



## <a name="flow-control"></a>Control de flujo

El hardware del sombreador de píxeles y vértices más actual está diseñado para ejecutar un sombreador línea a línea y ejecutar cada instrucción una vez. HLSL admite el control de flujo, que incluye bifurcaciones estáticas, instrucciones de predicado, bucles estáticos, bifurcación dinámica y bucle dinámico.

Anteriormente, el uso de una instrucción If producía el código del sombreador de lenguaje de ensamblado que implementa tanto el lado if como el lado else del flujo de código. Este es un ejemplo de en el código HLSL que se compiló para vs \_ 1 \_ 1:


```
if (Value > 0)
    oPos = Value1; 
else
    oPos = Value2; 
```



Y este es el código de ensamblado resultante:


```
// Calculate linear interpolation value in r0.w
mov r1.w, c2.x               
slt r0.w, c3.x, r1.w         
// Linear interpolation between value1 and value2
mov r7, -c1                      
add r2, r7, c0                   
mad oPos, r0.w, r2, c1  
```



Cierto hardware permite bucles estáticos o dinámicos, pero la mayoría de ellas requieren ejecución lineal. En los modelos que no admiten bucles, todos los bucles deben estar inscritos. Un ejemplo es el ejemplo de ejemplo [DepthOfField](https://msdn.microsoft.com/library/Ee416592(v=VS.85).aspx) que usa bucles no rescritos incluso para los \_ sombreadores de PS 1 \_ 1.

HLSL ahora incluye compatibilidad con cada uno de estos tipos de control de flujo:

-   bifurcación estática
-   instrucciones de predicado
-   bucle estático
-   bifurcación dinámica
-   bucle dinámico

La bifurcación estática permite activar o desactivar bloques de código de sombreador en función de una constante de sombreador booleano. Este es un método práctico para habilitar o deshabilitar las rutas de acceso de código según el tipo de objeto que se está representando actualmente. Entre las llamadas a Draw, puede decidir qué características desea admitir con el sombreador actual y, a continuación, establecer las marcas booleanas necesarias para obtener ese comportamiento. Las instrucciones que están deshabilitadas por una constante booleana se omiten durante la ejecución del sombreador.

La compatibilidad con bifurcación más conocida es la bifurcación dinámica. Con las bifurcaciones dinámicas, la condición de comparación reside en una variable, lo que significa que la comparación se realiza para cada vértice o cada píxel en tiempo de ejecución (en lugar de la comparación que se produce en tiempo de compilación, o entre dos llamadas a Draw). El impacto en el rendimiento es el costo de la bifurcación más el costo de las instrucciones en el lateral de la bifurcación tomada. La bifurcación dinámica se implementa en el modelo de sombreador 3 o superior. La optimización de los sombreadores que funcionan con estos modelos es similar a la optimización del código que se ejecuta en una CPU.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación para HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 