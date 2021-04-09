---
title: size_is (atributo)
description: Use el atributo \ size \_ es \ para especificar el tamaño de la memoria, en elementos, asignados para punteros de tamaño, punteros de tamaño a punteros de tamaño y matrices de un solo o multidimensionales.
ms.assetid: 1f3f3629-f668-460d-86fd-16ef22449973
keywords:
- size_is el atributo MIDL
topic_type:
- apiref
api_name:
- size_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f65a4c3ea93ea9ed55ce4f6f9ce846c81b60fa40
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103789861"
---
# <a name="size_is-attribute"></a><span data-ttu-id="9f9ef-104">el tamaño \_ es Attribute</span><span class="sxs-lookup"><span data-stu-id="9f9ef-104">size\_is attribute</span></span>

<span data-ttu-id="9f9ef-105">Use el \[ **atributo \_ size** \] para especificar el tamaño de la memoria, en elementos, asignados para punteros de tamaño, punteros de tamaño a punteros de tamaño y Matrices unidimensionales o únicas.</span><span class="sxs-lookup"><span data-stu-id="9f9ef-105">Use the \[**size\_is**\] attribute to specify the size of memory, in elements, allocated for sized pointers, sized pointers to sized pointers, and single- or multidimensional arrays.</span></span>

``` syntax
[ size_is(limited-expression-list) ]
```

## <a name="parameters"></a><span data-ttu-id="9f9ef-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9f9ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f9ef-107">*Limited-Expression-List*</span><span class="sxs-lookup"><span data-stu-id="9f9ef-107">*limited-expression-list*</span></span> 
</dt> <dd>

<span data-ttu-id="9f9ef-108">Especifica una o más expresiones del lenguaje C.</span><span class="sxs-lookup"><span data-stu-id="9f9ef-108">Specifies one or more C-language expressions.</span></span> <span data-ttu-id="9f9ef-109">Cada expresión se evalúa como un entero no negativo que representa la cantidad de memoria asignada a un puntero de tamaño o una matriz.</span><span class="sxs-lookup"><span data-stu-id="9f9ef-109">Each expression evaluates to a non-negative integer that represents the amount of memory allocated to a sized pointer or an array.</span></span> <span data-ttu-id="9f9ef-110">En el caso de una matriz, especifica una expresión única que representa el tamaño de asignación, en elementos, de la primera dimensión de esa matriz.</span><span class="sxs-lookup"><span data-stu-id="9f9ef-110">In the case of an array, specifies a single expression that represents the allocation size, in elements, of the first dimension of that array.</span></span> <span data-ttu-id="9f9ef-111">El compilador MIDL admite expresiones condicionales, expresiones lógicas, expresiones relacionales y expresiones aritméticas.</span><span class="sxs-lookup"><span data-stu-id="9f9ef-111">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="9f9ef-112">MIDL no permite invocaciones de función en expresiones y no permite operadores de incremento y decremento.</span><span class="sxs-lookup"><span data-stu-id="9f9ef-112">MIDL does not allow function invocations in expressions and does not allow increment and decrement operators.</span></span> <span data-ttu-id="9f9ef-113">Use comas como marcadores de posición para los parámetros implícitos o para separar varias expresiones.</span><span class="sxs-lookup"><span data-stu-id="9f9ef-113">Use commas as placeholders for implicit parameters, or to separate multiple expressions.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9f9ef-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9f9ef-114">Remarks</span></span>

