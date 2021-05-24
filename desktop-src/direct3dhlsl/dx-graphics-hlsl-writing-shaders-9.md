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
ms.openlocfilehash: 64a64d08518cb987850c87da3fb19c264519a7f7
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335389"
---
# <a name="writing-hlsl-shaders-in-direct3d-9"></a>Escribir sombreadores HLSL en Direct3D 9

-   [Conceptos básicos del sombreador de vértices](#vertex-shader-basics)
-   [Conceptos básicos del sombreador de píxeles](#pixel-shader-basics)
    -   [Estados de la fase de textura y del muestreador](#texture-stage-and-sampler-states)
    -   [Entradas del sombreador de píxeles](#pixel-shader-inputs)
    -   [Salidas del sombreador de píxeles](#pixel-shader-outputs)
-   [Entradas del sombreador y variables de sombreador](#shader-inputs-and-shader-variables)
    -   [Declarar variables de sombreador](#declaring-shader-variables)
    -   [Entradas uniformes del sombreador](#uniform-shader-inputs)
    -   [Variación de las entradas y semánticas del sombreador](#varying-shader-inputs-and-semantics)
    -   [Muestreadores y objetos de textura](#samplers-and-texture-objects)
-   [Escribir funciones](#writing-functions)
-   [Control de flujo](#flow-control)
-   [Temas relacionados](#related-topics)

## <a name="vertex-shader-basics"></a>Vertex-Shader básicos

Cuando está en funcionamiento, un sombreador de vértices programable reemplaza el procesamiento de vértices realizado por la canalización de gráficos de Microsoft Direct3D. Mientras se usa un sombreador de vértices, la canalización de función fija omite la información de estado relativa a las operaciones de transformación e iluminación. Cuando se deshabilita el sombreador de vértices y se devuelve el procesamiento de funciones fijas, se aplica toda la configuración de estado actual.

La teselación de primitivas de orden alto debe realizarse antes de que se ejecute el sombreador de vértices. Las implementaciones que realizan teselación de superficie después del procesamiento del sombreador deben hacerlo de una manera que no sea evidente para la aplicación y el código del sombreador.

Como mínimo, un sombreador de vértices debe generar la posición del vértice en un espacio de recorte homogéneo. Opcionalmente, el sombreador de vértices puede generar coordenadas de textura, color de vértice, iluminación de vértices, factores de latitud, y así sucesivamente.

## <a name="pixel-shader-basics"></a>Pixel-Shader basics

Los sombreadores de píxeles realizan el procesamiento de píxeles en píxeles individuales. Los sombreadores de píxeles funcionan en colaboración con sombreadores de vértices; la salida de un sombreador de vértices proporciona las entradas para un sombreador de píxeles. Otras operaciones de píxeles (mezcla de mezcla, operaciones de galería de símbolos y combinación de destino de representación) se producen después de la ejecución del sombreador.

### <a name="texture-stage-and-sampler-states"></a>Estados de la fase de textura y del muestreador

Un sombreador de píxeles reemplaza completamente la funcionalidad de combinación de píxeles especificada por la mezcla de varias texturas, incluidas las operaciones definidas previamente por los estados de la fase de textura. Las operaciones de muestreo y filtrado de textura controladas por los estados de fase de textura estándar para la minificación, la ampliación, el filtrado de mip y los modos de direccionamiento de encapsulado, se pueden inicializar en sombreadores. La aplicación puede cambiar estos estados sin necesidad de regenerar el sombreador enlazado actualmente. El estado de configuración se puede facilitar aún más si los sombreadores están diseñados dentro de un efecto.

### <a name="pixel-shader-inputs"></a>Entradas del sombreador de píxeles

Para las versiones del sombreador de píxeles ps 1 - ps 2 0, los colores difusos y especulares se saturan (fijan) en el intervalo de 0 a 1 antes de que lo use el \_ \_ \_ \_ sombreador.

Se supone que la entrada de valores de color en el sombreador de píxeles es correcta en la perspectiva, pero esto no se garantiza (para todo el hardware). Los colores muestreados a partir de coordenadas de textura se iteran de una manera correcta de perspectiva y se fijan al intervalo de 0 a 1 durante la iteración.

### <a name="pixel-shader-outputs"></a>Salidas del sombreador de píxeles

Para las versiones del sombreador de píxeles ps \_ \_ 1 - ps 1 4, el resultado emitido por el sombreador de píxeles es el \_ \_ contenido del registro r0. Todo lo que contiene cuando el sombreador completa el procesamiento se envía a la fase de puesta en escena y al blender de destino de representación.

Para las versiones del sombreador de píxeles ps 2 0 y versiones posteriores, el color de salida se emite desde \_ \_ oC0 - oC4.

## <a name="shader-inputs-and-shader-variables"></a>Entradas del sombreador y variables de sombreador

-   [Declarar variables de sombreador](#declaring-shader-variables)
-   [Entradas uniformes del sombreador](#uniform-shader-inputs)
-   [Variación de las entradas y semánticas del sombreador](#varying-shader-inputs-and-semantics)
-   [Muestreadores y objetos de textura](#samplers-and-texture-objects)

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



Estas son algunas declaraciones que muestran muchas de las características de las variables de lenguaje de sombreador de alto nivel (HLSL):


```
float4 color;
uniform float4 position : POSITION; 
const float4 lightDirection = {0,0,1};
```



Las declaraciones de datos pueden usar cualquier tipo válido, incluido:

-   [Tipos de datos (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
-   [Tipo de vector (HLSL de DirectX)](dx-graphics-hlsl-vector.md)
-   [Tipo de matriz (DirectX HLSL)](dx-graphics-hlsl-matrix.md)
-   [Tipo de sombreador (HLSL de DirectX)](dx-graphics-hlsl-shader.md)
-   [Tipo de sampler (HLSL de DirectX)](dx-graphics-hlsl-sampler.md)
-   [Tipo definido por el usuario (HLSL de DirectX)](dx-graphics-hlsl-user-defined.md)

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



Las variables de nivel superior se declaran fuera de todas las funciones. Los argumentos de nivel superior son parámetros de una función de nivel superior. Una función de nivel superior es cualquier función a la que llama la aplicación (en lugar de una función a la que llama otra función).

### <a name="uniform-shader-inputs"></a>Entradas uniformes del sombreador

Los sombreadores de vértices y píxeles aceptan dos tipos de datos de entrada: variables y uniformes. La entrada variable son los datos que son únicos para cada ejecución del sombreador. Para un sombreador de vértices, los datos variables (por ejemplo: posición, normal, etc.) proceden de los flujos de vértices. Los datos uniformes (por ejemplo: color del material, transformación del mundo, etc.) son constantes para varias ejecuciones de un sombreador. Para aquellos que están familiarizados con los modelos de sombreador de ensamblados, los datos uniformes se especifican mediante registros constantes y datos variables por los registros v y t.

Los datos uniformes se pueden especificar mediante dos métodos. El método más común es declarar variables globales y usarlas dentro de un sombreador. Cualquier uso de variables globales dentro de un sombreador dará lugar a la adición de esa variable a la lista de variables uniformes requeridas por ese sombreador. El segundo método consiste en marcar un parámetro de entrada de la función de sombreador de nivel superior como uniforme. Este marcado especifica que la variable especificada debe agregarse a la lista de variables uniformes.

Las variables uniformes usadas por un sombreador se comunican de nuevo a la aplicación a través de la tabla constante. La tabla constante es el nombre de la tabla de símbolos que define cómo encajan las variables uniformes utilizadas por un sombreador en los registros constantes. Los parámetros uniformes de la función aparecen en la tabla constante anteponer un signo de dólar ($), a diferencia de las variables globales. El signo de dólar es necesario para evitar conflictos de nombres entre entradas uniformes locales y variables globales del mismo nombre.

La tabla constante contiene las ubicaciones de registro constantes de todas las variables uniformes utilizadas por el sombreador. La tabla también incluye la información de tipo y el valor predeterminado, si se especifica.

### <a name="varying-shader-inputs-and-semantics"></a>Variación de las entradas y semánticas del sombreador

Los distintos parámetros de entrada (de una función de sombreador de nivel superior) deben marcarse con una palabra clave semántica o uniforme que indique que el valor es constante para la ejecución del sombreador. Si una entrada de sombreador de nivel superior no está marcada con una palabra clave semántica o uniforme, el sombreador no se compilará.

La semántica de entrada es un nombre que se usa para vincular la entrada dada a una salida de la parte anterior de la canalización de gráficos. Por ejemplo, los sombreadores de vértices usan la semántica de entrada POSITION0 para especificar dónde se deben vincular los datos de posición del búfer de vértices.

Los sombreadores de píxeles y vértices tienen distintos conjuntos de semántica de entrada debido a las distintas partes de la canalización de gráficos que se alimentan en cada unidad de sombreador. La semántica de entrada del sombreador de vértices describe la información por vértice (por ejemplo: posición, normal, coordenadas de textura, color, tangente, binormal, etc.) que se va a cargar desde un búfer de vértice en un formulario que el sombreador de vértices puede consumir. La semántica de entrada se asigna directamente al uso de la declaración de vértice y al índice de uso.

La semántica de entrada del sombreador de píxeles describe la información proporcionada por píxel por la unidad de rasterización. Los datos se generan interpolando entre las salidas del sombreador de vértices para cada vértice de la primitiva actual. La semántica básica de entrada del sombreador de píxeles vincula el color de salida y la información de coordenadas de textura a los parámetros de entrada.

La semántica de entrada se puede asignar a la entrada del sombreador mediante dos métodos:

-   Anexar dos puntos y el nombre semántico a la declaración de parámetro.
-   Definir una estructura de entrada con semántica de entrada asignada a cada miembro de estructura.

Los sombreadores de vértices y píxeles proporcionan datos de salida a la fase de canalización de gráficos posterior. La semántica de salida se usa para especificar cómo se deben vincular los datos generados por el sombreador a las entradas de la siguiente fase. Por ejemplo, la semántica de salida de un sombreador de vértices se usa para vincular las salidas de los interpoladores en el rasterizador para generar los datos de entrada para el sombreador de píxeles. Las salidas del sombreador de píxeles son los valores proporcionados a la unidad de combinación alfa para cada uno de los destinos de representación o el valor de profundidad escrito en el búfer de profundidad.

La semántica de salida del sombreador de vértices se usa para vincular el sombreador al sombreador de píxeles y a la fase de rasterizador. Un sombreador de vértices consumido por el rasterizador y no expuesto al sombreador de píxeles debe generar datos de posición como mínimo. Los sombreadores de vértices que generan datos de color y coordenada de textura proporcionan los datos a un sombreador de píxeles después de realizar la interpolación.

La semántica de salida del sombreador de píxeles enlaza los colores de salida de un sombreador de píxeles con el destino de representación correcto. El color de salida del sombreador de píxeles está vinculado a la fase de combinación alfa, que determina cómo se modifican los destinos de representación de destino. La salida de profundidad del sombreador de píxeles se puede usar para cambiar los valores de profundidad de destino en la ubicación de trama actual. La salida de profundidad y varios destinos de representación solo se admiten con algunos modelos de sombreador.

La sintaxis de la semántica de salida es idéntica a la sintaxis para especificar la semántica de entrada. La semántica se puede especificar directamente en los parámetros declarados como parámetros "out" o asignarse durante la definición de una estructura que se devuelve como un parámetro "out" o el valor devuelto de una función.

La semántica identifica de dónde proceden los datos. La semántica son identificadores opcionales que identifican las entradas y salidas del sombreador. La semántica aparece en uno de estos tres lugares:

-   Después de un miembro de estructura.
-   Después de un argumento en la lista de argumentos de entrada de una función.
-   Después de la lista de argumentos de entrada de la función.

En este ejemplo se usa una estructura para proporcionar una o varias entradas del sombreador de vértices y otra estructura para proporcionar una o varias salidas del sombreador de vértices. Cada uno de los miembros de la estructura usa una semántica.


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



La estructura de entrada identifica los datos del búfer de vértices que proporcionarán las entradas del sombreador. Este sombreador asigna los datos de los elementos position, normal y blendweight del búfer de vértices a los registros del sombreador de vértices. El tipo de datos de entrada no tiene que coincidir exactamente con el tipo de datos de declaración de vértice. Si no coinciden exactamente, los datos del vértice se convertirán automáticamente en el tipo de datos de HLSL cuando se escriban en los registros del sombreador. Por ejemplo, si la aplicación definió que los datos normales eran de tipo UINT, se convertirían en float3 cuando los lee el sombreador.

Si los datos del flujo de vértices contienen menos componentes que el tipo de datos de sombreador correspondiente, los componentes que faltan se inicializarán en 0 (excepto w, que se inicializa en 1).

La semántica de entrada es similar a los valores de [**D3DDECLUSAGE.**](/windows/desktop/direct3d9/d3ddeclusage)

La estructura de salida identifica los parámetros de salida del sombreador de vértices de posición y color. La canalización usará estas salidas para la rasterización de triángulos (en el procesamiento primitivo). La salida marcada como datos de posición denota la posición de un vértice en un espacio homogéneo. Como mínimo, un sombreador de vértices debe generar datos de posición. La posición del espacio de pantalla se calcula una vez completado el sombreador de vértices dividiendo la coordenada (x, y, z) por w. En el espacio de pantalla, -1 y 1 son los valores mínimo y máximo x e y de los límites de la ventanilla, mientras que z se usa para las pruebas de búfer z.

La semántica de salida también es similar a los valores de [**D3DDECLUSAGE.**](/windows/desktop/direct3d9/d3ddeclusage) En general, también se puede usar una estructura de salida para un sombreador de vértices como estructura de entrada para un sombreador de píxeles, siempre que el sombreador de píxeles no lea de ninguna variable marcada con la posición, el tamaño de punto o la semántica de los píxeles. Esta semántica está asociada a valores escalares por vértice que no usa un sombreador de píxeles. Si estos valores son necesarios para el sombreador de píxeles, se pueden copiar en otra variable de salida que use una semántica de sombreador de píxeles.

El compilador asigna automáticamente las variables globales a los registros. Las variables globales también se denominan parámetros uniformes porque el contenido de la variable es el mismo para todos los píxeles procesados cada vez que se llama al sombreador. Los registros se encuentran en la tabla constante, que se puede leer mediante la [**interfaz ID3DXConstantTable.**](/windows/desktop/direct3d9/id3dxconstanttable)

La semántica de entrada para los sombreadores de píxeles asigna valores a registros de hardware específicos para el transporte entre sombreadores de vértices y sombreadores de píxeles. Cada tipo de registro tiene propiedades específicas. Dado que actualmente solo hay dos semánticas para las coordenadas de color y textura, es habitual que la mayoría de los datos se marquen como una coordenada de textura aunque no lo sea.

Observe que la estructura de salida del sombreador de vértices usó una entrada con datos de posición, que el sombreador de píxeles no usa. HLSL permite datos de salida válidos de un sombreador de vértices que no son datos de entrada válidos para un sombreador de píxeles, siempre que no se haga referencia a ellos en el sombreador de píxeles.

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



La declaración explícita anterior es equivalente a la siguiente declaración que tendrá semántica incrementada automáticamente por el compilador:


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



Los colores de salida del sombreador de píxeles deben ser de tipo float4. Al escribir varios colores, todos los colores de salida deben usarse de forma contigua. En otras palabras, [COLOR1 no puede](dx-graphics-hlsl-semantics.md) ser una salida a menos que ya se haya escrito [COLOR0.](dx-graphics-hlsl-semantics.md) La salida de profundidad del sombreador de píxeles debe ser de tipo float1.

### <a name="samplers-and-texture-objects"></a>Muestreadores y objetos de textura

Un sampler contiene el estado del sampler. El estado del muestreador especifica la textura que se va a muestrear y controla el filtrado que se realiza durante el muestreo. Se requieren tres cosas para muestrear una textura:

-   Una textura
-   Un sampler (con estado sampler)
-   Una instrucción de muestreo

Los muestreadores se pueden inicializar con texturas y el estado del muestreador, como se muestra aquí:


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

En este ejemplo, se declara una variable sampler denominada \_ s 2D. El muestreador contiene el estado del muestreador dentro de las llaves. Esto incluye la textura que se muestrea y, opcionalmente, el estado del filtro (es decir, los modos de encapsulado, los modos de filtro, etc.). Si se omite el estado del muestreador, se aplica un estado de muestreador predeterminado que especifica el filtrado lineal y un modo de encapsulado para las coordenadas de textura. La función sampler toma una coordenada de textura de punto flotante de dos componentes y devuelve un color de dos componentes. Se representa con el tipo de valor devuelto float2 y representa los datos de los componentes rojo y verde.

Se definen cuatro tipos de muestreadores (consulte Palabras clave) y las [búsquedas](dx-graphics-hlsl-appendix.md)de textura las realizan las funciones intrínsecas: [**tex1D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md), [**tex2D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex2d.md), [**tex3D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex3d.md), [**texCUBE(s, t) (DirectX HLSL).**](dx-graphics-hlsl-texcube.md) Este es un ejemplo de muestreo 3D:


```
texture tex0;
sampler3D s_3D;

float3 sample_3D(float3 tex : TEXCOORD0) : COLOR
{
  return tex3D(s_3D, tex);
}
```



Esta declaración de sampler usa el estado de sampler predeterminado para la configuración del filtro y el modo de dirección.

Este es el ejemplo de muestreo de cubo correspondiente:


```
texture tex0;
samplerCUBE s_CUBE;

float3 sample_CUBE(float3 tex : TEXCOORD0) : COLOR
{
  return texCUBE(s_CUBE, tex);
}
```



Por último, este es el ejemplo de muestreo 1D:


```
texture tex0;
sampler1D s_1D;

float sample_1D(float tex : TEXCOORD0) : COLOR
{
  return tex1D(s_1D, tex);
}
```



Dado que el tiempo de ejecución no admite texturas 1D, el compilador usará una textura 2D con el conocimiento de que la coordenada y no es importante. Dado [**que la clase tex1D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md) se implementa como una búsqueda de textura 2D, el compilador puede elegir el componente y de forma eficaz. En algunos escenarios poco frecuentes, el compilador no puede elegir un componente Y eficaz, en cuyo caso emitirá una advertencia.


```
texture tex0;
sampler s_1D_float;

float4 main(float texCoords : TEXCOORD) : COLOR
{
    return tex1D(s_1D_float, texCoords);
}
```



Este ejemplo concreto es ineficaz porque el compilador debe mover la coordenada de entrada a otro registro (porque una búsqueda 1D se implementa como una búsqueda 2D y la coordenada de textura se declara como float1). Si el código se reescribe mediante una entrada float2 en lugar de float1, el compilador puede usar la coordenada de textura de entrada porque sabe que y se inicializa en algo.


```
texture tex0;
sampler s_1D_float2;

float4 main(float2 texCoords : TEXCOORD) : COLOR
{
    return tex1D(s_1D_float2, texCoords);
}
```



Todas las búsquedas de texturas se pueden anexar con "sesgo" o "proj" (es decir, [**texas2Dbias (DirectX HLSL)**](dx-graphics-hlsl-tex2dbias.md), [**texCUBEproj (DirectX HLSL)**](dx-graphics-hlsl-texcubeproj.md)). Con el sufijo "proj", la coordenada de textura se divide por el componente w. Con "sesgo", el nivel de mip se desplaza mediante el componente w. Por lo tanto, todas las búsquedas de textura con un sufijo siempre toman una entrada float4. los componentes yz y z, respectivamente, omiten los componentes [**yz(s, t) (hl1D(s, t) (DirectX**](dx-graphics-hlsl-tex1d.md) [**HLSL) (HLSL de DirectX).**](dx-graphics-hlsl-tex2d.md)

Los muestreadores también se pueden usar en la matriz, aunque ningún back-end admite actualmente el acceso a la matriz dinámica de muestreadores. Por lo tanto, lo siguiente es válido porque se puede resolver en tiempo de compilación:


```
tex2D(s[0],tex)
```



Sin embargo, este ejemplo no es válido.


```
tex2D(s[a],tex)
```



El acceso dinámico de muestreadores es principalmente útil para escribir programas con bucles literales. El código siguiente muestra el acceso a la matriz de sampler:


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
> El uso del entorno de ejecución de depuración de Microsoft Direct3D puede ayudarle a detectar discrepancias entre el número de componentes de una textura y un muestreador.

 

## <a name="writing-functions"></a>Escribir funciones

Las funciones divide las tareas grandes en otras más pequeñas. Las tareas pequeñas son más fáciles de depurar y se pueden reutilizar, una vez probadas. Las funciones se pueden usar para ocultar los detalles de otras funciones, lo que facilita el seguimiento de un programa compuesto de funciones.

Las funciones HLSL son similares a las funciones de C de varias maneras: ambas contienen una definición y un cuerpo de función y declaran tipos de valor devuelto y listas de argumentos. Al igual que las funciones de C, la validación hlsl comprueba los argumentos, los tipos de argumento y el valor devuelto durante la compilación del sombreador.

A diferencia de las funciones de C, las funciones de punto de entrada HLSL usan semántica para enlazar argumentos de función a entradas y salidas del sombreador (las funciones HLSL llamadas internamente omiten la semántica). Esto facilita el enlace de datos de búfer a un sombreador y el enlace de las salidas del sombreador a las entradas del sombreador.

Una función contiene una declaración y un cuerpo, y la declaración debe preceder al cuerpo.


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
{
    return mul(inPos, WorldViewProj );
};
```



La declaración de función incluye todo lo que hay delante de las llaves:


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
```



Una declaración de función contiene:

-   Tipo de valor devuelto
-   Un nombre de función
-   Una lista de argumentos (opcional)
-   Semántica de salida (opcional)
-   Una anotación (opcional)

El tipo de valor devuelto puede ser cualquiera de los tipos de datos básicos de HLSL, como float4:


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



Una lista de argumentos declara los argumentos de entrada a una función. También puede declarar valores que se devolverán. Algunos argumentos son argumentos de entrada y salida. Este es un ejemplo de un sombreador que toma cuatro argumentos de entrada.


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



Esta función devuelve un color final, que es una mezcla de una muestra de textura y el color claro. La función toma cuatro entradas. Dos entradas tienen semántica: LightDir tiene la semántica [DECORCOORD1](dx-graphics-hlsl-semantics.md) y la semántica [de TEXCOORD0.](dx-graphics-hlsl-semantics.md) La semántica significa que los datos de estas variables procederán del búfer de vértices. Aunque la variable LightDir tiene una [semántica DECORCOORD1,](dx-graphics-hlsl-semantics.md) es probable que el parámetro no sea una coordenada de textura. El tipo semántico TEXASCOORDn se usa a menudo para proporcionar una semántica para un tipo que no está predefinido (no hay semántica de entrada del sombreador de vértices para una dirección de luz).

Las otras dos entradas LightColor y asíns se etiquetan con la [palabra clave uniform.](dx-graphics-hlsl-appendix.md) Se trata de constantes uniformes que no cambiarán entre las llamadas a draw. Los valores de estos parámetros proceden de variables globales del sombreador.

Los argumentos se pueden etiquetar como entradas con la palabra clave in y como argumentos de salida con la palabra clave out. Los argumentos no se pueden pasar por referencia; sin embargo, un argumento puede ser una entrada y una salida si se declara con la palabra clave inout. Los argumentos pasados a una función marcada con la palabra clave inout se consideran copias del original hasta que la función vuelve y se copian de nuevo. Este es un ejemplo de uso de inout:


```
void Increment_ByVal(inout float A, inout float B) 
{ 
    A++; B++;
}
```



Esta función incrementa los valores de A y B y los devuelve.

El cuerpo de la función es todo el código después de la declaración de función.


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
{
    return mul(inPos, WorldViewProj );
};
```



El cuerpo consta de instrucciones que están entre llaves. El cuerpo de la función implementa toda la funcionalidad mediante variables, literales, expresiones e instrucciones.

El cuerpo del sombreador hace dos cosas: realiza una multiplicación de matriz y devuelve un resultado float4. La multiplicación de matriz se realiza con la [**función mul (HLSL de DirectX),**](dx-graphics-hlsl-mul.md) que realiza una multiplicación de matriz 4x4. **Mul (DirectX HLSL)** se denomina función intrínseca porque ya está integrada en la biblioteca hlsl de funciones. Las funciones intrínsecas se tratarán con más detalle en la sección siguiente.

La multiplicación de matriz combina un vector de entrada Pos y una matriz compuesta WorldViewProj. El resultado son los datos de posición transformados en espacio de pantalla. Este es el procesamiento mínimo del sombreador de vértices que podemos hacer. Si se usara la canalización de función fija en lugar de un sombreador de vértices, los datos del vértice se podrían dibujar después de realizar esta transformación.

La última instrucción de un cuerpo de función es una instrucción return. Al igual que C, esta instrucción devuelve el control de la función a la instrucción que llamó a la función.

Los tipos de valor devuelto de función pueden ser cualquiera de los tipos de datos simples definidos en HLSL, incluidos bool, int half, float y double. Los tipos de valor devuelto pueden ser uno de los tipos de datos complejos, como vectores y matrices. Los tipos HLSL que hacen referencia a objetos no se pueden usar como tipos de valor devuelto. Esto incluye pixelshader, vertexshader, texture y sampler.

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



El tipo de valor devuelto float4 se ha reemplazado por la estructura VS \_ OUTPUT, que ahora contiene un único miembro float4.

Una instrucción return indica el final de una función. Esta es la instrucción return más sencilla. Devuelve el control de la función al programa que realiza la llamada. No devuelve ningún valor.


```
void main()
{
    return ;
}
```



Una instrucción return puede devolver uno o varios valores. Este ejemplo devuelve un valor literal:


```
float main( float input : COLOR0) : COLOR0
{
    return 0;
}
```



Este ejemplo devuelve el resultado escalar de una expresión:


```
return  light.enabled;
```



Este ejemplo devuelve un valor float4 construido a partir de una variable local y un literal:


```
return  float4(color.rgb, 1) ;
```



Este ejemplo devuelve un valor float4 que se construye a partir del resultado devuelto a partir de una función intrínseca y algunos valores literales:


```
float4 func(float2 a: POSITION): COLOR
{
    return float4(sin(length(a) * 100.0) * 0.5 + 0.5, sin(a.y * 50.0), 0, 1);
}
```



Este ejemplo devuelve una estructura que contiene uno o varios miembros:


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

La mayoría del hardware actual del sombreador de vértices y píxeles está diseñado para ejecutar una línea de sombreador, ejecutando cada instrucción una vez. HLSL admite el control de flujo, que incluye bifurcación estática, instrucciones predicadas, bucle estático, bifurcación dinámica y bucle dinámico.

Anteriormente, el uso de una instrucción if generaba código de sombreador de lenguaje de ensamblado que implementa el lado if y el otro lado del flujo de código. Este es un ejemplo de en el código HLSL que se compiló para vs \_ \_ 1 1:


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



Algunos hardware permiten bucles estáticos o dinámicos, pero la mayoría requiere una ejecución lineal. En los modelos que no admiten bucles, todos los bucles deben estar inscritos. Un ejemplo es el [ejemplo DepthOfField que](https://msdn.microsoft.com/library/Ee416592(v=VS.85).aspx) usa bucles no inscritos incluso para sombreadores ps \_ \_ 1.

HLSL ahora incluye compatibilidad con cada uno de estos tipos de control de flujo:

-   bifurcación estática
-   instrucciones predicadas
-   bucle estático
-   bifurcación dinámica
-   bucle dinámico

La bifurcación estática permite activar o desactivar bloques de código de sombreador en función de una constante de sombreador booleano. Se trata de un método cómodo para habilitar o deshabilitar rutas de acceso de código en función del tipo de objeto que se representa actualmente. Entre las llamadas a draw, puede decidir qué características desea admitir con el sombreador actual y, a continuación, establecer las marcas booleanas necesarias para obtener ese comportamiento. Las instrucciones deshabilitadas por una constante booleana se omiten durante la ejecución del sombreador.

La compatibilidad con la bifurcación más conocida es la bifurcación dinámica. Con la bifurcación dinámica, la condición de comparación reside en una variable, lo que significa que la comparación se realiza para cada vértice o cada píxel en tiempo de ejecución (en lugar de la comparación que se produce en tiempo de compilación o entre dos llamadas a draw). El impacto en el rendimiento es el costo de la rama más el costo de las instrucciones del lado de la rama tomada. La bifurcación dinámica se implementa en el modelo de sombreador 3 o superior. La optimización de sombreadores que funcionan con estos modelos es similar a la optimización del código que se ejecuta en una CPU.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación para HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 
