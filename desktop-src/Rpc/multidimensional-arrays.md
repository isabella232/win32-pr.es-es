---
title: Matrices multidimensionales
description: Los atributos de matriz también se pueden usar con matrices multidimensionales.
ms.assetid: a01b904c-fbe8-4af4-8393-6864f7ef7364
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb7bcf94d97e1f35fdd6ab432ea5869e47f79ed
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995473"
---
# <a name="multidimensional-arrays"></a><span data-ttu-id="a8f9a-103">Matrices multidimensionales</span><span class="sxs-lookup"><span data-stu-id="a8f9a-103">Multidimensional Arrays</span></span>

<span data-ttu-id="a8f9a-104">Los atributos de matriz también se pueden usar con matrices multidimensionales.</span><span class="sxs-lookup"><span data-stu-id="a8f9a-104">Array attributes can also be used with multidimensional arrays.</span></span> <span data-ttu-id="a8f9a-105">Sin embargo, tenga cuidado para asegurarse de que todas las dimensiones de la matriz tienen el atributo correspondiente.</span><span class="sxs-lookup"><span data-stu-id="a8f9a-105">However, be careful to ensure that every dimension of the array has a corresponding attribute.</span></span> <span data-ttu-id="a8f9a-106">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="a8f9a-106">For example:</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(2.0)
]
interface multiarray
{
  void arr2d( [in] short        d1size,
              [in] short        d2len,
              [in, size_is( d1size, ), length_is ( , d2len) ] long array2d[*][30] ) ;
}
```

<span data-ttu-id="a8f9a-107">La matriz anterior es una matriz compatible (de tamaño d1size) de 30 matrices de elementos (con elementos d2len enviados para cada uno).</span><span class="sxs-lookup"><span data-stu-id="a8f9a-107">The preceding array is a conformant array (of size d1size ) of 30 element arrays (with d2len elements shipped for each).</span></span> <span data-ttu-id="a8f9a-108">La coma entre paréntesis del \[ [**tamaño \_ es**](/windows/desktop/Midl/size-is) \] Attribute especifica que el valor de d1size se aplica a la primera dimensión de la matriz.</span><span class="sxs-lookup"><span data-stu-id="a8f9a-108">The comma in the parentheses of the \[[**size\_is**](/windows/desktop/Midl/size-is)\] attribute specifies that value in d1size is applied to the first dimension of the array.</span></span> <span data-ttu-id="a8f9a-109">Del mismo modo, el comando de los paréntesis de la \[ [**longitud \_ es**](/windows/desktop/Midl/length-is) \] Attribute indica que el valor de d2len se aplica a la segunda dimensión de la matriz.</span><span class="sxs-lookup"><span data-stu-id="a8f9a-109">Likewise, the command in the parentheses of the \[[**length\_is**](/windows/desktop/Midl/length-is)\] attribute indicates that the value in d2len is applied to the second dimension of the array.</span></span>

<span data-ttu-id="a8f9a-110">El compilador de MIDL 2,0 proporciona dos métodos para calcular las referencias de los parámetros: modo mixto (/**os**) y completamente interpretado (/Activated **o/** **Oicf**).</span><span class="sxs-lookup"><span data-stu-id="a8f9a-110">The MIDL 2.0 compiler provides two methods for marshaling parameters: mixed-mode (/**Os**) and fully-interpreted (/**Oif** or /**Oicf**).</span></span> <span data-ttu-id="a8f9a-111">De forma predeterminada, el compilador MIDL compila las interfaces en modo mixto.</span><span class="sxs-lookup"><span data-stu-id="a8f9a-111">By default, the MIDL compiler compiles interfaces in mixed mode.</span></span> <span data-ttu-id="a8f9a-112">No es necesario especificar explícitamente el modificador [**/os**](/windows/desktop/Midl/-os) para obtener el cálculo de referencias en modo mixto.</span><span class="sxs-lookup"><span data-stu-id="a8f9a-112">You do not need to explicitly specify the [**/Os**](/windows/desktop/Midl/-os) switch to get mixed-mode marshaling.</span></span>

<span data-ttu-id="a8f9a-113">El método totalmente interpretado calcula las referencias de los datos completamente sin conexión.</span><span class="sxs-lookup"><span data-stu-id="a8f9a-113">The fully-interpreted method marshals data completely offline.</span></span> <span data-ttu-id="a8f9a-114">Esto reduce considerablemente el tamaño del código auxiliar, pero también reduce el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="a8f9a-114">This reduces the size of the stub code considerably, but it also results in decreased performance.</span></span> <span data-ttu-id="a8f9a-115">En el cálculo de referencias en modo mixto, el código auxiliar calcula las referencias de algunos parámetros en línea.</span><span class="sxs-lookup"><span data-stu-id="a8f9a-115">In mixed-mode marshaling, the stubs marshals some parameters online.</span></span> <span data-ttu-id="a8f9a-116">Aunque esto da como resultado un mayor tamaño de código auxiliar, también ofrece un mayor rendimiento.</span><span class="sxs-lookup"><span data-stu-id="a8f9a-116">While this results in a larger stub size, it also offers increased performance.</span></span>

> [!Caution]  
> <span data-ttu-id="a8f9a-117">Tenga cuidado al compilar archivos IDL en este modo.</span><span class="sxs-lookup"><span data-stu-id="a8f9a-117">Exercise caution when compiling IDL files in this mode.</span></span> <span data-ttu-id="a8f9a-118">El uso de matrices multidimensionales en modo mixto puede dar lugar a parámetros cuyas referencias no se han calculado correctamente.</span><span class="sxs-lookup"><span data-stu-id="a8f9a-118">Using multidimensional arrays in mixed mode can result in parameters that are not marshaled correctly.</span></span> <span data-ttu-id="a8f9a-119">Se recomienda el modificador de la línea de comandos [**/Oicf**](/windows/desktop/Midl/-oi) cuando la interfaz define parámetros que son matrices multidimensionales.</span><span class="sxs-lookup"><span data-stu-id="a8f9a-119">The [**/Oicf**](/windows/desktop/Midl/-oi) command line switch is recommended when your interface defines parameters that are multidimensional arrays.</span></span>

 

<span data-ttu-id="a8f9a-120">El \[ atributo [**String**](/windows/desktop/Midl/string) \] también se puede utilizar con matrices multidimensionales.</span><span class="sxs-lookup"><span data-stu-id="a8f9a-120">The \[[**string**](/windows/desktop/Midl/string)\] attribute can also be used with multidimensional arrays.</span></span> <span data-ttu-id="a8f9a-121">El atributo se aplica a la dimensión menos significativa, como una matriz de cadenas compatible.</span><span class="sxs-lookup"><span data-stu-id="a8f9a-121">The attribute applies to the least significant dimension, such as a conformant array of strings.</span></span> <span data-ttu-id="a8f9a-122">También puede usar atributos de puntero multidimensionales.</span><span class="sxs-lookup"><span data-stu-id="a8f9a-122">You can also use multidimensional pointer attributes.</span></span> <span data-ttu-id="a8f9a-123">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="a8f9a-123">For example:</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(2.0)
]
interface multiarray
{
  void arr2d([in] short  d1len,
             [in] short  d2len,
             [in] size_is(d1len, d2len) ] long  ** ptr2d) ;
}
```