<span data-ttu-id="9f9ef-115">Si está utilizando el atributo \[ **size \_** \] para asignar memoria para una matriz multidimensional y usa la notación de matriz \[ \] , tenga en cuenta que solo la primera dimensión de una matriz multidimensional se puede determinar dinámicamente en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="9f9ef-115">If you are using the \[**size\_is**\] attribute to allocate memory for a multidimensional array and you are using array \[ \] notation, keep in mind that only the first dimension of a multidimensional array can be dynamically determined at run time.</span></span> <span data-ttu-id="9f9ef-116">Las demás dimensiones deben especificarse estáticamente.</span><span class="sxs-lookup"><span data-stu-id="9f9ef-116">The other dimensions must be statically specified.</span></span> <span data-ttu-id="9f9ef-117">Para obtener más información sobre el uso del \[ atributo **size \_** \] con varios niveles de punteros para permitir que un servidor devuelva una matriz de datos de tamaño dinámico a un cliente, como se muestra en el Proc7 de ejemplo, vea [varios niveles de punteros](/windows/desktop/Rpc/multiple-levels-of-pointers).</span><span class="sxs-lookup"><span data-stu-id="9f9ef-117">For more information on using the \[**size\_is**\] attribute with multiple levels of pointers to enable a server to return a dynamically-sized array of data to a client, as shown in the example Proc7, see [Multiple Levels of Pointers](/windows/desktop/Rpc/multiple-levels-of-pointers).</span></span>

<span data-ttu-id="9f9ef-118">Puede usar cualquier \[ **tamaño \_ es** \] o [**Max \_ es**](max-is.md) (pero no ambos en la misma lista de atributos) para especificar el tamaño de una matriz cuyos límites superiores se determinan en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="9f9ef-118">You can use either \[**size\_is**\] or [**max\_is**](max-is.md) (but not both in the same attribute list) to specify the size of an array whose upper bounds are determined at run time.</span></span> <span data-ttu-id="9f9ef-119">Tenga en cuenta, sin embargo, que no se \[ **\_** \] puede usar el atributo size en las dimensiones de la matriz que son fijas.</span><span class="sxs-lookup"><span data-stu-id="9f9ef-119">Note, however, that the \[**size\_is**\] attribute cannot be used on array dimensions that are fixed.</span></span> <span data-ttu-id="9f9ef-120">El \[ atributo **Max \_ is** \] especifica el índice de matriz válido máximo.</span><span class="sxs-lookup"><span data-stu-id="9f9ef-120">The \[**max\_is**\] attribute specifies the maximum valid array index.</span></span> <span data-ttu-id="9f9ef-121">Como resultado, la especificación \[ del tamaño \_ es (n) \] equivale a especificar \[ Max \_ es (n-1) \] .</span><span class="sxs-lookup"><span data-stu-id="9f9ef-121">As a result, specifying \[size\_is(n)\] is equivalent to specifying \[max\_is(n-1)\].</span></span>

<span data-ttu-id="9f9ef-122">\[ [](in.md) \] \[ No es necesario que un parámetro in o in, [**out**](out-idl.md) \] -array compatible con el atributo de \[ [**cadena**](string.md) \] tenga el \[ atributo **size \_** \] o \[ [**Max \_ is**](max-is.md) \] .</span><span class="sxs-lookup"><span data-stu-id="9f9ef-122">An \[ [**in**](in.md)\] or \[in, [**out**](out-idl.md)\] conformant-array parameter with the \[ [**string**](string.md)\] attribute need not have the \[**size\_is**\] or \[[**max\_is**](max-is.md)\] attribute.</span></span> <span data-ttu-id="9f9ef-123">En este caso, el tamaño de la asignación se determina a partir del terminador nulo de la cadena de entrada.</span><span class="sxs-lookup"><span data-stu-id="9f9ef-123">In this case, the size of the allocation is determined from the NULL terminator of the input string.</span></span> <span data-ttu-id="9f9ef-124">Todas las demás matrices compatibles con el atributo de \[ cadena \] deben tener el atributo \[ **size \_** \] o \[ **Max \_ is** \] .</span><span class="sxs-lookup"><span data-stu-id="9f9ef-124">All other conformant arrays with the \[string\] attribute must have a \[**size\_is**\] or \[**max\_is**\] attribute.</span></span>

<span data-ttu-id="9f9ef-125">Aunque es legal usar el \[ **\_ atributo size** \] con una constante, hacerlo es ineficaz e innecesario.</span><span class="sxs-lookup"><span data-stu-id="9f9ef-125">While it is legal to use the \[**size\_is**\] attribute with a constant, doing so is inefficient and unnecessary.</span></span> <span data-ttu-id="9f9ef-126">Por ejemplo, use una matriz de tamaño fijo:</span><span class="sxs-lookup"><span data-stu-id="9f9ef-126">For example, use a fixed size array:</span></span>

