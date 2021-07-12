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
ms.openlocfilehash: 5cd065e415aafffa59dd6c31d2b9aa4f4505021d
ms.sourcegitcommit: 7c7a05f65d2cf1ba2dadf05f63ae91a048083946
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "113589592"
---
# <a name="per-component-math-operations"></a><span data-ttu-id="0b883-103">Per-Component operaciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="0b883-103">Per-Component Math Operations</span></span>

<span data-ttu-id="0b883-104">Con HLSL, puede programar sombreadores en un nivel de algoritmo.</span><span class="sxs-lookup"><span data-stu-id="0b883-104">With HLSL, you can program shaders at an algorithm level.</span></span> <span data-ttu-id="0b883-105">Para entender el lenguaje, deberá saber cómo declarar variables y funciones, usar funciones intrínsecas, definir tipos de datos personalizados y usar semántica para conectar argumentos de sombreador a otros sombreadores y a la canalización.</span><span class="sxs-lookup"><span data-stu-id="0b883-105">To understand the language, you will need to know how to declare variables and functions, use intrinsic functions, define custom data types and use semantics to connect shader arguments to other shaders and to the pipeline.</span></span>

<span data-ttu-id="0b883-106">Una vez que aprenda a crear sombreadores en HLSL, deberá obtener información sobre las llamadas API para que pueda: compilar un sombreador para hardware determinado, inicializar constantes de sombreador e inicializar otro estado de canalización si es necesario.</span><span class="sxs-lookup"><span data-stu-id="0b883-106">Once you learn how to author shaders in HLSL, you will need to learn about API calls so that you can: compile a shader for particular hardware, initialize shader constants, and initialize other pipeline state if necessary.</span></span>

