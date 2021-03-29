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
ms.openlocfilehash: 69fc29f366fa781483edb5fd4653674b387fd156
ms.sourcegitcommit: 37fb32f6150b6ca1db6c52d68a553ec2c8c0879a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2020
ms.locfileid: "104487334"
---
# <a name="operators"></a><span data-ttu-id="b5f0e-103">Operadores</span><span class="sxs-lookup"><span data-stu-id="b5f0e-103">Operators</span></span>

<span data-ttu-id="b5f0e-104">Las expresiones son secuencias de [variables](dx-graphics-hlsl-variable-syntax.md) y literales puntuados por [operadores](dx-graphics-hlsl-statement-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="b5f0e-104">Expressions are sequences of [variables](dx-graphics-hlsl-variable-syntax.md) and literals punctuated by [operators](dx-graphics-hlsl-statement-blocks.md).</span></span> <span data-ttu-id="b5f0e-105">Los operadores determinan cómo se combinan las variables y los literales, se comparan, se seleccionan, etc.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-105">Operators determine how the variables and literals are combined, compared, selected, and so on.</span></span> <span data-ttu-id="b5f0e-106">Los operadores incluyen:</span><span class="sxs-lookup"><span data-stu-id="b5f0e-106">The operators include:</span></span>



|                                                                                 |                                                                    |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="b5f0e-107">Nombre de operador</span><span class="sxs-lookup"><span data-stu-id="b5f0e-107">Operator Name</span></span>                                                                   | <span data-ttu-id="b5f0e-108">Operadores</span><span class="sxs-lookup"><span data-stu-id="b5f0e-108">Operators</span></span>                                                          |
| [<span data-ttu-id="b5f0e-109">Operadores de suma y multiplicación</span><span class="sxs-lookup"><span data-stu-id="b5f0e-109">Additive and Multiplicative Operators</span></span>](#additive-and-multiplicative-operators) | <span data-ttu-id="b5f0e-110">+, -, \*, /, %</span><span class="sxs-lookup"><span data-stu-id="b5f0e-110">+, -, \*, /, %</span></span>                                                     |
| [<span data-ttu-id="b5f0e-111">Array (operador)</span><span class="sxs-lookup"><span data-stu-id="b5f0e-111">Array Operator</span></span>](#array-operator)                                               | <span data-ttu-id="b5f0e-112">\[i\]</span><span class="sxs-lookup"><span data-stu-id="b5f0e-112">\[i\]</span></span>                                                              |
| [<span data-ttu-id="b5f0e-113">Operadores de asignación</span><span class="sxs-lookup"><span data-stu-id="b5f0e-113">Assignment Operators</span></span>](#assignment-operators)                                   | <span data-ttu-id="b5f0e-114">=, +=, -=, \*=, /=, %=</span><span class="sxs-lookup"><span data-stu-id="b5f0e-114">=, +=, -=, \*=, /=, %=</span></span>                                             |
| [<span data-ttu-id="b5f0e-115">Conversiones binarias</span><span class="sxs-lookup"><span data-stu-id="b5f0e-115">Binary Casts</span></span>](#binary-casts)                                                   | <span data-ttu-id="b5f0e-116">Reglas de c para Float e int, reglas de C o intrínsecos de HLSL para bool</span><span class="sxs-lookup"><span data-stu-id="b5f0e-116">C rules for float and int, C rules or HLSL intrinsics for bool</span></span>     |
| [<span data-ttu-id="b5f0e-117">Operadores bit a bit</span><span class="sxs-lookup"><span data-stu-id="b5f0e-117">Bitwise Operators</span></span>](#bitwise-operators)                                         | <span data-ttu-id="b5f0e-118">~,  <<,  >>, &, \| , ^,  <<=,  >>=, &=, \| =, ^ =</span><span class="sxs-lookup"><span data-stu-id="b5f0e-118">~, <<, >>, &, \|, ^, <<=, >>=, &=, \|=, ^=</span></span> |
| [<span data-ttu-id="b5f0e-119">Operadores matemáticos booleanos</span><span class="sxs-lookup"><span data-stu-id="b5f0e-119">Boolean Math Operators</span></span>](#boolean-math-operators)                               | <span data-ttu-id="b5f0e-120">& &, \| \| ,?:</span><span class="sxs-lookup"><span data-stu-id="b5f0e-120">& &, \|\|, ?:</span></span>                                                      |
| [<span data-ttu-id="b5f0e-121">Operador de conversión</span><span class="sxs-lookup"><span data-stu-id="b5f0e-121">Cast Operator</span></span>](#cast-operator)                                                 | <span data-ttu-id="b5f0e-122">automáticamente</span><span class="sxs-lookup"><span data-stu-id="b5f0e-122">(type)</span></span>                                                             |
| [<span data-ttu-id="b5f0e-123">Coma (operador)</span><span class="sxs-lookup"><span data-stu-id="b5f0e-123">Comma Operator</span></span>](#comma-operator)                                               | <span data-ttu-id="b5f0e-124">,</span><span class="sxs-lookup"><span data-stu-id="b5f0e-124">,</span></span>                                                                  |
| [<span data-ttu-id="b5f0e-125">Operadores de comparación</span><span class="sxs-lookup"><span data-stu-id="b5f0e-125">Comparison Operators</span></span>](#comparison-operators)                                   | <span data-ttu-id="b5f0e-126"><, >, = =,! =, <=, >=</span><span class="sxs-lookup"><span data-stu-id="b5f0e-126"><, >, ==, !=, <=, >=</span></span>                                   |
| [<span data-ttu-id="b5f0e-127">Operadores de prefijo o postfijo</span><span class="sxs-lookup"><span data-stu-id="b5f0e-127">Prefix or Postfix Operators</span></span>](#prefix-or-postfix-operators)                     | <span data-ttu-id="b5f0e-128">++, --</span><span class="sxs-lookup"><span data-stu-id="b5f0e-128">++, --</span></span>                                                             |
| [<span data-ttu-id="b5f0e-129">Operador de estructura</span><span class="sxs-lookup"><span data-stu-id="b5f0e-129">Structure Operator</span></span>](#structure-operator)                                       | <span data-ttu-id="b5f0e-130">.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-130">.</span></span>                                                                  |
| [<span data-ttu-id="b5f0e-131">Operadores unarios</span><span class="sxs-lookup"><span data-stu-id="b5f0e-131">Unary Operators</span></span>](#unary-operators)                                             | <span data-ttu-id="b5f0e-132">!, -, +</span><span class="sxs-lookup"><span data-stu-id="b5f0e-132">!, -, +</span></span>                                                            |



 

<span data-ttu-id="b5f0e-133">Muchos de los operadores son por componente, lo que significa que la operación se realiza de forma independiente para cada componente de cada variable.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-133">Many of the operators are per-component, which means that the operation is performed independently for each component of each variable.</span></span> <span data-ttu-id="b5f0e-134">Por ejemplo, una única variable de componente tiene una operación realizada.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-134">For example, a single component variable has one operation performed.</span></span> <span data-ttu-id="b5f0e-135">Por otro lado, una variable de cuatro componentes tiene cuatro operaciones realizadas, una para cada componente.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-135">On the other hand, a four-component variable has four operations performed, one for each component.</span></span>

<span data-ttu-id="b5f0e-136">Todos los operadores que realizan alguna acción en el valor, como + y \* , funcionan por componente.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-136">All of the operators that do something to the value, such as + and \*, work per component.</span></span>

<span data-ttu-id="b5f0e-137">Los operadores de comparación requieren que un único componente funcione, a menos que se use la función [**All**](dx-graphics-hlsl-all.md) o [**any**](dx-graphics-hlsl-any.md) intrínseca con una variable de varios componentes.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-137">The comparison operators require a single component to work unless you use the [**all**](dx-graphics-hlsl-all.md) or [**any**](dx-graphics-hlsl-any.md) intrinsic function with a multiple-component variable.</span></span> <span data-ttu-id="b5f0e-138">Se produce un error en la siguiente operación porque la instrucción If requiere un solo booleano, pero recibe un bool4:</span><span class="sxs-lookup"><span data-stu-id="b5f0e-138">The following operation fails because the if statement requires a single bool but receives a bool4:</span></span>


```
if (A4 < B4)
```



<span data-ttu-id="b5f0e-139">Las siguientes operaciones se realizan correctamente:</span><span class="sxs-lookup"><span data-stu-id="b5f0e-139">The following operations succeed:</span></span>


```
if ( any(A4 < B4) )
if ( all(A4 < B4) )
```



<span data-ttu-id="b5f0e-140">Los operadores de conversión binaria [**Interfloat**](dx-graphics-hlsl-asfloat.md), [**asint**](dx-graphics-hlsl-asint.md)y así sucesivamente en el trabajo por componente, excepto en un [**valor Double**](asdouble.md) cuyas reglas especiales están documentadas.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-140">The binary cast operators [**asfloat**](dx-graphics-hlsl-asfloat.md), [**asint**](dx-graphics-hlsl-asint.md), and so on work per component except for [**asdouble**](asdouble.md) whose special rules are documented.</span></span>

<span data-ttu-id="b5f0e-141">Los operadores de selección como el punto, la coma y los corchetes de matriz no funcionan por componente.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-141">Selection operators like period, comma, and array brackets do not work per component.</span></span>

<span data-ttu-id="b5f0e-142">Los operadores de conversión cambian el número de componentes.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-142">Cast operators change the number of components.</span></span> <span data-ttu-id="b5f0e-143">Las siguientes operaciones de conversión muestran su equivalencia:</span><span class="sxs-lookup"><span data-stu-id="b5f0e-143">The following cast operations show their equivalence:</span></span>


```
(float) i4 ->   float(i4.x)
(float4)i ->   float4(i, i, i, i)
```



## <a name="additive-and-multiplicative-operators"></a><span data-ttu-id="b5f0e-144">Operadores de suma y multiplicación</span><span class="sxs-lookup"><span data-stu-id="b5f0e-144">Additive and Multiplicative Operators</span></span>

<span data-ttu-id="b5f0e-145">Los operadores de suma y multiplicación son: +,-, \* ,/,%</span><span class="sxs-lookup"><span data-stu-id="b5f0e-145">The additive and multiplicative operators are: +, -, \*, /, %</span></span>


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



<span data-ttu-id="b5f0e-146">El operador de módulo devuelve el resto de una división.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-146">The modulus operator returns the remainder of a division.</span></span> <span data-ttu-id="b5f0e-147">Esto produce resultados diferentes cuando se usan enteros y números de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-147">This produces different results when using integers and floating-point numbers.</span></span> <span data-ttu-id="b5f0e-148">Los restos de enteros que son fracciones se truncarán.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-148">Integer remainders that are fractional will be truncated.</span></span>


```
int i1 = 1;
int i2 = 2;
i3 = i1 % i2;      // i3 = remainder of 1/2, which is 1
i3 = i2 % i1;      // i3 = remainder of 2/1, which is 0
i3 = 5 % 2;        // i3 = remainder of 5/2, which is 1
i3 = 9 % 2;        // i3 = remainder of 9/2, which is 1
```



<span data-ttu-id="b5f0e-149">El operador de módulo trunca un resto fraccionario cuando se usan enteros.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-149">The modulus operator truncates a fractional remainder when using integers.</span></span>


```
f3 = f1 % f2;      // f3 = remainder of 1.0/2.0, which is 0.5
f3 = f2 % f1;      // f3 = remainder of 2.0/1.0, which is 0.0
```



<span data-ttu-id="b5f0e-150">El operador% solo se define en los casos en los que ambos lados son positivos o ambos lados son negativos.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-150">The % operator is defined only in cases where either both sides are positive or both sides are negative.</span></span> <span data-ttu-id="b5f0e-151">A diferencia de C, también funciona en tipos de datos de punto flotante, así como enteros.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-151">Unlike C, it also operates on floating-point data types, as well as integers.</span></span>

## <a name="array-operator"></a><span data-ttu-id="b5f0e-152">Array (operador)</span><span class="sxs-lookup"><span data-stu-id="b5f0e-152">Array Operator</span></span>

<span data-ttu-id="b5f0e-153">El operador de selección de miembro \[ de matriz "i \] " selecciona uno o más componentes de una matriz.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-153">The array member selection operator "\[i\]" selects one or more components in an array.</span></span> <span data-ttu-id="b5f0e-154">Es un conjunto de corchetes que contienen un índice basado en cero.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-154">It is a set of square brackets that contain a zero-based index.</span></span>


```
int arrayOfInts[4] = { 0,1,2,3 };
arrayOfInts[0] = 2;
arrayOfInts[1] = arrayOfInts[0];
```



<span data-ttu-id="b5f0e-155">El operador de matriz también se puede utilizar para tener acceso a un vector.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-155">The array operator can also be used to access a vector.</span></span>


```
float4 4D_Vector = { 0.0f, 1.0f, 2.0f, 3.0f  };         
float 1DFloat = 4D_Vector[1];          // 1.0f
```



<span data-ttu-id="b5f0e-156">Al agregar un índice adicional, el operador de matriz también puede tener acceso a una matriz.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-156">By adding an additional index, the array operator can also access a matrix.</span></span>


```
float4x4 mat4x4 = {{0,0,0,0}, {1,1,1,1}, {2,2,2,2}, {3,3,3,3} };
mat4x4[0][1] = 1.1f;
float 1DFloat = mat4x4[0][1];      // 0.0f
```



<span data-ttu-id="b5f0e-157">El primer índice es el índice de fila basado en cero.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-157">The first index is the zero-based row index.</span></span> <span data-ttu-id="b5f0e-158">El segundo índice es el índice de columna basado en cero.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-158">The second index is the zero-based column index.</span></span>

## <a name="assignment-operators"></a><span data-ttu-id="b5f0e-159">Operadores de asignación</span><span class="sxs-lookup"><span data-stu-id="b5f0e-159">Assignment Operators</span></span>

<span data-ttu-id="b5f0e-160">Los operadores de asignación son: =, + =,-=, \* =,/=</span><span class="sxs-lookup"><span data-stu-id="b5f0e-160">The assignment operators are: =, +=, -=, \*=, /=</span></span>

<span data-ttu-id="b5f0e-161">A las variables se les pueden asignar valores literales:</span><span class="sxs-lookup"><span data-stu-id="b5f0e-161">Variables can be assigned literal values:</span></span>


```
int i = 1;            
float f2 = 3.1f; 
bool b = false;
string str = "string";
```



<span data-ttu-id="b5f0e-162">También se puede asignar el resultado de una operación matemática a las variables:</span><span class="sxs-lookup"><span data-stu-id="b5f0e-162">Variables can also be assigned the result of a mathematical operation:</span></span>


```
int i1 = 1;
i1 += 2;           // i1 = 1 + 2 = 3
```



<span data-ttu-id="b5f0e-163">Se puede usar una variable en cualquier lado del signo igual:</span><span class="sxs-lookup"><span data-stu-id="b5f0e-163">A variable can be used on either side of the equals sign:</span></span>


```
float f3 = 0.5f;
f3 *= f3;          // f3 = 0.5 * 0.5 = 0.25
```



<span data-ttu-id="b5f0e-164">La división de las variables de punto flotante es la esperada porque el resto decimal no es un problema.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-164">Division for floating-point variables is as expected because decimal remainders are not a problem.</span></span>


```
float f1 = 1.0;
f1 /= 3.0f;        // f1 = 1.0/3.0 = 0.333
```



<span data-ttu-id="b5f0e-165">Tenga cuidado si usa enteros que se pueden dividir, especialmente cuando el truncamiento afecta al resultado.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-165">Be careful if you are using integers that may get divided, especially when truncation affects the result.</span></span> <span data-ttu-id="b5f0e-166">Este ejemplo es idéntico al ejemplo anterior, excepto para el tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-166">This example is identical to the previous example, except for the data type.</span></span> <span data-ttu-id="b5f0e-167">El truncamiento produce un resultado muy diferente.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-167">The truncation causes a very different result.</span></span>


```
int i1 = 1;
i1 /= 3;           // i1 = 1/3 = 0.333, which gets truncated to 0
```



## <a name="binary-casts"></a><span data-ttu-id="b5f0e-168">Conversiones binarias</span><span class="sxs-lookup"><span data-stu-id="b5f0e-168">Binary Casts</span></span>

<span data-ttu-id="b5f0e-169">La operación de conversión entre int y Float convertirá el valor numérico en las representaciones adecuadas después de las reglas de C para truncar un tipo int.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-169">Casting operation between int and float will convert the numeric value into the appropriate representations following C rules for truncating an int type.</span></span> <span data-ttu-id="b5f0e-170">La conversión de un valor de Float a int y de nuevo a un valor Float producirá una conversión de pérdida basada en la precisión del destino.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-170">Casting a value from a float to an int and back to a float will result in a lossy conversion based on the precision of the target.</span></span>

<span data-ttu-id="b5f0e-171">Las conversiones binarias también se pueden realizar mediante [**funciones intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md), que reinterpretan la representación de bits de un número en el tipo de datos de destino.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-171">Binary casts may also be performed using [**Intrinsic Functions (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md), which reinterpret the bit representation of a number into the target data type.</span></span>


```
asfloat() // Cast to float
asint()   // Cast to int 
asuint()  // Cast to uint
```



## <a name="bitwise-operators"></a><span data-ttu-id="b5f0e-172">Operadores bit a bit</span><span class="sxs-lookup"><span data-stu-id="b5f0e-172">Bitwise Operators</span></span>

<span data-ttu-id="b5f0e-173">HLSL admite los siguientes operadores bit a bit, que tienen la misma prioridad que C con respecto a otros operadores.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-173">HLSL supports the following bitwise operators, which follow the same precedence as C with regard to other operators.</span></span> <span data-ttu-id="b5f0e-174">En la tabla siguiente se describen los operadores.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-174">The following table describes the operators.</span></span>

> [!Note]  
> <span data-ttu-id="b5f0e-175">Los operadores bit a bit requieren el [modelo de sombreador 4 \_ 0](dx-graphics-hlsl-sm4.md) con Direct3D 10 y un hardware superior.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-175">Bitwise operators require [Shader Model 4\_0](dx-graphics-hlsl-sm4.md) with Direct3D 10 and higher hardware.</span></span>

 



|           |                   |
|-----------|-------------------|
| <span data-ttu-id="b5f0e-176">Operador</span><span class="sxs-lookup"><span data-stu-id="b5f0e-176">Operator</span></span>  | <span data-ttu-id="b5f0e-177">Función</span><span class="sxs-lookup"><span data-stu-id="b5f0e-177">Function</span></span>          |
| ~         | <span data-ttu-id="b5f0e-178">Not lógico</span><span class="sxs-lookup"><span data-stu-id="b5f0e-178">Logical Not</span></span>       |
| <<  | <span data-ttu-id="b5f0e-179">Desplazamiento a la izquierda</span><span class="sxs-lookup"><span data-stu-id="b5f0e-179">Left Shift</span></span>        |
| >>  | <span data-ttu-id="b5f0e-180">Desplazamiento a la derecha</span><span class="sxs-lookup"><span data-stu-id="b5f0e-180">Right Shift</span></span>       |
| &         | <span data-ttu-id="b5f0e-181">Logical And</span><span class="sxs-lookup"><span data-stu-id="b5f0e-181">Logical And</span></span>       |
| \|        | <span data-ttu-id="b5f0e-182">Or lógico.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-182">Logical Or</span></span>        |
| ^         | <span data-ttu-id="b5f0e-183">XOR lógico</span><span class="sxs-lookup"><span data-stu-id="b5f0e-183">Logical Xor</span></span>       |
| <<= | <span data-ttu-id="b5f0e-184">Igual a la izquierda</span><span class="sxs-lookup"><span data-stu-id="b5f0e-184">Left Shift Equal</span></span>  |
| >>= | <span data-ttu-id="b5f0e-185">Desplazamiento a la derecha</span><span class="sxs-lookup"><span data-stu-id="b5f0e-185">Right Shift Equal</span></span> |
| &=        | <span data-ttu-id="b5f0e-186">Y igual</span><span class="sxs-lookup"><span data-stu-id="b5f0e-186">And Equal</span></span>         |
| \|=       | <span data-ttu-id="b5f0e-187">O igual</span><span class="sxs-lookup"><span data-stu-id="b5f0e-187">Or Equal</span></span>          |
| ^=        | <span data-ttu-id="b5f0e-188">XOR igual</span><span class="sxs-lookup"><span data-stu-id="b5f0e-188">Xor Equal</span></span>         |



 

<span data-ttu-id="b5f0e-189">Los operadores bit a bit se definen para funcionar solo en los tipos de datos int y uint.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-189">Bitwise operators are defined to operate only on int and uint data types.</span></span> <span data-ttu-id="b5f0e-190">Si se intenta usar operadores bit a bit en tipos de datos float o struct, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-190">Attempting to use bitwise operators on float, or struct data types will result in an error.</span></span>

## <a name="boolean-math-operators"></a><span data-ttu-id="b5f0e-191">Operadores matemáticos booleanos</span><span class="sxs-lookup"><span data-stu-id="b5f0e-191">Boolean Math Operators</span></span>

<span data-ttu-id="b5f0e-192">Los operadores matemáticos booleanos son:  &&, \| \| ,?:</span><span class="sxs-lookup"><span data-stu-id="b5f0e-192">The Boolean math operators are: &&, \|\|, ?:</span></span>


```
bool b1 = true;
bool b2 = false;
bool b3 = b1 && b2 // b3 = true AND false = false
b3 = b1 || b2                // b3 = true OR false = true
```



<span data-ttu-id="b5f0e-193">A diferencia de la evaluación de cortocircuito de &&, \| \| y?: en C, las expresiones de HLSL nunca cortocircuitan una evaluación porque son operaciones vectoriales.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-193">Unlike short-circuit evaluation of &&, \|\|, and ?: in C, HLSL expressions never short-circuit an evaluation because they are vector operations.</span></span> <span data-ttu-id="b5f0e-194">Siempre se evalúan todos los lados de la expresión.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-194">All sides of the expression are always evaluated.</span></span>

<span data-ttu-id="b5f0e-195">Los operadores booleanos funcionan por componente.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-195">Boolean operators function on a per-component basis.</span></span> <span data-ttu-id="b5f0e-196">Esto significa que si se comparan dos vectores, el resultado es un vector que contiene el resultado booleano de la comparación de cada componente.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-196">This means that if you compare two vectors, the result is a vector containing the Boolean result of the comparison for each component.</span></span>

<span data-ttu-id="b5f0e-197">En el caso de las expresiones que usan operadores booleanos, el tamaño y el tipo de componente de cada variable se promueven a la misma antes de que se produzca la operación.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-197">For expressions that use Boolean operators, the size and component type of each variable are promoted to be the same before the operation occurs.</span></span> <span data-ttu-id="b5f0e-198">El tipo promocionado determina la resolución en la que tiene lugar la operación, así como el tipo de resultado de la expresión.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-198">The promoted type determines the resolution at which the operation takes place, as well as the result type of the expression.</span></span> <span data-ttu-id="b5f0e-199">Por ejemplo, una expresión INT3 + float se promocionaría a float3 + float3 para su evaluación, y su resultado sería de tipo float3.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-199">For example an int3 + float expression would be promoted to float3 + float3 for evaluation, and its result would be of type float3.</span></span>

## <a name="cast-operator"></a><span data-ttu-id="b5f0e-200">Operador de conversión</span><span class="sxs-lookup"><span data-stu-id="b5f0e-200">Cast Operator</span></span>

<span data-ttu-id="b5f0e-201">Una expresión precedida por un nombre de tipo entre paréntesis es una conversión de tipo explícita.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-201">An expression preceded by a type name in parenthesis is an explicit type cast.</span></span> <span data-ttu-id="b5f0e-202">Una conversión de tipos convierte la expresión original al tipo de datos de la conversión.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-202">A type cast converts the original expression to the data type of the cast.</span></span> <span data-ttu-id="b5f0e-203">En general, los tipos de datos simples se pueden convertir en tipos de datos más complejos (con una conversión de promoción), pero solo algunos tipos de datos complejos se pueden convertir en tipos de datos simples (con una conversión de degradación).</span><span class="sxs-lookup"><span data-stu-id="b5f0e-203">In general, the simple data types can be cast to the more complex data types (with a promotion cast), but only some complex data types can be cast into simple data types (with a demotion cast).</span></span>

<span data-ttu-id="b5f0e-204">Solo la conversión de tipo del lado derecho es legal.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-204">Only right hand side type casting is legal.</span></span> <span data-ttu-id="b5f0e-205">Por ejemplo, las expresiones como `(int)myFloat = myInt;` no son válidas.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-205">For example, expressions such as `(int)myFloat = myInt;` are illegal.</span></span> <span data-ttu-id="b5f0e-206">En su lugar, use `myFloat = (float)myInt;`.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-206">Use `myFloat = (float)myInt;` instead.</span></span>

<span data-ttu-id="b5f0e-207">El compilador también realiza una conversión de tipos implícita.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-207">The compiler also performs implicit type cast.</span></span> <span data-ttu-id="b5f0e-208">Por ejemplo, las dos expresiones siguientes son equivalentes:</span><span class="sxs-lookup"><span data-stu-id="b5f0e-208">For example, the following two expressions are equivalent:</span></span>


```
int2 b = int2(1,2) + 2;
int2 b = int2(1,2) + int2(2,2);
```



## <a name="comma-operator"></a><span data-ttu-id="b5f0e-209">Coma (operador)</span><span class="sxs-lookup"><span data-stu-id="b5f0e-209">Comma Operator</span></span>

<span data-ttu-id="b5f0e-210">El operador de coma (,) separa una o más expresiones que se van a evaluar en orden.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-210">The comma operator (,) separates one or more expressions that are to be evaluated in order.</span></span> <span data-ttu-id="b5f0e-211">El valor de la última expresión de la secuencia se usa como el valor de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-211">The value of the last expression in the sequence is used as the value of the sequence.</span></span>

<span data-ttu-id="b5f0e-212">Este es un caso que merece la pena llamar a.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-212">Here is one case worth calling attention to.</span></span> <span data-ttu-id="b5f0e-213">Si el tipo de constructor se deja accidentalmente fuera del lado derecho del signo igual, el lado derecho contiene ahora cuatro expresiones, separadas por tres comas.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-213">If the constructor type is accidentally left off the right side of the equals sign, the right side now contains four expressions, separated by three commas.</span></span>


```
// Instead of using a constructor
float4 x = float4(0,0,0,1); 

// The type on the right side is accidentally left off
float4 x = (0,0,0,1); 
```



<span data-ttu-id="b5f0e-214">El operador de comas evalúa una expresión de izquierda a derecha.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-214">The comma operator evaluates an expression from left to right.</span></span> <span data-ttu-id="b5f0e-215">Esto reduce el lado derecho a:</span><span class="sxs-lookup"><span data-stu-id="b5f0e-215">This reduces the right hand side to:</span></span>


```
float4 x = 1; 
```



<span data-ttu-id="b5f0e-216">En este caso, HLSL usa la promoción escalar, por lo que el resultado es como si se hubiera escrito como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="b5f0e-216">HLSL uses scalar promotion in this case, so the result is as if this were written as follows:</span></span>


```
float4 x = float4(1,1,1,1);
```



<span data-ttu-id="b5f0e-217">En esta instancia, salir del tipo FLOAT4 del lado derecho es probablemente un error que el compilador no puede detectar porque es una instrucción válida.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-217">In this instance, leaving off the float4 type from the right side is probably a mistake that the compiler is unable to detect because this is a valid statement.</span></span>

## <a name="comparison-operators"></a><span data-ttu-id="b5f0e-218">Operadores de comparación</span><span class="sxs-lookup"><span data-stu-id="b5f0e-218">Comparison Operators</span></span>

<span data-ttu-id="b5f0e-219">Los operadores de comparación son: <, >, = =,! =, <=, >=.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-219">The comparison operators are: <, >, ==, !=, <=, >=.</span></span>

<span data-ttu-id="b5f0e-220">Compara los valores que son mayores que (o menor que) con cualquier valor escalar:</span><span class="sxs-lookup"><span data-stu-id="b5f0e-220">Compare values that are greater than (or less than) any scalar value:</span></span>


```
if( dot(lightDirection, normalVector) > 0 )
   // Do something; the face is lit
```




```
if( dot(lightDirection, normalVector) < 0 )
   // Do nothing; the face is backwards
```



<span data-ttu-id="b5f0e-221">O bien, compare los valores iguales a (o no igual a) con cualquier valor escalar:</span><span class="sxs-lookup"><span data-stu-id="b5f0e-221">Or, compare values equal to (or not equal to) any scalar value:</span></span>


```
if(color.a == 0)
   // Skip processing because the face is invisible

if(color.a != 0)
   // Blend two colors together using the alpha value
```



<span data-ttu-id="b5f0e-222">O combinan y comparan valores que son mayores o iguales que (o menor o igual que) cualquier valor escalar:</span><span class="sxs-lookup"><span data-stu-id="b5f0e-222">Or combine both and compare values that are greater than or equal to (or less than or equal to) any scalar value:</span></span>


```
if( position.z >= oldPosition.z )
   // Skip the new face because it is behind the existing face
```




```
if( currentValue <= someInitialCondition )
   // Reset the current value to its initial condition
```



<span data-ttu-id="b5f0e-223">Cada una de estas comparaciones se puede realizar con cualquier tipo de datos escalar.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-223">Each of these comparisons can be done with any scalar data type.</span></span>

<span data-ttu-id="b5f0e-224">Para usar operadores de comparación con tipos vectoriales y de matriz, utilice la función [**All**](dx-graphics-hlsl-all.md) o [**cualquier**](dx-graphics-hlsl-any.md) función intrínseca.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-224">To use comparison operators with vector and matrix types, use the [**all**](dx-graphics-hlsl-all.md) or [**any**](dx-graphics-hlsl-any.md) intrinsic function.</span></span>

<span data-ttu-id="b5f0e-225">Se produce un error en esta operación porque la instrucción If requiere un solo booleano, pero recibe un bool4:</span><span class="sxs-lookup"><span data-stu-id="b5f0e-225">This operation fails because the if statement requires a single bool but receives a bool4:</span></span>


```
if (A4 < B4)
```



<span data-ttu-id="b5f0e-226">Estas operaciones se realizan correctamente:</span><span class="sxs-lookup"><span data-stu-id="b5f0e-226">These operations succeed:</span></span>


```
if ( any(A4 < B4) )
if ( all(A4 < B4) )
```



## <a name="prefix-or-postfix-operators"></a><span data-ttu-id="b5f0e-227">Operadores de prefijo o postfijo</span><span class="sxs-lookup"><span data-stu-id="b5f0e-227">Prefix or Postfix Operators</span></span>

<span data-ttu-id="b5f0e-228">Los operadores prefix y postfijo son: + +,--.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-228">The prefix and postfix operators are: ++, --.</span></span> <span data-ttu-id="b5f0e-229">Los operadores de prefijo cambian el contenido de la variable antes de que se evalúe la expresión.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-229">Prefix operators change the contents of the variable before the expression is evaluated.</span></span> <span data-ttu-id="b5f0e-230">Los operadores de postfijo cambian el contenido de la variable una vez que se evalúa la expresión.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-230">Postfix operators change the contents of the variable after the expression is evaluated.</span></span>

<span data-ttu-id="b5f0e-231">En este caso, un bucle usa el contenido de i para realizar un seguimiento del recuento de bucles.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-231">In this case, a loop uses the contents of i to keep track of the loop count.</span></span>


```
float4 arrayOfFloats[4] = { 1.0f, 2.0f, 3.0f, 4.4f };

for (int i = 0; i<4; )
{
    arrayOfFloats[i++] *= 2; 
}
```



<span data-ttu-id="b5f0e-232">Dado que se usa el operador de incremento de postfijo (+ +), arrayOfFloats \[ i \] se multiplica por 2 antes de incrementar.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-232">Because the postfix increment operator (++) is used, arrayOfFloats\[i\] is multiplied by 2 before i is incremented.</span></span> <span data-ttu-id="b5f0e-233">Esto podría reorganizarse ligeramente para usar el operador de incremento de prefijo.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-233">This could be slightly rearranged to use the prefix increment operator.</span></span> <span data-ttu-id="b5f0e-234">Este es más difícil de leer, aunque ambos ejemplos son equivalentes.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-234">This one is harder to read, although both examples are equivalent.</span></span>


```
float4 arrayOfFloats[4] = { 1.0f, 2.0f, 3.0f, 4.4f };

for (int i = 0; i<4; )
{
    arrayOfFloats[++i - 1] *= 2; 
}
```



<span data-ttu-id="b5f0e-235">Dado que se usa el operador de prefijo (+ +), arrayOfFloats \[ i + 1-1 \] se multiplica por 2 después de incrementar.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-235">Because the prefix operator (++) is used, arrayOfFloats\[i+1 - 1\] is multiplied by 2 after i is incremented.</span></span>

<span data-ttu-id="b5f0e-236">El operador de decremento de prefijo y postfijo de decremento (--) se aplican en la misma secuencia que el operador de incremento.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-236">The prefix decrement and postfix decrement operator (--) are applied in the same sequence as the increment operator.</span></span> <span data-ttu-id="b5f0e-237">La diferencia es que decremento resta 1 en lugar de agregar 1.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-237">The difference is that decrement subtracts 1 instead of adding 1.</span></span>

## <a name="structure-operator"></a><span data-ttu-id="b5f0e-238">Operador de estructura</span><span class="sxs-lookup"><span data-stu-id="b5f0e-238">Structure Operator</span></span>

<span data-ttu-id="b5f0e-239">El operador de selección de miembros de estructura (.) es un punto.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-239">The structure member selection operator (.) is a period.</span></span> <span data-ttu-id="b5f0e-240">Dada esta estructura:</span><span class="sxs-lookup"><span data-stu-id="b5f0e-240">Given this structure:</span></span>


```
struct position
{
float4 x;
float4 y;
float4 z;
};
```



<span data-ttu-id="b5f0e-241">Se puede leer de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="b5f0e-241">It can be read like this:</span></span>


```
struct position pos = { 1,2,3 };

float 1D_Float = pos.x
1D_Float = pos.y
```



<span data-ttu-id="b5f0e-242">Cada miembro se puede leer o escribir con el operador de estructura:</span><span class="sxs-lookup"><span data-stu-id="b5f0e-242">Each member can be read or written with the structure operator:</span></span>


```
struct position pos = { 1,2,3 };
pos.x = 2.0f;
pos.z = 1.0f;       // z = 1.0f
pos.z = pos.x      // z = 2.0f
```



## <a name="unary-operators"></a><span data-ttu-id="b5f0e-243">Operadores unarios</span><span class="sxs-lookup"><span data-stu-id="b5f0e-243">Unary Operators</span></span>

<span data-ttu-id="b5f0e-244">Los operadores unarios son:!,-, +</span><span class="sxs-lookup"><span data-stu-id="b5f0e-244">The unary operators are: !, -, +</span></span>

<span data-ttu-id="b5f0e-245">Los operadores unarios operan en un solo operando.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-245">Unary operators operate on a single operand.</span></span>


```
bool b = false;
bool b2 = !b;      // b2 = true
int i = 2;
int i2 = -i;       // i2 = -2
int j = +i2;       // j = +2
```



## <a name="operator-precedence"></a><span data-ttu-id="b5f0e-246">Prioridad de los operadores</span><span class="sxs-lookup"><span data-stu-id="b5f0e-246">Operator Precedence</span></span>

<span data-ttu-id="b5f0e-247">Cuando una expresión contiene más de un operador, la precedencia del operador determina el orden de evaluación.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-247">When an expression contains more than one operator, operator precedence determines the order of evaluation.</span></span> <span data-ttu-id="b5f0e-248">La prioridad de operador para HLSL sigue la misma prioridad que C.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-248">Operator precedence for HLSL follows the same precedence as C.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5f0e-249">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b5f0e-249">Remarks</span></span>

<span data-ttu-id="b5f0e-250">Las llaves ( {,} ) inician y finalizan un bloque de instrucciones.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-250">Curly braces ({,}) start and end a statement block.</span></span> <span data-ttu-id="b5f0e-251">Cuando un bloque de instrucciones utiliza una única instrucción, las llaves son opcionales.</span><span class="sxs-lookup"><span data-stu-id="b5f0e-251">When a statement block uses a single statement, the curly braces are optional.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b5f0e-252">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b5f0e-252">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5f0e-253">Instrucciones (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b5f0e-253">Statements (DirectX HLSL)</span></span>](dx-graphics-hlsl-statements.md)
</dt> </dl>

 

 