``` syntax
HRESULT Proc3([in] short Arr[MAX_SIZE]);
```

<span data-ttu-id="9f9ef-127">en lugar de:</span><span class="sxs-lookup"><span data-stu-id="9f9ef-127">instead of:</span></span>

``` syntax
// legal but marshaling code is much slower
HRESULT Proc3([in size_is(MAX_SIZE)] short Arr[] );
```

<span data-ttu-id="9f9ef-128">Puede usar el \[ **tamaño \_** \] y la \[ [**longitud \_ son**](length-is.md) \] atributos juntos.</span><span class="sxs-lookup"><span data-stu-id="9f9ef-128">You can use the \[**size\_is**\] and \[[**length\_is**](length-is.md)\] attributes together.</span></span> <span data-ttu-id="9f9ef-129">Al hacerlo, el atributo \[ **size \_** \] controla la cantidad de memoria asignada a los datos.</span><span class="sxs-lookup"><span data-stu-id="9f9ef-129">When you do, the \[**size\_is**\] attribute controls the amount of memory allocated for the data.</span></span> <span data-ttu-id="9f9ef-130">El \[ **atributo \_ length** \] especifica el número de elementos que se transmiten.</span><span class="sxs-lookup"><span data-stu-id="9f9ef-130">The \[**length\_is**\] attribute specifies how many elements are transmitted.</span></span> <span data-ttu-id="9f9ef-131">La cantidad de memoria especificada por el \[ **tamaño \_ es** \] y la \[ **longitud \_** de \] los atributos no debe ser la misma.</span><span class="sxs-lookup"><span data-stu-id="9f9ef-131">The amount of memory specified by the \[**size\_is**\] and \[**length\_is**\] attributes need not be the same.</span></span> <span data-ttu-id="9f9ef-132">Por ejemplo, el cliente puede pasar un \[ parámetro in, out \] a un servidor y especificar una asignación de memoria grande con \[ **el tamaño \_ es** \] , aunque especifique un número pequeño de elementos de datos que se van a pasar con la \[ **longitud \_** \] .</span><span class="sxs-lookup"><span data-stu-id="9f9ef-132">For instance, your client may pass an \[in,out\] parameter to a server and specify a large memory allocation with \[**size\_is**\], even though it specifies a small number of data elements to be passed with \[**length\_is**\].</span></span> <span data-ttu-id="9f9ef-133">Esto permite que el servidor rellene la matriz con más datos de los recibidos, que puede devolver al cliente.</span><span class="sxs-lookup"><span data-stu-id="9f9ef-133">This enables the server to fill the array with more data than it received, which it can then send back to the client.</span></span>

<span data-ttu-id="9f9ef-134">En general, no es útil especificar \[ **el tamaño \_ es** \] y la \[ [**longitud \_ está**](length-is.md) \] en \[ \] los parámetros in o \[ out \] .</span><span class="sxs-lookup"><span data-stu-id="9f9ef-134">In general, it isn't useful to specify both \[**size\_is**\] and \[[**length\_is**](length-is.md)\] on \[in\] or \[out\] parameters.</span></span> <span data-ttu-id="9f9ef-135">En ambos casos, \[ **el tamaño \_ es** \] controlar la asignación de memoria.</span><span class="sxs-lookup"><span data-stu-id="9f9ef-135">In both cases, \[**size\_is**\] controls memory allocation.</span></span> <span data-ttu-id="9f9ef-136">La aplicación podría usar \[ **el \_ tamaño** \] para asignar más elementos de matriz de los transmitidos (según lo especificado por la \[ **longitud \_ es** \] ).</span><span class="sxs-lookup"><span data-stu-id="9f9ef-136">Your application could use \[**size\_is**\] to allocate more array elements than it transmits (as specified by \[**length\_is**\]).</span></span> <span data-ttu-id="9f9ef-137">Sin embargo, esto sería ineficaz.</span><span class="sxs-lookup"><span data-stu-id="9f9ef-137">However, this would be inefficient.</span></span> <span data-ttu-id="9f9ef-138">También sería ineficaz especificar valores idénticos para \[ **el tamaño \_** \] y la \[ **longitud \_ es** \] .</span><span class="sxs-lookup"><span data-stu-id="9f9ef-138">It would also be inefficient to specify identical values for \[**size\_is**\] and \[**length\_is**\].</span></span> <span data-ttu-id="9f9ef-139">Crearía una sobrecarga adicional durante la serialización de parámetros.</span><span class="sxs-lookup"><span data-stu-id="9f9ef-139">It would create extra overhead during parameter marshaling.</span></span> <span data-ttu-id="9f9ef-140">Si los valores de \[ **size \_ es** \] y \[ **length \_ es** \] siempre el mismo, omita el atributo \[ **length \_** \] .</span><span class="sxs-lookup"><span data-stu-id="9f9ef-140">If the values of \[**size\_is**\] and \[**length\_is**\] are always the same, omit the \[**length\_is**\] attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="9f9ef-141">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9f9ef-141">Examples</span></span>

