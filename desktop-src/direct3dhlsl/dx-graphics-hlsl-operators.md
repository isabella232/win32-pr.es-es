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
ms.openlocfilehash: d7a44fe02983038658247fedaec7122f09306548
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119610"
---
# <a name="operators"></a><span data-ttu-id="e1023-103">Operadores</span><span class="sxs-lookup"><span data-stu-id="e1023-103">Operators</span></span>

<span data-ttu-id="e1023-104">Las expresiones son secuencias de [variables](dx-graphics-hlsl-variable-syntax.md) y literales puntuados por [operadores](dx-graphics-hlsl-statement-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="e1023-104">Expressions are sequences of [variables](dx-graphics-hlsl-variable-syntax.md) and literals punctuated by [operators](dx-graphics-hlsl-statement-blocks.md).</span></span> <span data-ttu-id="e1023-105">Los operadores determinan cómo se combinan, comparan, seleccionan, y así sucesivamente las variables y literales.</span><span class="sxs-lookup"><span data-stu-id="e1023-105">Operators determine how the variables and literals are combined, compared, selected, and so on.</span></span> <span data-ttu-id="e1023-106">Los operadores incluyen:</span><span class="sxs-lookup"><span data-stu-id="e1023-106">The operators include:</span></span>



| <span data-ttu-id="e1023-107">Nombre del operador</span><span class="sxs-lookup"><span data-stu-id="e1023-107">Operator name</span></span>                                                                                | <span data-ttu-id="e1023-108">Operadores</span><span class="sxs-lookup"><span data-stu-id="e1023-108">Operators</span></span>                                                                   |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="e1023-109">Operadores aditivos y multiplicativos</span><span class="sxs-lookup"><span data-stu-id="e1023-109">Additive and Multiplicative Operators</span></span>](#additive-and-multiplicative-operators) | <span data-ttu-id="e1023-110">+, -, \*, /, %</span><span class="sxs-lookup"><span data-stu-id="e1023-110">+, -, \*, /, %</span></span>                                                     |
| [<span data-ttu-id="e1023-111">Operador array</span><span class="sxs-lookup"><span data-stu-id="e1023-111">Array Operator</span></span>](#array-operator)                                               | <span data-ttu-id="e1023-112">\[i\]</span><span class="sxs-lookup"><span data-stu-id="e1023-112">\[i\]</span></span>                                                              |
| [<span data-ttu-id="e1023-113">Operadores de asignación</span><span class="sxs-lookup"><span data-stu-id="e1023-113">Assignment Operators</span></span>](#assignment-operators)                                   | <span data-ttu-id="e1023-114">=, +=, -=, \*=, /=, %=</span><span class="sxs-lookup"><span data-stu-id="e1023-114">=, +=, -=, \*=, /=, %=</span></span>                                             |
| [<span data-ttu-id="e1023-115">Conversión binaria</span><span class="sxs-lookup"><span data-stu-id="e1023-115">Binary Casts</span></span>](#binary-casts)                                                   | <span data-ttu-id="e1023-116">Reglas de C para float e int, reglas de C o intrínsecas HLSL para bool</span><span class="sxs-lookup"><span data-stu-id="e1023-116">C rules for float and int, C rules or HLSL intrinsics for bool</span></span>     |
| [<span data-ttu-id="e1023-117">Operadores bit a bit</span><span class="sxs-lookup"><span data-stu-id="e1023-117">Bitwise Operators</span></span>](#bitwise-operators)                                         | <span data-ttu-id="e1023-118">~, <<, >>, &, \| , ^, <<=, >>=, &=, \| =, ^=</span><span class="sxs-lookup"><span data-stu-id="e1023-118">~, <<, >>, &, \|, ^, <<=, >>=, &=, \|=, ^=</span></span> |
| [<span data-ttu-id="e1023-119">Operadores matemáticos booleanos</span><span class="sxs-lookup"><span data-stu-id="e1023-119">Boolean Math Operators</span></span>](#boolean-math-operators)                               | <span data-ttu-id="e1023-120">& &, , \| \| ?:</span><span class="sxs-lookup"><span data-stu-id="e1023-120">& &, \|\|, ?:</span></span>                                                      |
| [<span data-ttu-id="e1023-121">Operador de conversión</span><span class="sxs-lookup"><span data-stu-id="e1023-121">Cast Operator</span></span>](#cast-operator)                                                 | <span data-ttu-id="e1023-122">(tipo)</span><span class="sxs-lookup"><span data-stu-id="e1023-122">(type)</span></span>                                                             |
| [<span data-ttu-id="e1023-123">Operador de coma</span><span class="sxs-lookup"><span data-stu-id="e1023-123">Comma Operator</span></span>](#comma-operator)                                               | <span data-ttu-id="e1023-124">,</span><span class="sxs-lookup"><span data-stu-id="e1023-124">,</span></span>                                                                  |
| [<span data-ttu-id="e1023-125">Operadores de comparación</span><span class="sxs-lookup"><span data-stu-id="e1023-125">Comparison Operators</span></span>](#comparison-operators)                                   | <span data-ttu-id="e1023-126"><, >, ==, !=, <=, >=</span><span class="sxs-lookup"><span data-stu-id="e1023-126"><, >, ==, !=, <=, >=</span></span>                                   |
| [<span data-ttu-id="e1023-127">Operadores de prefijo o postfijo</span><span class="sxs-lookup"><span data-stu-id="e1023-127">Prefix or Postfix Operators</span></span>](#prefix-or-postfix-operators)                     | <span data-ttu-id="e1023-128">++, --</span><span class="sxs-lookup"><span data-stu-id="e1023-128">++, --</span></span>                                                             |
| [<span data-ttu-id="e1023-129">Structure (Operador)</span><span class="sxs-lookup"><span data-stu-id="e1023-129">Structure Operator</span></span>](#structure-operator)                                       | <span data-ttu-id="e1023-130">.</span><span class="sxs-lookup"><span data-stu-id="e1023-130">.</span></span>                                                                  |
| [<span data-ttu-id="e1023-131">Operadores unarios</span><span class="sxs-lookup"><span data-stu-id="e1023-131">Unary Operators</span></span>](#unary-operators)                                             | <span data-ttu-id="e1023-132">!, -, +</span><span class="sxs-lookup"><span data-stu-id="e1023-132">!, -, +</span></span>                                                            |



 

<span data-ttu-id="e1023-133">Muchos de los operadores son por componente, lo que significa que la operación se realiza de forma independiente para cada componente de cada variable.</span><span class="sxs-lookup"><span data-stu-id="e1023-133">Many of the operators are per-component, which means that the operation is performed independently for each component of each variable.</span></span> <span data-ttu-id="e1023-134">Por ejemplo, una única variable de componente tiene una operación realizada.</span><span class="sxs-lookup"><span data-stu-id="e1023-134">For example, a single component variable has one operation performed.</span></span> <span data-ttu-id="e1023-135">Por otro lado, una variable de cuatro componentes tiene cuatro operaciones realizadas, una para cada componente.</span><span class="sxs-lookup"><span data-stu-id="e1023-135">On the other hand, a four-component variable has four operations performed, one for each component.</span></span>

<span data-ttu-id="e1023-136">Todos los operadores que hacen algo al valor, como + y \* , funcionan por componente.</span><span class="sxs-lookup"><span data-stu-id="e1023-136">All of the operators that do something to the value, such as + and \*, work per component.</span></span>

<span data-ttu-id="e1023-137">Los operadores de comparación requieren un único componente [](dx-graphics-hlsl-any.md) para funcionar a menos que use la función intrínseca [**all**](dx-graphics-hlsl-all.md) o con una variable de varios componentes.</span><span class="sxs-lookup"><span data-stu-id="e1023-137">The comparison operators require a single component to work unless you use the [**all**](dx-graphics-hlsl-all.md) or [**any**](dx-graphics-hlsl-any.md) intrinsic function with a multiple-component variable.</span></span> <span data-ttu-id="e1023-138">Se produce un error en la operación siguiente porque la instrucción if requiere un solo valor bool, pero recibe un bool4:</span><span class="sxs-lookup"><span data-stu-id="e1023-138">The following operation fails because the if statement requires a single bool but receives a bool4:</span></span>


```
if (A4 < B4)
```



<span data-ttu-id="e1023-139">Las siguientes operaciones se realizarán correctamente:</span><span class="sxs-lookup"><span data-stu-id="e1023-139">The following operations succeed:</span></span>


```
if ( any(A4 < B4) )
if ( all(A4 < B4) )
```



<span data-ttu-id="e1023-140">Los operadores de conversión [**binaria asfloat**](dx-graphics-hlsl-asfloat.md), [**asint**](dx-graphics-hlsl-asint.md), y así sucesivamente funcionan por componente, excepto [**para asdouble**](asdouble.md) cuyas reglas especiales están documentadas.</span><span class="sxs-lookup"><span data-stu-id="e1023-140">The binary cast operators [**asfloat**](dx-graphics-hlsl-asfloat.md), [**asint**](dx-graphics-hlsl-asint.md), and so on work per component except for [**asdouble**](asdouble.md) whose special rules are documented.</span></span>

<span data-ttu-id="e1023-141">Los operadores de selección, como los corchetes de punto, coma y matriz, no funcionan por componente.</span><span class="sxs-lookup"><span data-stu-id="e1023-141">Selection operators like period, comma, and array brackets do not work per component.</span></span>

<span data-ttu-id="e1023-142">Los operadores de conversión cambian el número de componentes.</span><span class="sxs-lookup"><span data-stu-id="e1023-142">Cast operators change the number of components.</span></span> <span data-ttu-id="e1023-143">Las siguientes operaciones de conversión muestran su equivalencia:</span><span class="sxs-lookup"><span data-stu-id="e1023-143">The following cast operations show their equivalence:</span></span>


```
(float) i4 ->   float(i4.x)
(float4)i ->   float4(i, i, i, i)
```



## <a name="additive-and-multiplicative-operators"></a><span data-ttu-id="e1023-144">Operadores aditivos y multiplicativos</span><span class="sxs-lookup"><span data-stu-id="e1023-144">Additive and Multiplicative Operators</span></span>

<span data-ttu-id="e1023-145">Los operadores de suma y multiplicación son: +, -, \* , /, %</span><span class="sxs-lookup"><span data-stu-id="e1023-145">The additive and multiplicative operators are: +, -, \*, /, %</span></span>


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



<span data-ttu-id="e1023-146">El operador de módulo devuelve el resto de una división.</span><span class="sxs-lookup"><span data-stu-id="e1023-146">The modulus operator returns the remainder of a division.</span></span> <span data-ttu-id="e1023-147">Esto genera resultados diferentes al usar números enteros y de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="e1023-147">This produces different results when using integers and floating-point numbers.</span></span> <span data-ttu-id="e1023-148">Los restos enteros que son fraccionales se truncarán.</span><span class="sxs-lookup"><span data-stu-id="e1023-148">Integer remainders that are fractional will be truncated.</span></span>


```
int i1 = 1;
int i2 = 2;
i3 = i1 % i2;      // i3 = remainder of 1/2, which is 1
i3 = i2 % i1;      // i3 = remainder of 2/1, which is 0
i3 = 5 % 2;        // i3 = remainder of 5/2, which is 1
i3 = 9 % 2;        // i3 = remainder of 9/2, which is 1
```



<span data-ttu-id="e1023-149">El operador de módulo trunca un resto fracciontario cuando se usan enteros.</span><span class="sxs-lookup"><span data-stu-id="e1023-149">The modulus operator truncates a fractional remainder when using integers.</span></span>


```
f3 = f1 % f2;      // f3 = remainder of 1.0/2.0, which is 0.5
f3 = f2 % f1;      // f3 = remainder of 2.0/1.0, which is 0.0
```



<span data-ttu-id="e1023-150">El operador % solo se define en los casos en los que ambos lados son positivos o ambos lados son negativos.</span><span class="sxs-lookup"><span data-stu-id="e1023-150">The % operator is defined only in cases where either both sides are positive or both sides are negative.</span></span> <span data-ttu-id="e1023-151">A diferencia de C, también funciona en tipos de datos de punto flotante, así como en enteros.</span><span class="sxs-lookup"><span data-stu-id="e1023-151">Unlike C, it also operates on floating-point data types, as well as integers.</span></span>

## <a name="array-operator"></a><span data-ttu-id="e1023-152">Operador array</span><span class="sxs-lookup"><span data-stu-id="e1023-152">Array Operator</span></span>

<span data-ttu-id="e1023-153">El operador de selección de miembros de matriz " \[ i " selecciona uno o varios componentes de una \] matriz.</span><span class="sxs-lookup"><span data-stu-id="e1023-153">The array member selection operator "\[i\]" selects one or more components in an array.</span></span> <span data-ttu-id="e1023-154">Es un conjunto de corchetes que contienen un índice de base cero.</span><span class="sxs-lookup"><span data-stu-id="e1023-154">It is a set of square brackets that contain a zero-based index.</span></span>


```
int arrayOfInts[4] = { 0,1,2,3 };
arrayOfInts[0] = 2;
arrayOfInts[1] = arrayOfInts[0];
```



<span data-ttu-id="e1023-155">El operador de matriz también se puede usar para acceder a un vector.</span><span class="sxs-lookup"><span data-stu-id="e1023-155">The array operator can also be used to access a vector.</span></span>


```
float4 4D_Vector = { 0.0f, 1.0f, 2.0f, 3.0f  };         
float 1DFloat = 4D_Vector[1];          // 1.0f
```



<span data-ttu-id="e1023-156">Al agregar un índice adicional, el operador de matriz también puede acceder a una matriz.</span><span class="sxs-lookup"><span data-stu-id="e1023-156">By adding an additional index, the array operator can also access a matrix.</span></span>


```
float4x4 mat4x4 = {{0,0,0,0}, {1,1,1,1}, {2,2,2,2}, {3,3,3,3} };
mat4x4[0][1] = 1.1f;
float 1DFloat = mat4x4[0][1];      // 0.0f
```



<span data-ttu-id="e1023-157">El primer índice es el índice de fila de base cero.</span><span class="sxs-lookup"><span data-stu-id="e1023-157">The first index is the zero-based row index.</span></span> <span data-ttu-id="e1023-158">El segundo índice es el índice de columna de base cero.</span><span class="sxs-lookup"><span data-stu-id="e1023-158">The second index is the zero-based column index.</span></span>

## <a name="assignment-operators"></a><span data-ttu-id="e1023-159">Operadores de asignación</span><span class="sxs-lookup"><span data-stu-id="e1023-159">Assignment Operators</span></span>

<span data-ttu-id="e1023-160">Los operadores de asignación son: =, +=, -=, \* =, /=</span><span class="sxs-lookup"><span data-stu-id="e1023-160">The assignment operators are: =, +=, -=, \*=, /=</span></span>

<span data-ttu-id="e1023-161">A las variables se les pueden asignar valores literales:</span><span class="sxs-lookup"><span data-stu-id="e1023-161">Variables can be assigned literal values:</span></span>


```
int i = 1;            
float f2 = 3.1f; 
bool b = false;
string str = "string";
```



<span data-ttu-id="e1023-162">También se pueden asignar variables al resultado de una operación matemática:</span><span class="sxs-lookup"><span data-stu-id="e1023-162">Variables can also be assigned the result of a mathematical operation:</span></span>


```
int i1 = 1;
i1 += 2;           // i1 = 1 + 2 = 3
```



<span data-ttu-id="e1023-163">Una variable se puede usar en cualquier lado del signo igual:</span><span class="sxs-lookup"><span data-stu-id="e1023-163">A variable can be used on either side of the equals sign:</span></span>


```
float f3 = 0.5f;
f3 *= f3;          // f3 = 0.5 * 0.5 = 0.25
```



<span data-ttu-id="e1023-164">La división de las variables de punto flotante es la esperada porque los restos decimales no son un problema.</span><span class="sxs-lookup"><span data-stu-id="e1023-164">Division for floating-point variables is as expected because decimal remainders are not a problem.</span></span>


```
float f1 = 1.0;
f1 /= 3.0f;        // f1 = 1.0/3.0 = 0.333
```



<span data-ttu-id="e1023-165">Tenga cuidado si usa enteros que se pueden dividir, especialmente cuando el truncamiento afecta al resultado.</span><span class="sxs-lookup"><span data-stu-id="e1023-165">Be careful if you are using integers that may get divided, especially when truncation affects the result.</span></span> <span data-ttu-id="e1023-166">Este ejemplo es idéntico al ejemplo anterior, excepto para el tipo de datos .</span><span class="sxs-lookup"><span data-stu-id="e1023-166">This example is identical to the previous example, except for the data type.</span></span> <span data-ttu-id="e1023-167">El truncamiento produce un resultado muy diferente.</span><span class="sxs-lookup"><span data-stu-id="e1023-167">The truncation causes a very different result.</span></span>


```
int i1 = 1;
i1 /= 3;           // i1 = 1/3 = 0.333, which gets truncated to 0
```



## <a name="binary-casts"></a><span data-ttu-id="e1023-168">Conversión binaria</span><span class="sxs-lookup"><span data-stu-id="e1023-168">Binary Casts</span></span>

<span data-ttu-id="e1023-169">La operación de conversión entre int y float convertirá el valor numérico en las representaciones adecuadas siguiendo las reglas de C para truncar un tipo int.</span><span class="sxs-lookup"><span data-stu-id="e1023-169">Casting operation between int and float will convert the numeric value into the appropriate representations following C rules for truncating an int type.</span></span> <span data-ttu-id="e1023-170">La conversión de un valor de float a int y de vuelta a float dará lugar a una conversión de pérdida en función de la precisión del destino.</span><span class="sxs-lookup"><span data-stu-id="e1023-170">Casting a value from a float to an int and back to a float will result in a lossy conversion based on the precision of the target.</span></span>

<span data-ttu-id="e1023-171">Las conversión binarias también se pueden realizar mediante funciones intrínsecas [**(DirectX HLSL),**](dx-graphics-hlsl-intrinsic-functions.md)que reinterpretan la representación de bits de un número en el tipo de datos de destino.</span><span class="sxs-lookup"><span data-stu-id="e1023-171">Binary casts may also be performed using [**Intrinsic Functions (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md), which reinterpret the bit representation of a number into the target data type.</span></span>


```
asfloat() // Cast to float
asint()   // Cast to int 
asuint()  // Cast to uint
```



## <a name="bitwise-operators"></a><span data-ttu-id="e1023-172">Operadores bit a bit</span><span class="sxs-lookup"><span data-stu-id="e1023-172">Bitwise Operators</span></span>

<span data-ttu-id="e1023-173">HLSL admite los siguientes operadores bit a bit, que siguen la misma prioridad que C con respecto a otros operadores.</span><span class="sxs-lookup"><span data-stu-id="e1023-173">HLSL supports the following bitwise operators, which follow the same precedence as C with regard to other operators.</span></span> <span data-ttu-id="e1023-174">En la tabla siguiente se describen los operadores.</span><span class="sxs-lookup"><span data-stu-id="e1023-174">The following table describes the operators.</span></span>

> [!Note]  
> <span data-ttu-id="e1023-175">Los operadores bit a bit [requieren Shader Model 4 \_ 0](dx-graphics-hlsl-sm4.md) con Direct3D 10 y hardware superior.</span><span class="sxs-lookup"><span data-stu-id="e1023-175">Bitwise operators require [Shader Model 4\_0](dx-graphics-hlsl-sm4.md) with Direct3D 10 and higher hardware.</span></span>

 



| <span data-ttu-id="e1023-176">Operador</span><span class="sxs-lookup"><span data-stu-id="e1023-176">Operator</span></span>          |  <span data-ttu-id="e1023-177">Función</span><span class="sxs-lookup"><span data-stu-id="e1023-177">Function</span></span>                 |
|-----------|-------------------|
| ~         | <span data-ttu-id="e1023-178">No lógico</span><span class="sxs-lookup"><span data-stu-id="e1023-178">Logical Not</span></span>       |
| <<  | <span data-ttu-id="e1023-179">Desplazamiento a la izquierda</span><span class="sxs-lookup"><span data-stu-id="e1023-179">Left Shift</span></span>        |
| >>  | <span data-ttu-id="e1023-180">Desplazamiento a la derecha</span><span class="sxs-lookup"><span data-stu-id="e1023-180">Right Shift</span></span>       |
| &         | <span data-ttu-id="e1023-181">Logical And</span><span class="sxs-lookup"><span data-stu-id="e1023-181">Logical And</span></span>       |
| \|        | <span data-ttu-id="e1023-182">Or lógico.</span><span class="sxs-lookup"><span data-stu-id="e1023-182">Logical Or</span></span>        |
| ^         | <span data-ttu-id="e1023-183">Xor lógico</span><span class="sxs-lookup"><span data-stu-id="e1023-183">Logical Xor</span></span>       |
| <<= | <span data-ttu-id="e1023-184">Desplazamiento a la izquierda Igual</span><span class="sxs-lookup"><span data-stu-id="e1023-184">Left Shift Equal</span></span>  |
| >>= | <span data-ttu-id="e1023-185">Desplazamiento a la derecha Igual</span><span class="sxs-lookup"><span data-stu-id="e1023-185">Right Shift Equal</span></span> |
| &=        | <span data-ttu-id="e1023-186">Y iguales</span><span class="sxs-lookup"><span data-stu-id="e1023-186">And Equal</span></span>         |
| \|=       | <span data-ttu-id="e1023-187">O igual</span><span class="sxs-lookup"><span data-stu-id="e1023-187">Or Equal</span></span>          |
| ^=        | <span data-ttu-id="e1023-188">Xor Equal</span><span class="sxs-lookup"><span data-stu-id="e1023-188">Xor Equal</span></span>         |



 

<span data-ttu-id="e1023-189">Los operadores bit a bit se definen para funcionar solo en tipos de datos int y uint.</span><span class="sxs-lookup"><span data-stu-id="e1023-189">Bitwise operators are defined to operate only on int and uint data types.</span></span> <span data-ttu-id="e1023-190">Si intenta usar operadores bit a bit en tipos de datos float o struct, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="e1023-190">Attempting to use bitwise operators on float, or struct data types will result in an error.</span></span>

## <a name="boolean-math-operators"></a><span data-ttu-id="e1023-191">Operadores matemáticos booleanos</span><span class="sxs-lookup"><span data-stu-id="e1023-191">Boolean Math Operators</span></span>

<span data-ttu-id="e1023-192">Los operadores matemáticos booleanos son: &&, \| \| , ?:</span><span class="sxs-lookup"><span data-stu-id="e1023-192">The Boolean math operators are: &&, \|\|, ?:</span></span>


```
bool b1 = true;
bool b2 = false;
bool b3 = b1 && b2 // b3 = true AND false = false
b3 = b1 || b2                // b3 = true OR false = true
```



<span data-ttu-id="e1023-193">A diferencia de la evaluación de cortocircuito de &&, y ?: en C, las expresiones HLSL nunca cortocircuiona una evaluación porque son \| \| operaciones vectoriales.</span><span class="sxs-lookup"><span data-stu-id="e1023-193">Unlike short-circuit evaluation of &&, \|\|, and ?: in C, HLSL expressions never short-circuit an evaluation because they are vector operations.</span></span> <span data-ttu-id="e1023-194">Siempre se evalúan todos los lados de la expresión.</span><span class="sxs-lookup"><span data-stu-id="e1023-194">All sides of the expression are always evaluated.</span></span>

<span data-ttu-id="e1023-195">Los operadores booleanos funcionan por componente.</span><span class="sxs-lookup"><span data-stu-id="e1023-195">Boolean operators function on a per-component basis.</span></span> <span data-ttu-id="e1023-196">Esto significa que si compara dos vectores, el resultado es un vector que contiene el resultado booleano de la comparación para cada componente.</span><span class="sxs-lookup"><span data-stu-id="e1023-196">This means that if you compare two vectors, the result is a vector containing the Boolean result of the comparison for each component.</span></span>

<span data-ttu-id="e1023-197">Para las expresiones que usan operadores booleanos, el tamaño y el tipo de componente de cada variable se promueven para que sean los mismos antes de que se produzca la operación.</span><span class="sxs-lookup"><span data-stu-id="e1023-197">For expressions that use Boolean operators, the size and component type of each variable are promoted to be the same before the operation occurs.</span></span> <span data-ttu-id="e1023-198">El tipo promocionado determina la resolución en la que tiene lugar la operación, así como el tipo de resultado de la expresión.</span><span class="sxs-lookup"><span data-stu-id="e1023-198">The promoted type determines the resolution at which the operation takes place, as well as the result type of the expression.</span></span> <span data-ttu-id="e1023-199">Por ejemplo, una expresión int3 + float se promovería a float3 + float3 para la evaluación y su resultado sería de tipo float3.</span><span class="sxs-lookup"><span data-stu-id="e1023-199">For example an int3 + float expression would be promoted to float3 + float3 for evaluation, and its result would be of type float3.</span></span>

## <a name="cast-operator"></a><span data-ttu-id="e1023-200">Operador de conversión</span><span class="sxs-lookup"><span data-stu-id="e1023-200">Cast Operator</span></span>

<span data-ttu-id="e1023-201">Una expresión precedida de un nombre de tipo entre paréntesis es una conversión de tipo explícita.</span><span class="sxs-lookup"><span data-stu-id="e1023-201">An expression preceded by a type name in parenthesis is an explicit type cast.</span></span> <span data-ttu-id="e1023-202">Una conversión de tipo convierte la expresión original en el tipo de datos de la conversión.</span><span class="sxs-lookup"><span data-stu-id="e1023-202">A type cast converts the original expression to the data type of the cast.</span></span> <span data-ttu-id="e1023-203">En general, los tipos de datos simples se pueden convertir a los tipos de datos más complejos (con una conversión de promoción), pero solo algunos tipos de datos complejos se pueden convertir en tipos de datos simples (con una conversión de degradación).</span><span class="sxs-lookup"><span data-stu-id="e1023-203">In general, the simple data types can be cast to the more complex data types (with a promotion cast), but only some complex data types can be cast into simple data types (with a demotion cast).</span></span>

<span data-ttu-id="e1023-204">Solo la conversión de tipos del lado derecho es legal.</span><span class="sxs-lookup"><span data-stu-id="e1023-204">Only right hand side type casting is legal.</span></span> <span data-ttu-id="e1023-205">Por ejemplo, expresiones como `(int)myFloat = myInt;` no son válidas.</span><span class="sxs-lookup"><span data-stu-id="e1023-205">For example, expressions such as `(int)myFloat = myInt;` are illegal.</span></span> <span data-ttu-id="e1023-206">Utilice `myFloat = (float)myInt;` en su lugar.</span><span class="sxs-lookup"><span data-stu-id="e1023-206">Use `myFloat = (float)myInt;` instead.</span></span>

<span data-ttu-id="e1023-207">El compilador también realiza la conversión de tipos implícita.</span><span class="sxs-lookup"><span data-stu-id="e1023-207">The compiler also performs implicit type cast.</span></span> <span data-ttu-id="e1023-208">Por ejemplo, las dos expresiones siguientes son equivalentes:</span><span class="sxs-lookup"><span data-stu-id="e1023-208">For example, the following two expressions are equivalent:</span></span>


```
int2 b = int2(1,2) + 2;
int2 b = int2(1,2) + int2(2,2);
```



## <a name="comma-operator"></a><span data-ttu-id="e1023-209">Operador de coma</span><span class="sxs-lookup"><span data-stu-id="e1023-209">Comma Operator</span></span>

<span data-ttu-id="e1023-210">El operador de coma (,) separa una o varias expresiones que se van a evaluar en orden.</span><span class="sxs-lookup"><span data-stu-id="e1023-210">The comma operator (,) separates one or more expressions that are to be evaluated in order.</span></span> <span data-ttu-id="e1023-211">El valor de la última expresión de la secuencia se usa como valor de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="e1023-211">The value of the last expression in the sequence is used as the value of the sequence.</span></span>

<span data-ttu-id="e1023-212">Este es un caso al que merece la pena llamar la atención.</span><span class="sxs-lookup"><span data-stu-id="e1023-212">Here is one case worth calling attention to.</span></span> <span data-ttu-id="e1023-213">Si el tipo de constructor se deja accidentalmente fuera del lado derecho del signo igual, el lado derecho ahora contiene cuatro expresiones, separadas por tres comas.</span><span class="sxs-lookup"><span data-stu-id="e1023-213">If the constructor type is accidentally left off the right side of the equals sign, the right side now contains four expressions, separated by three commas.</span></span>


```
// Instead of using a constructor
float4 x = float4(0,0,0,1); 

// The type on the right side is accidentally left off
float4 x = (0,0,0,1); 
```



<span data-ttu-id="e1023-214">El operador de coma evalúa una expresión de izquierda a derecha.</span><span class="sxs-lookup"><span data-stu-id="e1023-214">The comma operator evaluates an expression from left to right.</span></span> <span data-ttu-id="e1023-215">Esto reduce el lado derecho a:</span><span class="sxs-lookup"><span data-stu-id="e1023-215">This reduces the right hand side to:</span></span>


```
float4 x = 1; 
```



<span data-ttu-id="e1023-216">HLSL usa la promoción escalar en este caso, por lo que el resultado es como si se hubiera escrito de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="e1023-216">HLSL uses scalar promotion in this case, so the result is as if this were written as follows:</span></span>


```
float4 x = float4(1,1,1,1);
```



<span data-ttu-id="e1023-217">En este caso, dejar fuera el tipo float4 del lado derecho probablemente sea un error que el compilador no pueda detectar porque se trata de una instrucción válida.</span><span class="sxs-lookup"><span data-stu-id="e1023-217">In this instance, leaving off the float4 type from the right side is probably a mistake that the compiler is unable to detect because this is a valid statement.</span></span>

## <a name="comparison-operators"></a><span data-ttu-id="e1023-218">Operadores de comparación</span><span class="sxs-lookup"><span data-stu-id="e1023-218">Comparison Operators</span></span>

<span data-ttu-id="e1023-219">Los operadores de comparación son: <, >, ==, !=, <=, >=.</span><span class="sxs-lookup"><span data-stu-id="e1023-219">The comparison operators are: <, >, ==, !=, <=, >=.</span></span>

<span data-ttu-id="e1023-220">Compare valores que sean mayores (o menores que) cualquier valor escalar:</span><span class="sxs-lookup"><span data-stu-id="e1023-220">Compare values that are greater than (or less than) any scalar value:</span></span>


```
if( dot(lightDirection, normalVector) > 0 )
   // Do something; the face is lit
```




```
if( dot(lightDirection, normalVector) < 0 )
   // Do nothing; the face is backwards
```



<span data-ttu-id="e1023-221">O bien, compare valores iguales a (o no iguales a) cualquier valor escalar:</span><span class="sxs-lookup"><span data-stu-id="e1023-221">Or, compare values equal to (or not equal to) any scalar value:</span></span>


```
if(color.a == 0)
   // Skip processing because the face is invisible

if(color.a != 0)
   // Blend two colors together using the alpha value
```



<span data-ttu-id="e1023-222">O bien, combine y compare valores mayores o iguales que (o menores o iguales que) cualquier valor escalar:</span><span class="sxs-lookup"><span data-stu-id="e1023-222">Or combine both and compare values that are greater than or equal to (or less than or equal to) any scalar value:</span></span>


```
if( position.z >= oldPosition.z )
   // Skip the new face because it is behind the existing face
```




```
if( currentValue <= someInitialCondition )
   // Reset the current value to its initial condition
```



<span data-ttu-id="e1023-223">Cada una de estas comparaciones se puede realizar con cualquier tipo de datos escalar.</span><span class="sxs-lookup"><span data-stu-id="e1023-223">Each of these comparisons can be done with any scalar data type.</span></span>

<span data-ttu-id="e1023-224">Para usar operadores de comparación con tipos de vector y matriz, use [**la función intrínseca all**](dx-graphics-hlsl-all.md) o any. [](dx-graphics-hlsl-any.md)</span><span class="sxs-lookup"><span data-stu-id="e1023-224">To use comparison operators with vector and matrix types, use the [**all**](dx-graphics-hlsl-all.md) or [**any**](dx-graphics-hlsl-any.md) intrinsic function.</span></span>

<span data-ttu-id="e1023-225">Se produce un error en esta operación porque la instrucción if requiere un solo valor bool, pero recibe un bool4:</span><span class="sxs-lookup"><span data-stu-id="e1023-225">This operation fails because the if statement requires a single bool but receives a bool4:</span></span>


```
if (A4 < B4)
```



<span data-ttu-id="e1023-226">Estas operaciones se realizarán correctamente:</span><span class="sxs-lookup"><span data-stu-id="e1023-226">These operations succeed:</span></span>


```
if ( any(A4 < B4) )
if ( all(A4 < B4) )
```



## <a name="prefix-or-postfix-operators"></a><span data-ttu-id="e1023-227">Operadores de prefijo o postfijo</span><span class="sxs-lookup"><span data-stu-id="e1023-227">Prefix or Postfix Operators</span></span>

<span data-ttu-id="e1023-228">Los operadores de prefijo y postfijo son: ++, --.</span><span class="sxs-lookup"><span data-stu-id="e1023-228">The prefix and postfix operators are: ++, --.</span></span> <span data-ttu-id="e1023-229">Los operadores de prefijo cambian el contenido de la variable antes de evaluar la expresión.</span><span class="sxs-lookup"><span data-stu-id="e1023-229">Prefix operators change the contents of the variable before the expression is evaluated.</span></span> <span data-ttu-id="e1023-230">Los operadores de postfijo cambian el contenido de la variable después de evaluar la expresión.</span><span class="sxs-lookup"><span data-stu-id="e1023-230">Postfix operators change the contents of the variable after the expression is evaluated.</span></span>

<span data-ttu-id="e1023-231">En este caso, un bucle usa el contenido de i para realizar un seguimiento del recuento de bucles.</span><span class="sxs-lookup"><span data-stu-id="e1023-231">In this case, a loop uses the contents of i to keep track of the loop count.</span></span>


```
float4 arrayOfFloats[4] = { 1.0f, 2.0f, 3.0f, 4.4f };

for (int i = 0; i<4; )
{
    arrayOfFloats[i++] *= 2; 
}
```



<span data-ttu-id="e1023-232">Dado que se usa el operador de incremento postfijo (++), arrayOfFloats i se multiplica por \[ \] 2 antes de que i se incremente.</span><span class="sxs-lookup"><span data-stu-id="e1023-232">Because the postfix increment operator (++) is used, arrayOfFloats\[i\] is multiplied by 2 before i is incremented.</span></span> <span data-ttu-id="e1023-233">Esto podría reorganizarse ligeramente para usar el operador de incremento de prefijo.</span><span class="sxs-lookup"><span data-stu-id="e1023-233">This could be slightly rearranged to use the prefix increment operator.</span></span> <span data-ttu-id="e1023-234">Este es más difícil de leer, aunque ambos ejemplos son equivalentes.</span><span class="sxs-lookup"><span data-stu-id="e1023-234">This one is harder to read, although both examples are equivalent.</span></span>


```
float4 arrayOfFloats[4] = { 1.0f, 2.0f, 3.0f, 4.4f };

for (int i = 0; i<4; )
{
    arrayOfFloats[++i - 1] *= 2; 
}
```



<span data-ttu-id="e1023-235">Dado que se usa el operador de prefijo (++), arrayOfFloats i+1 - 1 se multiplica por 2 después de \[ \] incrementar i.</span><span class="sxs-lookup"><span data-stu-id="e1023-235">Because the prefix operator (++) is used, arrayOfFloats\[i+1 - 1\] is multiplied by 2 after i is incremented.</span></span>

<span data-ttu-id="e1023-236">El operador de decremento de prefijo y decremento de postfijo (--) se aplican en la misma secuencia que el operador de incremento.</span><span class="sxs-lookup"><span data-stu-id="e1023-236">The prefix decrement and postfix decrement operator (--) are applied in the same sequence as the increment operator.</span></span> <span data-ttu-id="e1023-237">La diferencia es que el decremento resta 1 en lugar de agregar 1.</span><span class="sxs-lookup"><span data-stu-id="e1023-237">The difference is that decrement subtracts 1 instead of adding 1.</span></span>

## <a name="structure-operator"></a><span data-ttu-id="e1023-238">Structure (Operador)</span><span class="sxs-lookup"><span data-stu-id="e1023-238">Structure Operator</span></span>

<span data-ttu-id="e1023-239">El operador de selección de miembros de estructura (.) es un punto.</span><span class="sxs-lookup"><span data-stu-id="e1023-239">The structure member selection operator (.) is a period.</span></span> <span data-ttu-id="e1023-240">Dada esta estructura:</span><span class="sxs-lookup"><span data-stu-id="e1023-240">Given this structure:</span></span>


```
struct position
{
float4 x;
float4 y;
float4 z;
};
```



<span data-ttu-id="e1023-241">Se puede leer de la siguiente forma:</span><span class="sxs-lookup"><span data-stu-id="e1023-241">It can be read like this:</span></span>


```
struct position pos = { 1,2,3 };

float 1D_Float = pos.x
1D_Float = pos.y
```



<span data-ttu-id="e1023-242">Cada miembro se puede leer o escribir con el operador structure:</span><span class="sxs-lookup"><span data-stu-id="e1023-242">Each member can be read or written with the structure operator:</span></span>


```
struct position pos = { 1,2,3 };
pos.x = 2.0f;
pos.z = 1.0f;       // z = 1.0f
pos.z = pos.x      // z = 2.0f
```



## <a name="unary-operators"></a><span data-ttu-id="e1023-243">Operadores unarios</span><span class="sxs-lookup"><span data-stu-id="e1023-243">Unary Operators</span></span>

<span data-ttu-id="e1023-244">Los operadores unaarios son: !, -, +</span><span class="sxs-lookup"><span data-stu-id="e1023-244">The unary operators are: !, -, +</span></span>

<span data-ttu-id="e1023-245">Los operadores unarios operan en un solo operando.</span><span class="sxs-lookup"><span data-stu-id="e1023-245">Unary operators operate on a single operand.</span></span>


```
bool b = false;
bool b2 = !b;      // b2 = true
int i = 2;
int i2 = -i;       // i2 = -2
int j = +i2;       // j = +2
```



## <a name="operator-precedence"></a><span data-ttu-id="e1023-246">Prioridad de los operadores</span><span class="sxs-lookup"><span data-stu-id="e1023-246">Operator Precedence</span></span>

<span data-ttu-id="e1023-247">Cuando una expresión contiene más de un operador, la prioridad del operador determina el orden de evaluación.</span><span class="sxs-lookup"><span data-stu-id="e1023-247">When an expression contains more than one operator, operator precedence determines the order of evaluation.</span></span> <span data-ttu-id="e1023-248">La prioridad del operador para HLSL sigue la misma prioridad que C.</span><span class="sxs-lookup"><span data-stu-id="e1023-248">Operator precedence for HLSL follows the same precedence as C.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1023-249">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e1023-249">Remarks</span></span>

<span data-ttu-id="e1023-250">Las llaves ( {,} ) inician y finalizan un bloque de instrucciones.</span><span class="sxs-lookup"><span data-stu-id="e1023-250">Curly braces ({,}) start and end a statement block.</span></span> <span data-ttu-id="e1023-251">Cuando un bloque de instrucciones usa una sola instrucción, las llaves son opcionales.</span><span class="sxs-lookup"><span data-stu-id="e1023-251">When a statement block uses a single statement, the curly braces are optional.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e1023-252">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e1023-252">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1023-253">Instrucciones (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e1023-253">Statements (DirectX HLSL)</span></span>](dx-graphics-hlsl-statements.md)
</dt> </dl>

 

 




