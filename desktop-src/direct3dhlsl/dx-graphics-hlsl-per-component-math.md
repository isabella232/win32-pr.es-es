---
title: Per-Component operaciones matemáticas
description: Con HLSL, puede programar sombreadores en un nivel de algoritmo.
ms.assetid: a919df50-2d13-489d-9011-1137c997e121
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 96181604b04e888159352e06cc15305ea5b047fda4f2e4e161b81822e64e6c02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118513726"
---
# <a name="per-component-math-operations"></a>Per-Component operaciones matemáticas

Con HLSL, puede programar sombreadores en un nivel de algoritmo. Para entender el lenguaje, deberá saber cómo declarar variables y funciones, usar funciones intrínsecas, definir tipos de datos personalizados y usar semántica para conectar argumentos de sombreador a otros sombreadores y a la canalización.

Una vez que aprenda a crear sombreadores en HLSL, deberá obtener información sobre las llamadas API para que pueda: compilar un sombreador para hardware determinado, inicializar constantes de sombreador e inicializar otro estado de canalización si es necesario.

-   [El tipo de vector](#the-vector-type)
-   [El tipo de matriz](#the-matrix-type)
    -   [Ordenación de matrices](#matrix-ordering)
-   [Ejemplos](#examples)
-   [Temas relacionados](#related-topics)

## <a name="the-vector-type"></a>El tipo de vector

Un vector es una estructura de datos que contiene entre uno y cuatro componentes.


```
bool    bVector;   // scalar containing 1 Boolean
bool1   bVector;   // vector containing 1 Boolean
int1    iVector;   // vector containing 1 int
float3  fVector;   // vector containing 3 floats
double4 dVector;   // vector containing 4 doubles
```



El entero inmediatamente después del tipo de datos es el número de componentes del vector.

Los inicializadores también se pueden incluir en las declaraciones.


```
bool    bVector = false;
int1    iVector = 1;
float3  fVector = { 0.2f, 0.3f, 0.4f };
double4 dVector = { 0.2, 0.3, 0.4, 0.5 };
```



Como alternativa, el tipo de vector se puede usar para realizar las mismas declaraciones:


```
vector <bool,   1> bVector = false;
vector <int,    1> iVector = 1;
vector <float,  3> fVector = { 0.2f, 0.3f, 0.4f };
vector <double, 4> dVector = { 0.2, 0.3, 0.4, 0.5 };
```



El tipo de vector usa corchetes angulares para especificar el tipo y el número de componentes.

Los vectores contienen hasta cuatro componentes, a los que se puede acceder mediante uno de los dos conjuntos de nomenclatura:

-   El conjunto de posiciones: x,y,z,w
-   El conjunto de colores: r,g,b,a

Ambas instrucciones devuelven el valor del tercer componente.


```
// Given
float4 pos = float4(0,0,2,1);

pos.z    // value is 2
pos.b    // value is 2
```



Los conjuntos de nombres pueden usar uno o varios componentes, pero no se pueden mezclar.


```
// Given
float4 pos = float4(0,0,2,1);
float2 temp;

temp = pos.xy  // valid
temp = pos.rg  // valid

temp = pos.xg  // NOT VALID because the position and color sets were used.
```



La especificación de uno o varios componentes vectoriales al leer componentes se denomina deslizar. Por ejemplo:


```
float4 pos = float4(0,0,2,1);
float2 f_2D;
f_2D = pos.xy;   // read two components 
f_2D = pos.xz;   // read components in any order       
f_2D = pos.zx;

f_2D = pos.xx;   // components can be read more than once
f_2D = pos.yy;
```



El enmascaramiento controla cuántos componentes se escriben.


```
float4 pos = float4(0,0,2,1);
float4 f_4D;
f_4D    = pos;     // write four components          

f_4D.xz = pos.xz;  // write two components        
f_4D.zx = pos.xz;  // change the write order

f_4D.xzyw = pos.w; // write one component to more than one component
f_4D.wzyx = pos;
```



Las asignaciones no se pueden escribir en el mismo componente más de una vez. Por lo tanto, el lado izquierdo de esta instrucción no es válido:


```
f_4D.xx = pos.xy;   // cannot write to the same destination components 
```



Además, los espacios de nombres de componente no se pueden mezclar. Se trata de una escritura de componente no válida:


```
f_4D.xg = pos.rgrg;    // invalid write: cannot mix component name spaces 
```



El acceso a un vector como escalar accederá al primer componente del vector. Las dos instrucciones siguientes son equivalentes.


```
f_4D.a = pos * 5.0f;
f_4D.a = pos.r * 5.0f;
```



## <a name="the-matrix-type"></a>El tipo de matriz

Una matriz es una estructura de datos que contiene filas y columnas de datos. Los datos pueden ser cualquiera de los tipos de datos escalares, pero cada elemento de una matriz es el mismo tipo de datos. El número de filas y columnas se especifica con la cadena fila por columna que se anexa al tipo de datos.


```
int1x1    iMatrix;   // integer matrix with 1 row,  1 column
int2x1    iMatrix;   // integer matrix with 2 rows, 1 column
...
int4x1    iMatrix;   // integer matrix with 4 rows, 1 column
...
int1x4    iMatrix;   // integer matrix with 1 row, 4 columns
double1x1 dMatrix;   // double matrix with 1 row,  1 column
double2x2 dMatrix;   // double matrix with 2 rows, 2 columns
double3x3 dMatrix;   // double matrix with 3 rows, 3 columns
double4x4 dMatrix;   // double matrix with 4 rows, 4 columns
```



El número máximo de filas o columnas es 4; el número mínimo es 1.

Una matriz se puede inicializar cuando se declara:


```
float2x2 fMatrix = { 0.0f, 0.1, // row 1
                     2.1f, 2.2f // row 2
                   };   
```



O bien, el tipo de matriz se puede usar para realizar las mismas declaraciones:


```
matrix <float, 2, 2> fMatrix = { 0.0f, 0.1, // row 1
                                 2.1f, 2.2f // row 2
                               };
```



El tipo de matriz usa los corchetes angulares para especificar el tipo, el número de filas y el número de columnas. En este ejemplo se crea una matriz de punto flotante, con dos filas y dos columnas. Se puede usar cualquiera de los tipos de datos escalares.

Esta declaración define una matriz de valores float (números de punto flotante de 32 bits) con dos filas y tres columnas:


```
matrix <float, 2, 3> fFloatMatrix;
```



Una matriz contiene valores organizados en filas y columnas, a los que se puede acceder mediante el operador de estructura "." seguido de uno de los dos conjuntos de nomenclatura:

-   Posición de columna de fila de base cero:
    -   \_m00, \_ m01, \_ m02, \_ m03
    -   \_m10, \_ m11, \_ m12, \_ m13
    -   \_m20, \_ m21, \_ m22, \_ m23
    -   \_m30, \_ m31, \_ m32, \_ m33
-   Posición de columna de fila basada en uno:
    -   \_11, \_ 12, \_ 13, \_ 14
    -   \_21, \_ 22, \_ 23, \_ 24
    -   \_31, \_ 32, \_ 33, \_ 34
    -   \_41, \_ 42, \_ 43, \_ 44

Cada conjunto de nombres comienza con un carácter de subrayado seguido del número de fila y el número de columna. La convención de base cero también incluye la letra "m" antes del número de fila y columna. Este es un ejemplo en el que se usan los dos conjuntos de nomenclatura para acceder a una matriz:


```
// given
float2x2 fMatrix = { 1.0f, 1.1f, // row 1
                     2.0f, 2.1f  // row 2
                   }; 

float f_1D;
f_1D = matrix._m00; // read the value in row 1, column 1: 1.0
f_1D = matrix._m11; // read the value in row 2, column 2: 2.1

f_1D = matrix._11;  // read the value in row 1, column 1: 1.0
f_1D = matrix._22;  // read the value in row 2, column 2: 2.1
```



Al igual que los vectores, los conjuntos de nombres pueden usar uno o varios componentes de cualquier conjunto de nomenclatura.


```
// Given
float2x2 fMatrix = { 1.0f, 1.1f, // row 1
                     2.0f, 2.1f  // row 2
                   };
float2 temp;

temp = fMatrix._m00_m11 // valid
temp = fMatrix._m11_m00 // valid
temp = fMatrix._11_22   // valid
temp = fMatrix._22_11   // valid
```



También se puede acceder a una matriz mediante la notación de acceso de matriz, que es un conjunto de índices de base cero. Cada índice está entre corchetes. Se accede a una matriz 4x4 con los índices siguientes:

-   \[0 \] \[ 0 \] , \[ 0 \] \[ 1 \] , \[ 0 \] \[ 2 \] , \[ 0 \] \[ 3\]
-   \[1 \] \[ \] 0, \[ 1 \] \[ \] 1, \[ 1 \] \[ \] 2, \[ 1 \] \[ 3\]
-   \[2 \] \[ \] 0, \[ 2 \] \[ \] 1, \[ 2 \] \[ 2 \] , \[ 2 \] \[ 3\]
-   \[3 \] \[ \] 0, \[ 3 \] \[ \] 1, \[ 3 \] \[ 2 \] , \[ 3 \] \[ 3\]

Este es un ejemplo de acceso a una matriz:


```
float2x2 fMatrix = { 1.0f, 1.1f, // row 1
                     2.0f, 2.1f  // row 2
                   };
float temp;

temp = fMatrix[0][0] // single component read
temp = fMatrix[0][1] // single component read
```



Observe que el operador de estructura "." no se usa para tener acceso a una matriz. La notación de acceso de matriz no puede usar swling para leer más de un componente.


```
float2 temp;
temp = fMatrix[0][0]_[0][1] // invalid, cannot read two components
```



Sin embargo, el acceso a la matriz puede leer un vector de varios componentes.


```
float2 temp;
float2x2 fMatrix;
temp = fMatrix[0] // read the first row
```



Al igual que con los vectores, la lectura de más de un componente de matriz se denomina deslizar. Se puede asignar más de un componente, suponiendo que solo se usa un espacio de nombres. Todas estas son asignaciones válidas:


```
// Given these variables
float4x4 worldMatrix = float4( {0,0,0,0}, {1,1,1,1}, {2,2,2,2}, {3,3,3,3} );
float4x4 tempMatrix;

tempMatrix._m00_m11 = worldMatrix._m00_m11; // multiple components
tempMatrix._m00_m11 = worldMatrix.m13_m23;

tempMatrix._11_22_33 = worldMatrix._11_22_33; // any order on swizzles
tempMatrix._11_22_33 = worldMatrix._24_23_22;
```



El enmascaramiento controla cuántos componentes se escriben.


```
// Given
float4x4 worldMatrix = float4( {0,0,0,0}, {1,1,1,1}, {2,2,2,2}, {3,3,3,3} );
float4x4 tempMatrix;

tempMatrix._m00_m11 = worldMatrix._m00_m11; // write two components
tempMatrix._m23_m00 = worldMatrix._m00_m11;
```



Las asignaciones no se pueden escribir en el mismo componente más de una vez. Por lo tanto, el lado izquierdo de esta instrucción no es válido:


```
// cannot write to the same component more than once
tempMatrix._m00_m00 = worldMatrix._m00_m11;
```



Además, los espacios de nombres de componente no se pueden mezclar. Se trata de una escritura de componente no válida:


```
// Invalid use of same component on left side
tempMatrix._11_m23 = worldMatrix._11_22; 
```



### <a name="matrix-ordering"></a>Ordenación de matrices

El orden de empaquetado de la matriz para los parámetros uniformes se establece en column-major de forma predeterminada. Esto significa que cada columna de la matriz se almacena en un único registro constante. Por otro lado, una matriz principal de fila empaqueta cada fila de la matriz en un único registro constante. El empaquetado de matriz se puede cambiar con la directiva de matriz **\# \_ pragmapack** o con la fila **\_ principal** o la palabra **clave principal \_ de** columna.

Los datos de una matriz se cargan en registros constantes de sombreador antes de que se ejecute un sombreador. Hay dos opciones para leer los datos de la matriz: en orden principal de fila o en orden de columna principal. El orden principal de columna significa que cada columna de matriz se almacenará en un único registro constante y el orden principal de fila significa que cada fila de la matriz se almacenará en un único registro constante. Esta es una consideración importante para el número de registros constantes que se usan para una matriz.

Se dispone una matriz principal de filas como la siguiente:

:::row:::
    :::column:::
        11<br/>
        21<br/>
        31<br/>
        41<br/>
    :::column-end:::
    :::column:::
        12<br/>
        22<br/>
        32<br/>
        42<br/>
    :::column-end:::
    :::column:::
        13<br/>
        23<br/>
        33<br/>
        43<br/>
    :::column-end:::
    :::column:::
        14<br/>
        24<br/>
        34<br/>
        44<br/>
    :::column-end:::
:::row-end:::




 

Se dispone una matriz de columnas principales como la siguiente:


:::row:::
    :::column:::
        11<br/>
        12<br/>
        13<br/>
        14<br/>
    :::column-end:::
    :::column:::
        21<br/>
        22<br/>
        23<br/>
        24<br/>
    :::column-end:::
    :::column:::
        31<br/>
        32<br/>
        33<br/>
        34<br/>
    :::column-end:::
    :::column:::
        41<br/>
        42<br/>
        43<br/>
        44<br/>
    :::column-end:::
:::row-end:::




 

El orden de la matriz principal de fila y de columna determina el orden en que se leen los componentes de la matriz de las entradas del sombreador. Una vez que los datos se escriben en registros constantes, el orden de la matriz no tiene ningún efecto en cómo se usa o se accede a los datos desde el código del sombreador. Además, las matrices declaradas en un cuerpo del sombreador no se empaquetan en registros constantes. El orden de empaquetado principal de fila y de columna principal no influye en el orden de empaquetado de los constructores (que siempre sigue la ordenación de fila principal).

El orden de los datos de una matriz se puede declarar en tiempo de compilación o el compilador ordenará los datos en tiempo de ejecución para el uso más eficaz.

## <a name="examples"></a>Ejemplos

HLSL usa dos tipos especiales, un tipo de vector y un tipo de matriz para facilitar la programación de gráficos 2D y 3D. Cada uno de estos tipos contiene más de un componente; un vector contiene hasta cuatro componentes y una matriz contiene hasta 16 componentes. Cuando se usan vectores y matrices en ecuaciones HLSL estándar, las matemáticas realizadas están diseñadas para funcionar por componente. Por ejemplo, HLSL implementa esta multiplicación:


```
float4 v = a*b;
```



como una multiplicación de cuatro componentes. El resultado es cuatro escalares:


```
float4 v = a*b;

v.x = a.x*b.x;
v.y = a.y*b.y;
v.z = a.z*b.z;
v.w = a.w*b.w;
```



Se trata de cuatro multiplicaciones donde cada resultado se almacena en un componente independiente de v. Esto se denomina multiplicación de cuatro componentes. HLSL usa matemáticas de componentes, lo que hace que la escritura de sombreadores sea muy eficaz.

Esto es muy diferente de una multiplicación que normalmente se implementa como un producto de punto que genera un único escalar:


```
v = a.x*b.x + a.y*b.y + a.z*b.z + a.w*b.w;
```



Una matriz también usa operaciones por componente en HLSL:


```
float3x3 mat1,mat2;
...
float3x3 mat3 = mat1*mat2;
```



El resultado es una multiplicación por componente de las dos matrices (en lugar de una matriz estándar de 3x3 multiplicada). Una multiplicación por matriz de componentes produce este primer término:


```
mat3.m00 = mat1.m00 * mat2._m00;
```



Esto es diferente de una multiplicación de matriz 3x3 que produciría este primer término:


```
// First component of a four-component matrix multiply
mat.m00 = mat1._m00 * mat2._m00 + 
          mat1._m01 * mat2._m10 + 
          mat1._m02 * mat2._m20 + 
          mat1._m03 * mat2._m30;
```



Las versiones sobrecargadas de la función intrínseca de multiplicación controlan los casos en los que un operando es un vector y el otro operando es una matriz. Por ejemplo: vector \* vectorial, matriz \* vectorial, \* vector de matriz y \* matriz de matrices. Por ejemplo:


```
float4x3 World;

float4 main(float4 pos : SV_POSITION) : SV_POSITION
{
    float4 val;
    val.xyz = mul(pos,World);
    val.w = 0;

    return val;
}   
```



produce el mismo resultado que:


```
float4x3 World;

float4 main(float4 pos : SV_POSITION) : SV_POSITION
{
    float4 val;
    val.xyz = (float3) mul((float1x4)pos,World);
    val.w = 0;

    return val;
}   
```



En este ejemplo se convierte el vector pos en un vector de columna mediante la conversión (float1x4). Cambiar un vector mediante la conversión o el intercambio del orden de los argumentos proporcionados para multiplicar es equivalente a cambiar la matriz.

La conversión automática hace que las funciones intrínsecas de multiplicación y punto devuelvan los mismos resultados que se usan aquí:


```
{
  float4 val;
  return mul(val,val);
}
```



Este resultado de la multiplicación es un vector 1x4 \* 4x1 = 1x1. Esto equivale a un producto de punto:


```
{
  float4 val;
  return dot(val,val);
}
```



que devuelve un único valor escalar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de datos (HLSL de DirectX)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 




