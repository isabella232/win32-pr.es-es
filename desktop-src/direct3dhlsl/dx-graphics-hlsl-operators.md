---
title: Operadores
description: Las expresiones son secuencias de variables y literales puntuados por operadores.
ms.assetid: c31aa0b8-1284-48aa-b000-d72433f0f5cc
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 33b1a6f7dcc1297e415fe2e224ec39c58529f7619c9438586f28613a83ead1ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118091002"
---
# <a name="operators"></a>Operadores

Las expresiones son secuencias de [variables](dx-graphics-hlsl-variable-syntax.md) y literales puntuados por [operadores](dx-graphics-hlsl-statement-blocks.md). Los operadores determinan cómo se combinan, comparan, seleccionan, y así sucesivamente las variables y literales. Los operadores incluyen:



| Nombre del operador                                                                                | Operadores                                                                   |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Operadores aditivos y multiplicativos](#additive-and-multiplicative-operators) | +, -, \*, /, %                                                     |
| [Operador array](#array-operator)                                               | \[i\]                                                              |
| [Operadores de asignación](#assignment-operators)                                   | =, +=, -=, \*=, /=, %=                                             |
| [Conversión binaria](#binary-casts)                                                   | Reglas de C para float e int, reglas de C o int o int para valores int para bool     |
| [Operadores bit a bit](#bitwise-operators)                                         | ~, <<, >>, &, \| , ^, <<=, >>=, &=, \| =, ^= |
| [Operadores matemáticos booleanos](#boolean-math-operators)                               | & &, \| \| , ?:                                                      |
| [Operador de conversión](#cast-operator)                                                 | (tipo)                                                             |
| [Operador de coma](#comma-operator)                                               | ,                                                                  |
| [Operadores de comparación](#comparison-operators)                                   | <, >, ==, !=, <=, >=                                   |
| [Operadores de prefijo o postfijo](#prefix-or-postfix-operators)                     | ++, --                                                             |
| [Structure (Operador)](#structure-operator)                                       | .                                                                  |
| [Operadores unarios](#unary-operators)                                             | !, -, +                                                            |



 

Muchos de los operadores son por componente, lo que significa que la operación se realiza de forma independiente para cada componente de cada variable. Por ejemplo, una única variable de componente tiene una operación realizada. Por otro lado, una variable de cuatro componentes tiene cuatro operaciones realizadas, una para cada componente.

Todos los operadores que hacen algo al valor, como + y \* , funcionan por componente.

Los operadores de comparación requieren un único componente [](dx-graphics-hlsl-any.md) para funcionar a menos que use la función intrínseca [**all**](dx-graphics-hlsl-all.md) o con una variable de varios componentes. Se produce un error en la operación siguiente porque la instrucción if requiere un solo valor bool, pero recibe un bool4:


```
if (A4 < B4)
```



Las siguientes operaciones se realizarán correctamente:


```
if ( any(A4 < B4) )
if ( all(A4 < B4) )
```



Los operadores de conversión binaria [**asfloat**](dx-graphics-hlsl-asfloat.md), [**asint**](dx-graphics-hlsl-asint.md), y así sucesivamente funcionan por componente, excepto [**para asdouble**](asdouble.md) cuyas reglas especiales están documentadas.

Los operadores de selección, como los corchetes de punto, coma y matriz, no funcionan por componente.

Los operadores de conversión cambian el número de componentes. Las siguientes operaciones de conversión muestran su equivalencia:


```
(float) i4 ->   float(i4.x)
(float4)i ->   float4(i, i, i, i)
```



## <a name="additive-and-multiplicative-operators"></a>Operadores aditivos y multiplicativos

Los operadores de suma y multiplicación son: +, -, \* , /, %


```
int i1 = 1;
int i2 = 2;
int i3 = i1 + i2;  // i3 = 3
i3 = i1 * i2;        // i3 = 1 * 2 = 2
```




```
i3 = i1/i2;       // i3 = 1/3 = 0.333. Truncated to 0 because i3 is an integer.
i3 = i2/i1;       // i3 = 2/1 = 2
```




```
float f1 = 1.0;
float f2 = 2.0f;
float f3 = f1 - f2; // f3 = 1.0 - 2.0 = -1.0
f3 = f1 * f2;         // f3 = 1.0 * 2.0 = 2.0
```




```
f3 = f1/f2;        // f3 = 1.0/2.0 = 0.5
f3 = f2/f1;        // f3 = 2.0/1.0 = 2.0
```



El operador de módulo devuelve el resto de una división. Esto genera resultados diferentes al usar números enteros y de punto flotante. Los restos enteros que son fraccionales se truncarán.


```
int i1 = 1;
int i2 = 2;
i3 = i1 % i2;      // i3 = remainder of 1/2, which is 1
i3 = i2 % i1;      // i3 = remainder of 2/1, which is 0
i3 = 5 % 2;        // i3 = remainder of 5/2, which is 1
i3 = 9 % 2;        // i3 = remainder of 9/2, which is 1
```



El operador de módulo trunca un resto fracciontario cuando se usan enteros.


```
f3 = f1 % f2;      // f3 = remainder of 1.0/2.0, which is 0.5
f3 = f2 % f1;      // f3 = remainder of 2.0/1.0, which is 0.0
```



El operador % solo se define en los casos en los que ambos lados son positivos o ambos lados son negativos. A diferencia de C, también funciona en tipos de datos de punto flotante, así como en enteros.

## <a name="array-operator"></a>Operador array

El operador de selección de miembros de matriz " \[ i " selecciona uno o varios componentes de una \] matriz. Es un conjunto de corchetes que contienen un índice de base cero.


```
int arrayOfInts[4] = { 0,1,2,3 };
arrayOfInts[0] = 2;
arrayOfInts[1] = arrayOfInts[0];
```



El operador de matriz también se puede usar para acceder a un vector.


```
float4 4D_Vector = { 0.0f, 1.0f, 2.0f, 3.0f  };         
float 1DFloat = 4D_Vector[1];          // 1.0f
```



Al agregar un índice adicional, el operador de matriz también puede acceder a una matriz.


```
float4x4 mat4x4 = {{0,0,0,0}, {1,1,1,1}, {2,2,2,2}, {3,3,3,3} };
mat4x4[0][1] = 1.1f;
float 1DFloat = mat4x4[0][1];      // 0.0f
```



El primer índice es el índice de fila de base cero. El segundo índice es el índice de columna de base cero.

## <a name="assignment-operators"></a>Operadores de asignación

Los operadores de asignación son: =, +=, -=, \* =, /=

A las variables se les pueden asignar valores literales:


```
int i = 1;            
float f2 = 3.1f; 
bool b = false;
string str = "string";
```



También se pueden asignar variables al resultado de una operación matemática:


```
int i1 = 1;
i1 += 2;           // i1 = 1 + 2 = 3
```



Una variable se puede usar en cualquier lado del signo igual:


```
float f3 = 0.5f;
f3 *= f3;          // f3 = 0.5 * 0.5 = 0.25
```



La división de las variables de punto flotante es la esperada porque los restos decimales no son un problema.


```
float f1 = 1.0;
f1 /= 3.0f;        // f1 = 1.0/3.0 = 0.333
```



Tenga cuidado si usa enteros que se pueden dividir, especialmente cuando el truncamiento afecta al resultado. Este ejemplo es idéntico al ejemplo anterior, excepto para el tipo de datos . El truncamiento produce un resultado muy diferente.


```
int i1 = 1;
i1 /= 3;           // i1 = 1/3 = 0.333, which gets truncated to 0
```



## <a name="binary-casts"></a>Conversión binaria

La operación de conversión entre int y float convertirá el valor numérico en las representaciones adecuadas siguiendo las reglas de C para truncar un tipo int. La conversión de un valor de float a int y de vuelta a float dará como resultado una conversión con pérdida en función de la precisión del destino.

Las conversión binarias también se pueden realizar mediante funciones intrínsecas [**(DirectX HLSL),**](dx-graphics-hlsl-intrinsic-functions.md)que reinterpretan la representación de bits de un número en el tipo de datos de destino.


```
asfloat() // Cast to float
asint()   // Cast to int 
asuint()  // Cast to uint
```



## <a name="bitwise-operators"></a>Operadores bit a bit

HLSL admite los siguientes operadores bit a bit, que tienen la misma prioridad que C con respecto a otros operadores. En la tabla siguiente se describen los operadores.

> [!Note]  
> Los operadores bit a bit requieren [Shader Model 4 \_ 0](dx-graphics-hlsl-sm4.md) con Direct3D 10 y hardware superior.

 



| Operador          |  Función                 |
|-----------|-------------------|
| ~         | No lógico       |
| <<  | Desplazamiento a la izquierda        |
| >>  | Desplazamiento a la derecha       |
| &         | Logical And       |
| \|        | Or lógico.        |
| ^         | Xor lógico       |
| <<= | Desplazamiento a la izquierda Igual  |
| >>= | Desplazamiento a la derecha Igual |
| &=        | Y iguales         |
| \|=       | O igual          |
| ^=        | Xor Equal         |



 

Los operadores bit a bit se definen para funcionar solo en tipos de datos int y uint. Al intentar usar operadores bit a bit en tipos de datos float o struct, se producirá un error.

## <a name="boolean-math-operators"></a>Operadores matemáticos booleanos

Los operadores matemáticos booleanos son:  &&, \| \| , ?:


```
bool b1 = true;
bool b2 = false;
bool b3 = b1 && b2 // b3 = true AND false = false
b3 = b1 || b2                // b3 = true OR false = true
```



A diferencia de la evaluación de cortocircuito de &&, y ?: en C, las expresiones HLSL nunca cortocircuiona una evaluación porque son \| \| operaciones vectoriales. Siempre se evalúan todos los lados de la expresión.

Los operadores booleanos funcionan por componente. Esto significa que si compara dos vectores, el resultado es un vector que contiene el resultado booleano de la comparación para cada componente.

Para las expresiones que usan operadores booleanos, el tamaño y el tipo de componente de cada variable se promueven para que sean los mismos antes de que se produzca la operación. El tipo promocionado determina la resolución en la que tiene lugar la operación, así como el tipo de resultado de la expresión. Por ejemplo, una expresión int3 + float se promovería a float3 + float3 para la evaluación y su resultado sería de tipo float3.

## <a name="cast-operator"></a>Operador de conversión

Una expresión precedida de un nombre de tipo entre paréntesis es una conversión de tipo explícita. Una conversión de tipo convierte la expresión original en el tipo de datos de la conversión. En general, los tipos de datos simples se pueden convertir a los tipos de datos más complejos (con una conversión de promoción), pero solo algunos tipos de datos complejos se pueden convertir en tipos de datos simples (con una conversión de degradación).

Solo la conversión de tipos del lado derecho es legal. Por ejemplo, expresiones como `(int)myFloat = myInt;` no son válidas. En su lugar, use `myFloat = (float)myInt;`.

El compilador también realiza la conversión de tipos implícita. Por ejemplo, las dos expresiones siguientes son equivalentes:


```
int2 b = int2(1,2) + 2;
int2 b = int2(1,2) + int2(2,2);
```



## <a name="comma-operator"></a>Operador de coma

El operador de coma (,) separa una o varias expresiones que se van a evaluar en orden. El valor de la última expresión de la secuencia se usa como valor de la secuencia.

Este es un caso al que merece la pena llamar la atención. Si el tipo de constructor se deja accidentalmente fuera del lado derecho del signo igual, el lado derecho ahora contiene cuatro expresiones, separadas por tres comas.


```
// Instead of using a constructor
float4 x = float4(0,0,0,1); 

// The type on the right side is accidentally left off
float4 x = (0,0,0,1); 
```



El operador de coma evalúa una expresión de izquierda a derecha. Esto reduce el lado derecho a:


```
float4 x = 1; 
```



HLSL usa la promoción escalar en este caso, por lo que el resultado es como si se hubiera escrito de la siguiente manera:


```
float4 x = float4(1,1,1,1);
```



En este caso, dejar fuera el tipo float4 del lado derecho es probablemente un error que el compilador no pueda detectar porque se trata de una instrucción válida.

## <a name="comparison-operators"></a>Operadores de comparación

Los operadores de comparación son: <, >, ==, !=, <=, >=.

Compare valores que sean mayores (o menores que) cualquier valor escalar:


```
if( dot(lightDirection, normalVector) > 0 )
   // Do something; the face is lit
```




```
if( dot(lightDirection, normalVector) < 0 )
   // Do nothing; the face is backwards
```



O bien, compare valores iguales a (o no iguales a) cualquier valor escalar:


```
if(color.a == 0)
   // Skip processing because the face is invisible

if(color.a != 0)
   // Blend two colors together using the alpha value
```



O bien, combine y compare valores mayores o iguales que (o menores o iguales que) cualquier valor escalar:


```
if( position.z >= oldPosition.z )
   // Skip the new face because it is behind the existing face
```




```
if( currentValue <= someInitialCondition )
   // Reset the current value to its initial condition
```



Cada una de estas comparaciones se puede realizar con cualquier tipo de datos escalar.

Para usar operadores de comparación con tipos de vector y matriz, use [**la función intrínseca all**](dx-graphics-hlsl-all.md) o any. [](dx-graphics-hlsl-any.md)

Se produce un error en esta operación porque la instrucción if requiere un solo valor bool, pero recibe un bool4:


```
if (A4 < B4)
```



Estas operaciones se realizarán correctamente:


```
if ( any(A4 < B4) )
if ( all(A4 < B4) )
```



## <a name="prefix-or-postfix-operators"></a>Operadores de prefijo o postfijo

Los operadores de prefijo y postfijo son: ++, --. Los operadores de prefijo cambian el contenido de la variable antes de evaluar la expresión. Los operadores de postfijo cambian el contenido de la variable después de evaluar la expresión.

En este caso, un bucle usa el contenido de i para realizar un seguimiento del recuento de bucles.


```
float4 arrayOfFloats[4] = { 1.0f, 2.0f, 3.0f, 4.4f };

for (int i = 0; i<4; )
{
    arrayOfFloats[i++] *= 2; 
}
```



Dado que se usa el operador de incremento postfijo (++), arrayOfFloats i se multiplica por \[ \] 2 antes de que i se incremente. Esto podría reorganizarse ligeramente para usar el operador de incremento de prefijo. Este es más difícil de leer, aunque ambos ejemplos son equivalentes.


```
float4 arrayOfFloats[4] = { 1.0f, 2.0f, 3.0f, 4.4f };

for (int i = 0; i<4; )
{
    arrayOfFloats[++i - 1] *= 2; 
}
```



Dado que se usa el operador de prefijo (++), arrayOfFloats i+1 - 1 se multiplica por 2 después de \[ \] incrementar i.

El operador de decremento de prefijo y decremento de postfijo (--) se aplican en la misma secuencia que el operador de incremento. La diferencia es que el decremento resta 1 en lugar de agregar 1.

## <a name="structure-operator"></a>Structure (Operador)

El operador de selección de miembros de estructura (.) es un punto. Dada esta estructura:


```
struct position
{
float4 x;
float4 y;
float4 z;
};
```



Se puede leer de la siguiente forma:


```
struct position pos = { 1,2,3 };

float 1D_Float = pos.x
1D_Float = pos.y
```



Cada miembro se puede leer o escribir con el operador structure:


```
struct position pos = { 1,2,3 };
pos.x = 2.0f;
pos.z = 1.0f;       // z = 1.0f
pos.z = pos.x      // z = 2.0f
```



## <a name="unary-operators"></a>Operadores unarios

Los operadores unaarios son: !, -, +

Los operadores unarios operan en un solo operando.


```
bool b = false;
bool b2 = !b;      // b2 = true
int i = 2;
int i2 = -i;       // i2 = -2
int j = +i2;       // j = +2
```



## <a name="operator-precedence"></a>Prioridad de los operadores

Cuando una expresión contiene más de un operador, la prioridad del operador determina el orden de evaluación. La prioridad del operador para HLSL sigue la misma prioridad que C.

## <a name="remarks"></a>Comentarios

Las llaves ( {,} ) inician y finalizan un bloque de instrucciones. Cuando un bloque de instrucciones usa una sola instrucción, las llaves son opcionales.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones (DirectX HLSL)](dx-graphics-hlsl-statements.md)
</dt> </dl>

 

 