-   [<span data-ttu-id="0b883-107">Tipo de vector</span><span class="sxs-lookup"><span data-stu-id="0b883-107">The Vector Type</span></span>](#the-vector-type)
-   [<span data-ttu-id="0b883-108">El tipo de matriz</span><span class="sxs-lookup"><span data-stu-id="0b883-108">The Matrix Type</span></span>](#the-matrix-type)
    -   [<span data-ttu-id="0b883-109">Ordenación de matrices</span><span class="sxs-lookup"><span data-stu-id="0b883-109">Matrix Ordering</span></span>](#matrix-ordering)
-   [<span data-ttu-id="0b883-110">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="0b883-110">Examples</span></span>](#examples)
-   [<span data-ttu-id="0b883-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0b883-111">Related topics</span></span>](#related-topics)

## <a name="the-vector-type"></a><span data-ttu-id="0b883-112">Tipo de vector</span><span class="sxs-lookup"><span data-stu-id="0b883-112">The Vector Type</span></span>

<span data-ttu-id="0b883-113">Un vector es una estructura de datos que contiene entre uno y cuatro componentes.</span><span class="sxs-lookup"><span data-stu-id="0b883-113">A vector is a data structure that contains between one and four components.</span></span>


```
bool    bVector;   // scalar containing 1 Boolean
bool1   bVector;   // vector containing 1 Boolean
int1    iVector;   // vector containing 1 int
float3  fVector;   // vector containing 3 floats
double4 dVector;   // vector containing 4 doubles
```



<span data-ttu-id="0b883-114">El entero inmediatamente después del tipo de datos es el número de componentes del vector.</span><span class="sxs-lookup"><span data-stu-id="0b883-114">The integer immediately following the data type is the number of components on the vector.</span></span>

<span data-ttu-id="0b883-115">Los inicializadores también se pueden incluir en las declaraciones.</span><span class="sxs-lookup"><span data-stu-id="0b883-115">Initializers can also be included in the declarations.</span></span>


```
bool    bVector = false;
int1    iVector = 1;
float3  fVector = { 0.2f, 0.3f, 0.4f };
double4 dVector = { 0.2, 0.3, 0.4, 0.5 };
```



<span data-ttu-id="0b883-116">Como alternativa, el tipo de vector se puede usar para realizar las mismas declaraciones:</span><span class="sxs-lookup"><span data-stu-id="0b883-116">Alternatively, the vector type can be used to make the same declarations:</span></span>


```
vector <bool,   1> bVector = false;
vector <int,    1> iVector = 1;
vector <float,  3> fVector = { 0.2f, 0.3f, 0.4f };
vector <double, 4> dVector = { 0.2, 0.3, 0.4, 0.5 };
```



<span data-ttu-id="0b883-117">El tipo de vector usa corchetes angulares para especificar el tipo y el número de componentes.</span><span class="sxs-lookup"><span data-stu-id="0b883-117">The vector type uses angle brackets to specify the type and number of components.</span></span>

<span data-ttu-id="0b883-118">Los vectores contienen hasta cuatro componentes, a los que se puede acceder mediante uno de los dos conjuntos de nomenclatura:</span><span class="sxs-lookup"><span data-stu-id="0b883-118">Vectors contain up to four components, each of which can be accessed using one of two naming sets:</span></span>

-   <span data-ttu-id="0b883-119">El conjunto de posiciones: x,y,z,w</span><span class="sxs-lookup"><span data-stu-id="0b883-119">The position set: x,y,z,w</span></span>
-   <span data-ttu-id="0b883-120">El conjunto de colores: r,g,b,a</span><span class="sxs-lookup"><span data-stu-id="0b883-120">The color set: r,g,b,a</span></span>

<span data-ttu-id="0b883-121">Ambas instrucciones devuelven el valor en el tercer componente.</span><span class="sxs-lookup"><span data-stu-id="0b883-121">These statements both return the value in the third component.</span></span>


```
// Given
float4 pos = float4(0,0,2,1);

pos.z    // value is 2
pos.b    // value is 2
```



<span data-ttu-id="0b883-122">Los conjuntos de nombres pueden usar uno o varios componentes, pero no se pueden mezclar.</span><span class="sxs-lookup"><span data-stu-id="0b883-122">Naming sets can use one or more components, but they cannot be mixed.</span></span>


```
// Given
float4 pos = float4(0,0,2,1);
float2 temp;

temp = pos.xy  // valid
temp = pos.rg  // valid

temp = pos.xg  // NOT VALID because the position and color sets were used.
```



<span data-ttu-id="0b883-123">La especificación de uno o varios componentes vectoriales al leer componentes se denomina deslizar.</span><span class="sxs-lookup"><span data-stu-id="0b883-123">Specifying one or more vector components when reading components is called swizzling.</span></span> <span data-ttu-id="0b883-124">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="0b883-124">For example:</span></span>


```
float4 pos = float4(0,0,2,1);
float2 f_2D;
f_2D = pos.xy;   // read two components 
f_2D = pos.xz;   // read components in any order       
f_2D = pos.zx;

f_2D = pos.xx;   // components can be read more than once
f_2D = pos.yy;
```



<span data-ttu-id="0b883-125">El enmascaramiento controla cuántos componentes se escriben.</span><span class="sxs-lookup"><span data-stu-id="0b883-125">Masking controls how many components are written.</span></span>


```
float4 pos = float4(0,0,2,1);
float4 f_4D;
f_4D    = pos;     // write four components          

f_4D.xz = pos.xz;  // write two components        
f_4D.zx = pos.xz;  // change the write order

f_4D.xzyw = pos.w; // write one component to more than one component
f_4D.wzyx = pos;
```



<span data-ttu-id="0b883-126">Las asignaciones no se pueden escribir en el mismo componente más de una vez.</span><span class="sxs-lookup"><span data-stu-id="0b883-126">Assignments cannot be written to the same component more than once.</span></span> <span data-ttu-id="0b883-127">Por lo tanto, el lado izquierdo de esta instrucción no es válido:</span><span class="sxs-lookup"><span data-stu-id="0b883-127">So the left side of this statement is invalid:</span></span>


```
f_4D.xx = pos.xy;   // cannot write to the same destination components 
```



<span data-ttu-id="0b883-128">Además, los espacios de nombres de componente no se pueden mezclar.</span><span class="sxs-lookup"><span data-stu-id="0b883-128">Also, the component name spaces cannot be mixed.</span></span> <span data-ttu-id="0b883-129">Se trata de una escritura de componente no válida:</span><span class="sxs-lookup"><span data-stu-id="0b883-129">This is an invalid component write:</span></span>


```
f_4D.xg = pos.rgrg;    // invalid write: cannot mix component name spaces 
```



<span data-ttu-id="0b883-130">El acceso a un vector como escalar accederá al primer componente del vector.</span><span class="sxs-lookup"><span data-stu-id="0b883-130">Accessing a vector as a scalar will access the first component of the vector.</span></span> <span data-ttu-id="0b883-131">Las dos instrucciones siguientes son equivalentes.</span><span class="sxs-lookup"><span data-stu-id="0b883-131">The following two statements are equivalent.</span></span>


```
f_4D.a = pos * 5.0f;
f_4D.a = pos.r * 5.0f;
```



## <a name="the-matrix-type"></a><span data-ttu-id="0b883-132">El tipo de matriz</span><span class="sxs-lookup"><span data-stu-id="0b883-132">The Matrix Type</span></span>

<span data-ttu-id="0b883-133">Una matriz es una estructura de datos que contiene filas y columnas de datos.</span><span class="sxs-lookup"><span data-stu-id="0b883-133">A matrix is a data structure that contains rows and columns of data.</span></span> <span data-ttu-id="0b883-134">Los datos pueden ser cualquiera de los tipos de datos escalares, pero cada elemento de una matriz es el mismo tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="0b883-134">The data can be any of the scalar data types, however, every element of a matrix is the same data type.</span></span> <span data-ttu-id="0b883-135">El número de filas y columnas se especifica con la cadena fila por columna que se anexa al tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="0b883-135">The number of rows and columns is specified with the row-by-column string that is appended to the data type.</span></span>


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



<span data-ttu-id="0b883-136">El número máximo de filas o columnas es 4; el número mínimo es 1.</span><span class="sxs-lookup"><span data-stu-id="0b883-136">The maximum number of rows or columns is 4; the minimum number is 1.</span></span>

<span data-ttu-id="0b883-137">Una matriz se puede inicializar cuando se declara:</span><span class="sxs-lookup"><span data-stu-id="0b883-137">A matrix can be initialized when it is declared:</span></span>


```
float2x2 fMatrix = { 0.0f, 0.1, // row 1
                     2.1f, 2.2f // row 2
                   };   
```



<span data-ttu-id="0b883-138">O bien, el tipo de matriz se puede usar para realizar las mismas declaraciones:</span><span class="sxs-lookup"><span data-stu-id="0b883-138">Or, the matrix type can be used to make the same declarations:</span></span>


```
matrix <float, 2, 2> fMatrix = { 0.0f, 0.1, // row 1
                                 2.1f, 2.2f // row 2
                               };
```



<span data-ttu-id="0b883-139">El tipo de matriz usa los corchetes angulares para especificar el tipo, el número de filas y el número de columnas.</span><span class="sxs-lookup"><span data-stu-id="0b883-139">The matrix type uses the angle brackets to specify the type, the number of rows, and the number of columns.</span></span> <span data-ttu-id="0b883-140">En este ejemplo se crea una matriz de punto flotante, con dos filas y dos columnas.</span><span class="sxs-lookup"><span data-stu-id="0b883-140">This example creates a floating-point matrix, with two rows and two columns.</span></span> <span data-ttu-id="0b883-141">Se puede usar cualquiera de los tipos de datos escalares.</span><span class="sxs-lookup"><span data-stu-id="0b883-141">Any of the scalar data types can be used.</span></span>

<span data-ttu-id="0b883-142">Esta declaración define una matriz de valores float (números de punto flotante de 32 bits) con dos filas y tres columnas:</span><span class="sxs-lookup"><span data-stu-id="0b883-142">This declaration defines a matrix of float values (32-bit floating-point numbers) with two rows and three columns:</span></span>


```
matrix <float, 2, 3> fFloatMatrix;
```



<span data-ttu-id="0b883-143">Una matriz contiene valores organizados en filas y columnas, a los que se puede acceder mediante el operador de estructura "." seguido de uno de los dos conjuntos de nomenclatura:</span><span class="sxs-lookup"><span data-stu-id="0b883-143">A matrix contains values organized in rows and columns, which can be accessed using the structure operator "." followed by one of two naming sets:</span></span>

-   <span data-ttu-id="0b883-144">Posición de columna de fila de base cero:</span><span class="sxs-lookup"><span data-stu-id="0b883-144">The zero-based row-column position:</span></span>
    -   <span data-ttu-id="0b883-145">\_m00, \_ m01, \_ m02, \_ m03</span><span class="sxs-lookup"><span data-stu-id="0b883-145">\_m00, \_m01, \_m02, \_m03</span></span>
    -   <span data-ttu-id="0b883-146">\_m10, \_ m11, \_ m12, \_ m13</span><span class="sxs-lookup"><span data-stu-id="0b883-146">\_m10, \_m11, \_m12, \_m13</span></span>
    -   <span data-ttu-id="0b883-147">\_m20, \_ m21, \_ m22, \_ m23</span><span class="sxs-lookup"><span data-stu-id="0b883-147">\_m20, \_m21, \_m22, \_m23</span></span>
    -   <span data-ttu-id="0b883-148">\_m30, \_ m31, \_ m32, \_ m33</span><span class="sxs-lookup"><span data-stu-id="0b883-148">\_m30, \_m31, \_m32, \_m33</span></span>
-   <span data-ttu-id="0b883-149">Posición de columna de fila basada en uno:</span><span class="sxs-lookup"><span data-stu-id="0b883-149">The one-based row-column position:</span></span>
    -   <span data-ttu-id="0b883-150">\_11, \_ 12, \_ 13, \_ 14</span><span class="sxs-lookup"><span data-stu-id="0b883-150">\_11, \_12, \_13, \_14</span></span>
    -   <span data-ttu-id="0b883-151">\_21, \_ 22, \_ 23, \_ 24</span><span class="sxs-lookup"><span data-stu-id="0b883-151">\_21, \_22, \_23, \_24</span></span>
    -   <span data-ttu-id="0b883-152">\_31, \_ 32, \_ 33, \_ 34</span><span class="sxs-lookup"><span data-stu-id="0b883-152">\_31, \_32, \_33, \_34</span></span>
    -   <span data-ttu-id="0b883-153">\_41, \_ 42, \_ 43, \_ 44</span><span class="sxs-lookup"><span data-stu-id="0b883-153">\_41, \_42, \_43, \_44</span></span>

<span data-ttu-id="0b883-154">Cada conjunto de nombres comienza con un carácter de subrayado seguido del número de fila y el número de columna.</span><span class="sxs-lookup"><span data-stu-id="0b883-154">Each naming set starts with an underscore followed by the row number and the column number.</span></span> <span data-ttu-id="0b883-155">La convención de base cero también incluye la letra "m" antes del número de fila y columna.</span><span class="sxs-lookup"><span data-stu-id="0b883-155">The zero-based convention also includes the letter "m" before the row and column number.</span></span> <span data-ttu-id="0b883-156">Este es un ejemplo en el que se usan los dos conjuntos de nomenclatura para acceder a una matriz:</span><span class="sxs-lookup"><span data-stu-id="0b883-156">Here's an example that uses the two naming sets to access a matrix:</span></span>


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



<span data-ttu-id="0b883-157">Al igual que los vectores, los conjuntos de nombres pueden usar uno o varios componentes de cualquier conjunto de nomenclatura.</span><span class="sxs-lookup"><span data-stu-id="0b883-157">Just like vectors, naming sets can use one or more components from either naming set.</span></span>


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



<span data-ttu-id="0b883-158">También se puede acceder a una matriz mediante la notación de acceso de matriz, que es un conjunto de índices de base cero.</span><span class="sxs-lookup"><span data-stu-id="0b883-158">A matrix can also be accessed using array access notation, which is a zero-based set of indices.</span></span> <span data-ttu-id="0b883-159">Cada índice está entre corchetes.</span><span class="sxs-lookup"><span data-stu-id="0b883-159">Each index is inside of square brackets.</span></span> <span data-ttu-id="0b883-160">Se accede a una matriz 4x4 con los índices siguientes:</span><span class="sxs-lookup"><span data-stu-id="0b883-160">A 4x4 matrix is accessed with the following indices:</span></span>

-   <span data-ttu-id="0b883-161">\[0 \] \[ 0 \] , \[ 0 \] \[ 1 \] , \[ 0 \] \[ 2 \] , \[ 0 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="0b883-161">\[0\]\[0\], \[0\]\[1\], \[0\]\[2\], \[0\]\[3\]</span></span>
-   <span data-ttu-id="0b883-162">\[1 \] \[ \] 0, \[ 1 \] \[ \] 1, \[ 1 \] \[ \] 2, \[ 1 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="0b883-162">\[1\]\[0\], \[1\]\[1\], \[1\]\[2\], \[1\]\[3\]</span></span>
-   <span data-ttu-id="0b883-163">\[2 \] \[ \] 0, \[ 2 \] \[ \] 1, \[ 2 \] \[ 2 \] , \[ 2 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="0b883-163">\[2\]\[0\], \[2\]\[1\], \[2\]\[2\], \[2\]\[3\]</span></span>
-   <span data-ttu-id="0b883-164">\[3 \] \[ 0 \] , \[ 3 \] \[ 1 \] , \[ 3 \] \[ 2 \] , \[ 3 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="0b883-164">\[3\]\[0\], \[3\]\[1\], \[3\]\[2\], \[3\]\[3\]</span></span>

<span data-ttu-id="0b883-165">Este es un ejemplo de acceso a una matriz:</span><span class="sxs-lookup"><span data-stu-id="0b883-165">Here is an example of accessing a matrix:</span></span>


```
float2x2 fMatrix = { 1.0f, 1.1f, // row 1
                     2.0f, 2.1f  // row 2
                   };
float temp;

temp = fMatrix[0][0] // single component read
temp = fMatrix[0][1] // single component read
```



<span data-ttu-id="0b883-166">Observe que el operador de estructura "." no se usa para tener acceso a una matriz.</span><span class="sxs-lookup"><span data-stu-id="0b883-166">Notice that the structure operator "." is not used to access an array.</span></span> <span data-ttu-id="0b883-167">La notación de acceso de matriz no puede usar swling para leer más de un componente.</span><span class="sxs-lookup"><span data-stu-id="0b883-167">Array access notation cannot use swizzling to read more than one component.</span></span>


```
float2 temp;
temp = fMatrix[0][0]_[0][1] // invalid, cannot read two components
```



<span data-ttu-id="0b883-168">Sin embargo, el acceso a la matriz puede leer un vector de varios componentes.</span><span class="sxs-lookup"><span data-stu-id="0b883-168">However, array accessing can read a multi-component vector.</span></span>


```
float2 temp;
float2x2 fMatrix;
temp = fMatrix[0] // read the first row
```



<span data-ttu-id="0b883-169">Al igual que con los vectores, la lectura de más de un componente de matriz se denomina deslizar.</span><span class="sxs-lookup"><span data-stu-id="0b883-169">As with vectors, reading more than one matrix component is called swizzling.</span></span> <span data-ttu-id="0b883-170">Se puede asignar más de un componente, suponiendo que solo se usa un espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="0b883-170">More than one component can be assigned, assuming only one name space is used.</span></span> <span data-ttu-id="0b883-171">Todas estas son asignaciones válidas:</span><span class="sxs-lookup"><span data-stu-id="0b883-171">These are all valid assignments:</span></span>


```
// Given these variables
float4x4 worldMatrix = float4( {0,0,0,0}, {1,1,1,1}, {2,2,2,2}, {3,3,3,3} );
float4x4 tempMatrix;

tempMatrix._m00_m11 = worldMatrix._m00_m11; // multiple components
tempMatrix._m00_m11 = worldMatrix.m13_m23;

tempMatrix._11_22_33 = worldMatrix._11_22_33; // any order on swizzles
tempMatrix._11_22_33 = worldMatrix._24_23_22;
```



<span data-ttu-id="0b883-172">El enmascaramiento controla cuántos componentes se escriben.</span><span class="sxs-lookup"><span data-stu-id="0b883-172">Masking controls how many components are written.</span></span>


```
// Given
float4x4 worldMatrix = float4( {0,0,0,0}, {1,1,1,1}, {2,2,2,2}, {3,3,3,3} );
float4x4 tempMatrix;

tempMatrix._m00_m11 = worldMatrix._m00_m11; // write two components
tempMatrix._m23_m00 = worldMatrix._m00_m11;
```



<span data-ttu-id="0b883-173">Las asignaciones no se pueden escribir en el mismo componente más de una vez.</span><span class="sxs-lookup"><span data-stu-id="0b883-173">Assignments cannot be written to the same component more than once.</span></span> <span data-ttu-id="0b883-174">Por lo tanto, el lado izquierdo de esta instrucción no es válido:</span><span class="sxs-lookup"><span data-stu-id="0b883-174">So the left side of this statement is invalid:</span></span>


```
// cannot write to the same component more than once
tempMatrix._m00_m00 = worldMatrix._m00_m11;
```



<span data-ttu-id="0b883-175">Además, los espacios de nombres de componente no se pueden mezclar.</span><span class="sxs-lookup"><span data-stu-id="0b883-175">Also, the component name spaces cannot be mixed.</span></span> <span data-ttu-id="0b883-176">Se trata de una escritura de componente no válida:</span><span class="sxs-lookup"><span data-stu-id="0b883-176">This is an invalid component write:</span></span>


```
// Invalid use of same component on left side
tempMatrix._11_m23 = worldMatrix._11_22; 
```



### <a name="matrix-ordering"></a><span data-ttu-id="0b883-177">Ordenación de matrices</span><span class="sxs-lookup"><span data-stu-id="0b883-177">Matrix Ordering</span></span>

<span data-ttu-id="0b883-178">El orden de empaquetado de la matriz para los parámetros uniformes se establece en column-major de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="0b883-178">Matrix packing order for uniform parameters is set to column-major by default.</span></span> <span data-ttu-id="0b883-179">Esto significa que cada columna de la matriz se almacena en un único registro constante.</span><span class="sxs-lookup"><span data-stu-id="0b883-179">This means each column of the matrix is stored in a single constant register.</span></span> <span data-ttu-id="0b883-180">Por otro lado, una matriz principal de fila empaqueta cada fila de la matriz en un único registro constante.</span><span class="sxs-lookup"><span data-stu-id="0b883-180">On the other hand, a row-major matrix packs each row of the matrix in a single constant register.</span></span> <span data-ttu-id="0b883-181">El empaquetado de matriz se puede cambiar con la directiva de matriz **\# \_ pragmapack** o con la fila **\_ principal** o la palabra **clave principal \_ de** columna.</span><span class="sxs-lookup"><span data-stu-id="0b883-181">Matrix packing can be changed with the **\#pragmapack\_matrix** directive, or with the **row\_major** or the **column\_major** keyword.</span></span>

<span data-ttu-id="0b883-182">Los datos de una matriz se cargan en registros constantes de sombreador antes de que se ejecute un sombreador.</span><span class="sxs-lookup"><span data-stu-id="0b883-182">The data in a matrix is loaded into shader constant registers before a shader runs.</span></span> <span data-ttu-id="0b883-183">Hay dos opciones para leer los datos de la matriz: en orden principal de fila o en orden de columna principal.</span><span class="sxs-lookup"><span data-stu-id="0b883-183">There are two choices for how the matrix data is read: in row-major order or in column-major order.</span></span> <span data-ttu-id="0b883-184">El orden principal de columna significa que cada columna de matriz se almacenará en un único registro constante y el orden principal de fila significa que cada fila de la matriz se almacenará en un único registro constante.</span><span class="sxs-lookup"><span data-stu-id="0b883-184">Column-major order means that each matrix column will be stored in a single constant register, and row-major order means that each row of the matrix will be stored in a single constant register.</span></span> <span data-ttu-id="0b883-185">Esta es una consideración importante para el número de registros constantes que se usan para una matriz.</span><span class="sxs-lookup"><span data-stu-id="0b883-185">This is an important consideration for how many constant registers are used for a matrix.</span></span>

<span data-ttu-id="0b883-186">Una matriz principal de fila se dispone de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="0b883-186">A row-major matrix is laid out like the following:</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="0b883-187">11</span><span class="sxs-lookup"><span data-stu-id="0b883-187">11</span></span><br/>
        <span data-ttu-id="0b883-188">21</span><span class="sxs-lookup"><span data-stu-id="0b883-188">21</span></span><br/>
        <span data-ttu-id="0b883-189">31</span><span class="sxs-lookup"><span data-stu-id="0b883-189">31</span></span><br/>
        <span data-ttu-id="0b883-190">41</span><span class="sxs-lookup"><span data-stu-id="0b883-190">41</span></span><br/>
    :::column-end:::
    :::column:::
        <span data-ttu-id="0b883-191">12</span><span class="sxs-lookup"><span data-stu-id="0b883-191">12</span></span><br/>
        <span data-ttu-id="0b883-192">22</span><span class="sxs-lookup"><span data-stu-id="0b883-192">22</span></span><br/>
        <span data-ttu-id="0b883-193">32</span><span class="sxs-lookup"><span data-stu-id="0b883-193">32</span></span><br/>
        <span data-ttu-id="0b883-194">42</span><span class="sxs-lookup"><span data-stu-id="0b883-194">42</span></span><br/>
    :::column-end:::
    :::column:::
        <span data-ttu-id="0b883-195">13</span><span class="sxs-lookup"><span data-stu-id="0b883-195">13</span></span><br/>
        <span data-ttu-id="0b883-196">23</span><span class="sxs-lookup"><span data-stu-id="0b883-196">23</span></span><br/>
        <span data-ttu-id="0b883-197">33</span><span class="sxs-lookup"><span data-stu-id="0b883-197">33</span></span><br/>
        <span data-ttu-id="0b883-198">43</span><span class="sxs-lookup"><span data-stu-id="0b883-198">43</span></span><br/>
    :::column-end:::
    :::column:::
        <span data-ttu-id="0b883-199">14</span><span class="sxs-lookup"><span data-stu-id="0b883-199">14</span></span><br/>
        <span data-ttu-id="0b883-200">24</span><span class="sxs-lookup"><span data-stu-id="0b883-200">24</span></span><br/>
        <span data-ttu-id="0b883-201">34</span><span class="sxs-lookup"><span data-stu-id="0b883-201">34</span></span><br/>
        <span data-ttu-id="0b883-202">44</span><span class="sxs-lookup"><span data-stu-id="0b883-202">44</span></span><br/>
    :::column-end:::
:::row-end:::




 

<span data-ttu-id="0b883-203">Se dispone una matriz de columnas principales como la siguiente:</span><span class="sxs-lookup"><span data-stu-id="0b883-203">A column-major matrix is laid out like the following:</span></span>


:::row:::
    :::column:::
        <span data-ttu-id="0b883-204">11</span><span class="sxs-lookup"><span data-stu-id="0b883-204">11</span></span><br/>
        <span data-ttu-id="0b883-205">12</span><span class="sxs-lookup"><span data-stu-id="0b883-205">12</span></span><br/>
        <span data-ttu-id="0b883-206">13</span><span class="sxs-lookup"><span data-stu-id="0b883-206">13</span></span><br/>
        <span data-ttu-id="0b883-207">14</span><span class="sxs-lookup"><span data-stu-id="0b883-207">14</span></span><br/>
    :::column-end:::
    :::column:::
        <span data-ttu-id="0b883-208">21</span><span class="sxs-lookup"><span data-stu-id="0b883-208">21</span></span><br/>
        <span data-ttu-id="0b883-209">22</span><span class="sxs-lookup"><span data-stu-id="0b883-209">22</span></span><br/>
        <span data-ttu-id="0b883-210">23</span><span class="sxs-lookup"><span data-stu-id="0b883-210">23</span></span><br/>
        <span data-ttu-id="0b883-211">24</span><span class="sxs-lookup"><span data-stu-id="0b883-211">24</span></span><br/>
    :::column-end:::
    :::column:::
        <span data-ttu-id="0b883-212">31</span><span class="sxs-lookup"><span data-stu-id="0b883-212">31</span></span><br/>
        <span data-ttu-id="0b883-213">32</span><span class="sxs-lookup"><span data-stu-id="0b883-213">32</span></span><br/>
        <span data-ttu-id="0b883-214">33</span><span class="sxs-lookup"><span data-stu-id="0b883-214">33</span></span><br/>
        <span data-ttu-id="0b883-215">34</span><span class="sxs-lookup"><span data-stu-id="0b883-215">34</span></span><br/>
    :::column-end:::
    :::column:::
        <span data-ttu-id="0b883-216">41</span><span class="sxs-lookup"><span data-stu-id="0b883-216">41</span></span><br/>
        <span data-ttu-id="0b883-217">42</span><span class="sxs-lookup"><span data-stu-id="0b883-217">42</span></span><br/>
        <span data-ttu-id="0b883-218">43</span><span class="sxs-lookup"><span data-stu-id="0b883-218">43</span></span><br/>
        <span data-ttu-id="0b883-219">44</span><span class="sxs-lookup"><span data-stu-id="0b883-219">44</span></span><br/>
    :::column-end:::
:::row-end:::




 

<span data-ttu-id="0b883-220">El orden de la matriz principal de fila y de columna determina el orden en que se leen los componentes de la matriz de las entradas del sombreador.</span><span class="sxs-lookup"><span data-stu-id="0b883-220">Row-major and column-major matrix ordering determine the order the matrix components are read from shader inputs.</span></span> <span data-ttu-id="0b883-221">Una vez que los datos se escriben en registros constantes, el orden de la matriz no tiene ningún efecto en cómo se usa o se accede a los datos desde el código del sombreador.</span><span class="sxs-lookup"><span data-stu-id="0b883-221">Once the data is written into constant registers, matrix order has no effect on how the data is used or accessed from within shader code.</span></span> <span data-ttu-id="0b883-222">Además, las matrices declaradas en un cuerpo del sombreador no se empaquetan en registros constantes.</span><span class="sxs-lookup"><span data-stu-id="0b883-222">Also, matrices declared in a shader body do not get packed into constant registers.</span></span> <span data-ttu-id="0b883-223">El orden de empaquetado principal de fila y de columna principal no influye en el orden de empaquetado de los constructores (que siempre sigue la ordenación de fila principal).</span><span class="sxs-lookup"><span data-stu-id="0b883-223">Row-major and column-major packing order has no influence on the packing order of constructors (which always follows row-major ordering).</span></span>

<span data-ttu-id="0b883-224">El orden de los datos de una matriz se puede declarar en tiempo de compilación o el compilador ordenará los datos en tiempo de ejecución para el uso más eficaz.</span><span class="sxs-lookup"><span data-stu-id="0b883-224">The order of the data in a matrix can be declared at compile time or the compiler will order the data at runtime for the most efficient use.</span></span>

## <a name="examples"></a><span data-ttu-id="0b883-225">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="0b883-225">Examples</span></span>

<span data-ttu-id="0b883-226">HLSL usa dos tipos especiales, un tipo de vector y un tipo de matriz para facilitar la programación de gráficos 2D y 3D.</span><span class="sxs-lookup"><span data-stu-id="0b883-226">HLSL uses two special types, a vector type and a matrix type to make programming 2D and 3D graphics easier.</span></span> <span data-ttu-id="0b883-227">Cada uno de estos tipos contiene más de un componente; un vector contiene hasta cuatro componentes y una matriz contiene hasta 16 componentes.</span><span class="sxs-lookup"><span data-stu-id="0b883-227">Each of these types contain more than one component; a vector contains up to four components, and a matrix contains up to 16 components.</span></span> <span data-ttu-id="0b883-228">Cuando se usan vectores y matrices en ecuaciones HLSL estándar, las matemáticas realizadas están diseñadas para funcionar por componente.</span><span class="sxs-lookup"><span data-stu-id="0b883-228">When vectors and matrices are used in standard HLSL equations, the math performed is designed to work per-component.</span></span> <span data-ttu-id="0b883-229">Por ejemplo, HLSL implementa esta multiplicación:</span><span class="sxs-lookup"><span data-stu-id="0b883-229">For instance, HLSL implements this multiply:</span></span>


```
float4 v = a*b;
```



<span data-ttu-id="0b883-230">como una multiplicación de cuatro componentes.</span><span class="sxs-lookup"><span data-stu-id="0b883-230">as a four-component multiply.</span></span> <span data-ttu-id="0b883-231">El resultado es cuatro escalares:</span><span class="sxs-lookup"><span data-stu-id="0b883-231">The result is four scalars:</span></span>


```
float4 v = a*b;

v.x = a.x*b.x;
v.y = a.y*b.y;
v.z = a.z*b.z;
v.w = a.w*b.w;
```



<span data-ttu-id="0b883-232">Se trata de cuatro multiplicaciones donde cada resultado se almacena en un componente independiente de v.</span><span class="sxs-lookup"><span data-stu-id="0b883-232">This is four multiplications where each result is stored in a separate component of v.</span></span> <span data-ttu-id="0b883-233">Esto se denomina multiplicación de cuatro componentes.</span><span class="sxs-lookup"><span data-stu-id="0b883-233">This is called a four-component multiply.</span></span> <span data-ttu-id="0b883-234">HLSL usa matemáticas de componentes, lo que hace que la escritura de sombreadores sea muy eficaz.</span><span class="sxs-lookup"><span data-stu-id="0b883-234">HLSL uses component math which makes writing shaders very efficient.</span></span>

<span data-ttu-id="0b883-235">Esto es muy diferente de una multiplicación que normalmente se implementa como un producto de punto que genera un único escalar:</span><span class="sxs-lookup"><span data-stu-id="0b883-235">This is very different from a multiply which is typically implemented as a dot product which generates a single scalar:</span></span>


```
v = a.x*b.x + a.y*b.y + a.z*b.z + a.w*b.w;
```



<span data-ttu-id="0b883-236">Una matriz también usa operaciones por componente en HLSL:</span><span class="sxs-lookup"><span data-stu-id="0b883-236">A matrix also uses per-component operations in HLSL:</span></span>


```
float3x3 mat1,mat2;
...
float3x3 mat3 = mat1*mat2;
```



<span data-ttu-id="0b883-237">El resultado es una multiplicación por componente de las dos matrices (en lugar de una matriz estándar de 3x3 multiplicada).</span><span class="sxs-lookup"><span data-stu-id="0b883-237">The result is a per-component multiply of the two matrices (as opposed to a standard 3x3 matrix multiply).</span></span> <span data-ttu-id="0b883-238">Una multiplicación por matriz de componentes produce este primer término:</span><span class="sxs-lookup"><span data-stu-id="0b883-238">A per component matrix multiply yields this first term:</span></span>


```
mat3.m00 = mat1.m00 * mat2._m00;
```



<span data-ttu-id="0b883-239">Esto es diferente de una multiplicación de matriz 3x3 que produciría este primer término:</span><span class="sxs-lookup"><span data-stu-id="0b883-239">This is different from a 3x3 matrix multiply which would yield this first term:</span></span>


```
// First component of a four-component matrix multiply
mat.m00 = mat1._m00 * mat2._m00 + 
          mat1._m01 * mat2._m10 + 
          mat1._m02 * mat2._m20 + 
          mat1._m03 * mat2._m30;
```



<span data-ttu-id="0b883-240">Las versiones sobrecargadas de la función intrínseca de multiplicación controlan los casos en los que un operando es un vector y el otro operando es una matriz.</span><span class="sxs-lookup"><span data-stu-id="0b883-240">Overloaded versions of the multiply intrinsic function handle cases where one operand is a vector and the other operand is a matrix.</span></span> <span data-ttu-id="0b883-241">Por ejemplo: vector \* vectorial, matriz \* vectorial, \* vector de matriz y \* matriz de matrices.</span><span class="sxs-lookup"><span data-stu-id="0b883-241">Such as: vector \* vector, vector \* matrix, matrix \* vector, and matrix \* matrix.</span></span> <span data-ttu-id="0b883-242">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="0b883-242">For instance:</span></span>


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



<span data-ttu-id="0b883-243">produce el mismo resultado que:</span><span class="sxs-lookup"><span data-stu-id="0b883-243">produces the same result as:</span></span>


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



<span data-ttu-id="0b883-244">En este ejemplo se convierte el vector pos en un vector de columna mediante la conversión (float1x4).</span><span class="sxs-lookup"><span data-stu-id="0b883-244">This example casts the pos vector to a column vector using the (float1x4) cast.</span></span> <span data-ttu-id="0b883-245">Cambiar un vector mediante conversión o intercambiar el orden de los argumentos proporcionados para multiplicar es equivalente a cambiar la matriz.</span><span class="sxs-lookup"><span data-stu-id="0b883-245">Changing a vector by casting, or swapping the order of the arguments supplied to multiply is equivalent to transposing the matrix.</span></span>

<span data-ttu-id="0b883-246">La conversión automática hace que las funciones intrínsecas de multiplicación y punto devuelvan los mismos resultados que se usan aquí:</span><span class="sxs-lookup"><span data-stu-id="0b883-246">Automatic cast conversion causes the multiply and dot intrinsic functions to return the same results as used here:</span></span>


```
{
  float4 val;
  return mul(val,val);
}
```



<span data-ttu-id="0b883-247">Este resultado de la multiplicación es un vector 1x4 \* 4x1 = 1x1.</span><span class="sxs-lookup"><span data-stu-id="0b883-247">This result of the multiply is a 1x4 \* 4x1 = 1x1 vector.</span></span> <span data-ttu-id="0b883-248">Esto equivale a un producto de punto:</span><span class="sxs-lookup"><span data-stu-id="0b883-248">This is equivalent to a dot product:</span></span>


```
{
  float4 val;
  return dot(val,val);
}
```



<span data-ttu-id="0b883-249">que devuelve un único valor escalar.</span><span class="sxs-lookup"><span data-stu-id="0b883-249">which returns a single scalar value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b883-250">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0b883-250">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b883-251">Tipos de datos (HLSL de DirectX)</span><span class="sxs-lookup"><span data-stu-id="0b883-251">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 