<span data-ttu-id="a8f9a-124">En el ejemplo anterior, la variable ptr2d es un puntero a un bloque de punteros de tamaño d1len, cada uno de los cuales señala a los punteros d2len a **Long**.</span><span class="sxs-lookup"><span data-stu-id="a8f9a-124">In the preceding example, the variable ptr2d is a pointer to a d1len-sized block of pointers, each of which points to d2len pointers to **long**.</span></span>

<span data-ttu-id="a8f9a-125">Las matrices multidimensionales no son equivalentes a las matrices de punteros.</span><span class="sxs-lookup"><span data-stu-id="a8f9a-125">Multidimensional arrays are not equivalent to arrays of pointers.</span></span> <span data-ttu-id="a8f9a-126">Una matriz multidimensional es un bloque de datos único y grande en la memoria.</span><span class="sxs-lookup"><span data-stu-id="a8f9a-126">A multidimensional array is a single, large block of data in memory.</span></span> <span data-ttu-id="a8f9a-127">Una matriz de punteros solo contiene un bloque de punteros en la matriz.</span><span class="sxs-lookup"><span data-stu-id="a8f9a-127">An array of pointers only contains a block of pointers in the array.</span></span> <span data-ttu-id="a8f9a-128">Los datos a los que apuntan los punteros pueden encontrarse en cualquier parte de la memoria.</span><span class="sxs-lookup"><span data-stu-id="a8f9a-128">The data that the pointers point to can be anywhere in memory.</span></span> <span data-ttu-id="a8f9a-129">Además, la sintaxis de ANSI C solo permite que la dimensión de matriz más significativa (más a la izquierda) no se especifique en una matriz multidimensional.</span><span class="sxs-lookup"><span data-stu-id="a8f9a-129">Also, ANSI C syntax allows only the most significant (leftmost) array dimension to be unspecified in a multidimensional array.</span></span> <span data-ttu-id="a8f9a-130">Por lo tanto, la siguiente es una instrucción válida:</span><span class="sxs-lookup"><span data-stu-id="a8f9a-130">Therefore, the following is a valid statement:</span></span>

`long a1[] [20]`

<span data-ttu-id="a8f9a-131">Compárelo con la siguiente instrucción no válida:</span><span class="sxs-lookup"><span data-stu-id="a8f9a-131">Compare this to the following invalid statement:</span></span>

`long a1[20] []`

 

 