``` syntax
HRESULT Proc1(
    [in] short m;
    [in, size_is(m)] short a[]);  // If m = 10, a[10]
HRESULT Proc2(
    [in] short m;
    [in, size_is(m)] short b[][20]);  // If m = 10, b[10][20]
HRESULT Proc3(
    [in] short m;
    [size_is(m)] short * pshort); /* Specifies a pointer
                                  to an m-sized block of shorts */
HRESULT Proc4(
    [in] short m;
    [size_is( , m)] short ** ppshort); /* Specifies a pointer 
                                       to a pointer to an m-sized 
                                       block of shorts */
HRESULT Proc5(
    [in] short m;
    [size_is(m ,)] short ** ppshort); /* Specifies an
                                      m-sized block of pointers 
                                      to shorts */
HRESULT Proc6(
    [in] short m;
    [in] short n;
    [size_is(m,n)] short ** ppshort); /* Specifies a pointer to an 
                                      m-sized block of pointers, each 
                                      of which points to an n-sized 
                                      block of shorts. m associates with
                                      the pointer closeest to the identifer
                                      it decorates. n associates with rest.*/
 HRESULT Proc7(
     [out] long  * pSize,
     [out, size_is( , *pSize)] my_type ** ppMyType); /* Specifies a pointer 
                                              to a sized pointer, 
                                              which points to a block 
                                              of my_types, whose size is
                                              unknown when the stub 
                                              calls the server. */
```

## <a name="see-also"></a><span data-ttu-id="9f9ef-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="9f9ef-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f9ef-143">**matrices**</span><span class="sxs-lookup"><span data-stu-id="9f9ef-143">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="9f9ef-144">Atributos de campo</span><span class="sxs-lookup"><span data-stu-id="9f9ef-144">Field Attributes</span></span>](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[<span data-ttu-id="9f9ef-145">**el primero \_ es**</span><span class="sxs-lookup"><span data-stu-id="9f9ef-145">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="9f9ef-146">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="9f9ef-146">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="9f9ef-147">**de**</span><span class="sxs-lookup"><span data-stu-id="9f9ef-147">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="9f9ef-148">**última \_ es**</span><span class="sxs-lookup"><span data-stu-id="9f9ef-148">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="9f9ef-149">**la longitud \_ es**</span><span class="sxs-lookup"><span data-stu-id="9f9ef-149">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="9f9ef-150">**Max \_ es**</span><span class="sxs-lookup"><span data-stu-id="9f9ef-150">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="9f9ef-151">**min \_ es**</span><span class="sxs-lookup"><span data-stu-id="9f9ef-151">**min\_is**</span></span>](min-is.md)
</dt> <dt>

[<span data-ttu-id="9f9ef-152">**enuncia**</span><span class="sxs-lookup"><span data-stu-id="9f9ef-152">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="9f9ef-153">**string**</span><span class="sxs-lookup"><span data-stu-id="9f9ef-153">**string**</span></span>](string.md)
</dt> </dl>

 

 