---
title: Operaciones matemáticas Per-Component
description: Con HLSL, puede programar sombreadores en un nivel de algoritmo.
ms.assetid: a919df50-2d13-489d-9011-1137c997e121
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5ff30cd19b7821c9a059251e105f6acfa9cf961e
ms.sourcegitcommit: fa5c081bf792b119a7bb92182cde1f85ca75967b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/17/2021
ms.locfileid: "104987403"
---
# <a name="per-component-math-operations"></a>Operaciones matemáticas Per-Component

Con HLSL, puede programar sombreadores en un nivel de algoritmo. Para comprender el lenguaje, debe saber cómo declarar variables y funciones, usar funciones intrínsecas, definir tipos de datos personalizados y usar la semántica para conectar argumentos de sombreador a otros sombreadores y a la canalización.

Una vez que aprenda a crear sombreadores en HLSL, deberá obtener información sobre las llamadas de API para que pueda: compilar un sombreador para hardware determinado, inicializar constantes de sombreador e inicializar otro estado de canalización si es necesario.

-   [Tipo de vector](#the-vector-type)
-   [El tipo de matriz](#the-matrix-type)
    -   [Ordenación de matrices](#matrix-ordering)
-   [Ejemplos](#examples)
-   [Temas relacionados](#related-topics)

## <a name="the-vector-type"></a>Tipo de vector

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

Los vectores contienen hasta cuatro componentes, a los que se puede tener acceso a través de uno de los dos conjuntos de nombres:

-   Conjunto de posiciones: x, y, z, w
-   Conjunto de colores: r, g, b, a

Estas instrucciones devuelven el valor en el tercer componente.


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



La especificación de uno o más componentes vectoriales al leer componentes se denomina permutación. Por ejemplo:


```
float4 pos = float4(0,0,2,1);
float2 f_2D;
f_2D = pos.xy;   // read two components 
f_2D = pos.xz;   // read components in any order       
f_2D = pos.zx;

f_2D = pos.xx;   // components can be read more than once
f_2D = pos.yy;
```



Enmascaramiento controla el número de componentes que se escriben.


```
float4 pos = float4(0,0,2,1);
float4 f_4D;
f_4D    = pos;     // write four components          

f_4D.xz = pos.xz;  // write two components        
f_4D.zx = pos.xz;  // change the write order

f_4D.xzyw = pos.w; // write one component to more than one component
f_4D.wzyx = pos;
```



Las asignaciones no se pueden escribir más de una vez en el mismo componente. Por lo tanto, el lado izquierdo de esta instrucción no es válido:


```
f_4D.xx = pos.xy;   // cannot write to the same destination components 
```



Además, los espacios de nombres de componente no se pueden mezclar. Se trata de una escritura de componente no válida:


```
f_4D.xg = pos.rgrg;    // invalid write: cannot mix component name spaces 
```



El acceso a un vector como escalar tendrá acceso al primer componente del vector. Las dos instrucciones siguientes son equivalentes.


```
f_4D.a = pos * 5.0f;
f_4D.a = pos.r * 5.0f;
```



## <a name="the-matrix-type"></a>El tipo de matriz

Una matriz es una estructura de datos que contiene filas y columnas de datos. Los datos pueden ser cualquiera de los tipos de datos escalares; sin embargo, todos los elementos de una matriz tienen el mismo tipo de datos. El número de filas y columnas se especifica con la cadena de fila por columna anexada al tipo de datos.


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



El tipo de matriz utiliza corchetes angulares para especificar el tipo, el número de filas y el número de columnas. En este ejemplo se crea una matriz de punto flotante, con dos filas y dos columnas. Se puede usar cualquiera de los tipos de datos escalares.

Esta declaración define una matriz de valores Float (números de punto flotante de 32 bits) con dos filas y tres columnas:


```
matrix <float, 2, 3> fFloatMatrix;
```



Una matriz contiene valores organizados en filas y columnas, a los que se puede tener acceso mediante el operador de estructura "." seguido de uno de los dos conjuntos de nombres:

-   Posición de la columna de fila de base cero:
    -   \_M00, \_ M01, \_ M02, \_ M03
    -   \_M10, \_ M11, \_ M12, \_ M13
    -   \_M20, \_ M21, \_ M22, \_ M23
    -   \_M30, \_ M31, \_ M32, \_ M33
-   La posición de la columna de fila basada en uno:
    -   \_11, \_ 12, \_ 13, \_ 14
    -   \_21, \_ 22, \_ 23, \_ 24
    -   \_31, \_ 32, \_ 33, \_ 34
    -   \_41, \_ 42, \_ 43, \_ 44

Cada conjunto de nomenclatura comienza con un carácter de subrayado seguido por el número de fila y el número de columna. La Convención basada en cero también incluye la letra "m" antes del número de fila y columna. Este es un ejemplo en el que se usan los dos conjuntos de nombres para tener acceso a una matriz:


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



Al igual que los vectores, los conjuntos de nomenclatura pueden usar uno o varios componentes de cualquier conjunto de nomenclatura.


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



También se puede tener acceso a una matriz mediante la notación de acceso de matriz, que es un conjunto de índices de base cero. Cada índice se encuentra entre corchetes. Se tiene acceso a una matriz 4x4 con los índices siguientes:

-   \[0 \] \[ 0 \] , \[ 0 \] \[ 1 \] , \[ 0 \] \[ 2 \] , \[ 0 \] \[ 3\]
-   \[1 \] \[ 0 \] , \[ 1 \] \[ 1 \] , \[ 1 \] \[ 2 \] , \[ 1 \] \[ 3\]
-   \[2 \] \[ 0 \] , \[ 2 \] \[ 1 \] , \[ 2 \] \[ 2 \] , \[ 2 \] \[ 3\]
-   \[3 \] \[ 0 \] , \[ 3 \] \[ 1 \] , \[ 3 \] \[ 2 \] , \[ 3 \] \[ 3\]

Este es un ejemplo de acceso a una matriz:


```
float2x2 fMatrix = { 1.0f, 1.1f, // row 1
                     2.0f, 2.1f  // row 2
                   };
float temp;

temp = fMatrix[0][0] // single component read
temp = fMatrix[0][1] // single component read
```



Observe que el operador de estructura "." no se utiliza para tener acceso a una matriz. La notación de acceso a la matriz no puede usar permutación para leer más de un componente.


```
float2 temp;
temp = fMatrix[0][0]_[0][1] // invalid, cannot read two components
```



Sin embargo, el acceso a matrices puede leer un vector de varios componentes.


```
float2 temp;
float2x2 fMatrix;
temp = fMatrix[0] // read the first row
```



Al igual que con los vectores, la lectura de más de un componente de matriz se denomina permutación. Se puede asignar más de un componente, siempre que se use un solo espacio de nombres. Estas son todas las asignaciones válidas:


```
// Given these variables
float4x4 worldMatrix = float4( {0,0,0,0}, {1,1,1,1}, {2,2,2,2}, {3,3,3,3} );
float4x4 tempMatrix;

tempMatrix._m00_m11 = worldMatrix._m00_m11; // multiple components
tempMatrix._m00_m11 = worldMatrix.m13_m23;

tempMatrix._11_22_33 = worldMatrix._11_22_33; // any order on swizzles
tempMatrix._11_22_33 = worldMatrix._24_23_22;
```



Enmascaramiento controla el número de componentes que se escriben.


```
// Given
float4x4 worldMatrix = float4( {0,0,0,0}, {1,1,1,1}, {2,2,2,2}, {3,3,3,3} );
float4x4 tempMatrix;

tempMatrix._m00_m11 = worldMatrix._m00_m11; // write two components
tempMatrix._m23_m00 = worldMatrix._m00_m11;
```



Las asignaciones no se pueden escribir más de una vez en el mismo componente. Por lo tanto, el lado izquierdo de esta instrucción no es válido:


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

El orden de empaquetado de la matriz para los parámetros uniformes se establece en columna-principal de forma predeterminada. Esto significa que cada columna de la matriz se almacena en un único registro constante. Por otro lado, una matriz de una fila principal de filas empaqueta cada fila de la matriz en un solo registro de constante. El empaquetado de matrices se puede cambiar con la directiva **\# pragmapack \_ Matrix** o con la **fila \_ major** o la palabra clave **\_ major** .

Los datos de una matriz se cargan en registros de constantes del sombreador antes de que se ejecute un sombreador. Hay dos opciones para la forma en que se leen los datos de la matriz: en orden de fila principal o en orden de columna principal. El orden principal de las columnas significa que cada columna de la matriz se almacenará en un único registro constante y el orden principal de la fila significa que cada fila de la matriz se almacenará en un único registro constante. Esta es una consideración importante para el número de registros constantes que se usan para una matriz.

Una matriz de filas principales se dispone de la siguiente manera:



|     |     |     |     |
|-----|-----|-----|-----|
| 11  | 12  | 13  | 14  |
| 21  | 22  | 23  | 24  |
| 31  | 32  | 33  | 34  |
| 41  | 42  | 43  | 44  |



 

Una matriz de columnas principales se dispone de la siguiente manera:



|     |     |     |     |
|-----|-----|-----|-----|
| 11  | 21  | 31  | 41  |
| 12  | 22  | 32  | 42  |
| 13  | 23  | 33  | 43  |
| 14  | 24  | 34  | 44  |



 

La ordenación de matrices principal y de columna principal de fila determina el orden en que los componentes de la matriz se leen de las entradas del sombreador. Una vez que los datos se escriben en registros constantes, el orden de las matrices no tiene ningún efecto en la forma en que se usan los datos o se accede a ellos desde el código del sombreador. Además, las matrices declaradas en un cuerpo del sombreador no se empaquetan en registros constantes. El orden de empaquetado principal y de columna principal de fila no tiene influencia en el orden de empaquetado de los constructores (que siempre sigue el orden principal de las filas).

El orden de los datos de una matriz puede declararse en tiempo de compilación, o el compilador ordenará los datos en tiempo de ejecución para obtener el uso más eficaz.

## <a name="examples"></a>Ejemplos

HLSL usa dos tipos especiales, un tipo de vector y un tipo de matriz para facilitar la programación de gráficos 2D y 3D. Cada uno de estos tipos contiene más de un componente; un vector contiene hasta cuatro componentes y una matriz que contiene hasta 16 componentes. Cuando se usan vectores y matrices en ecuaciones estándar de HLSL, la función matemática realizada está diseñada para trabajar por componente. Por ejemplo, HLSL implementa esta multiplicación:


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



Se trata de cuatro multiplicaciones donde cada resultado se almacena en un componente independiente de v. Esto se denomina multiplicación de cuatro componentes. HLSL usa Math de componentes, lo que hace que los sombreadores de escritura sean muy eficaces.

Esto es muy diferente de una multiplicación que normalmente se implementa como un producto punto que genera un único escalar:


```
v = a.x*b.x + a.y*b.y + a.z*b.z + a.w*b.w;
```



Una matriz también usa operaciones por componente en HLSL:


```
float3x3 mat1,mat2;
...
float3x3 mat3 = mat1*mat2;
```



El resultado es una multiplicación por componente de las dos matrices (en lugar de una multiplicación de una matriz de 3x3 estándar). Una multiplicación por matriz de componentes produce este primer término:


```
mat3.m00 = mat1.m00 * mat2._m00;
```



Esto es diferente de la multiplicación de una matriz de 3x3 que produciría este primer término:


```
// First component of a four-component matrix multiply
mat.m00 = mat1._m00 * mat2._m00 + 
          mat1._m01 * mat2._m10 + 
          mat1._m02 * mat2._m20 + 
          mat1._m03 * mat2._m30;
```



Las versiones sobrecargadas de la función intrínseca Multiply controlan los casos en los que un operando es un vector y el otro operando es una matriz. Como: Vector vectorial \* , matriz vectorial \* , Vector de matriz \* y matriz de matriz \* . Por ejemplo:


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



En este ejemplo se convierte el vector de pos en un vector de columna mediante la conversión (float1x4). Cambiar un vector mediante la conversión o cambiar el orden de los argumentos proporcionados a Multiply es equivalente a transponer la matriz.

La conversión de conversión automática hace que las funciones intrínsecas Multiply y DOT devuelvan los mismos resultados que se usan aquí:


```
{
  float4 val;
  return mul(val,val);
}
```



Este resultado de la multiplicación es un \* Vector 4 TB = 1x1. Esto es equivalente a un producto DOT:


```
{
  float4 val;
  return dot(val,val);
}
```



que devuelve un único valor escalar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de datos (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 




