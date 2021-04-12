---
title: length_is (atributo)
description: El atributo \ length \_ es \ especifica el número de elementos de matriz que se van a transmitir. Debe especificar un valor no negativo.
ms.assetid: 060dbd4a-3078-4050-abfe-c1b633c06861
keywords:
- length_is el atributo MIDL
topic_type:
- apiref
api_name:
- length_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fac217bae01c6896c7dadd36bb18f15e425a0427
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487683"
---
# <a name="length_is-attribute"></a><span data-ttu-id="407f6-105">la longitud \_ es un atributo</span><span class="sxs-lookup"><span data-stu-id="407f6-105">length\_is attribute</span></span>

<span data-ttu-id="407f6-106">El atributo **\[ length \_ \]** especifica el número de elementos de matriz que se van a transmitir.</span><span class="sxs-lookup"><span data-stu-id="407f6-106">The **\[length\_is\]** attribute specifies the number of array elements to be transmitted.</span></span> <span data-ttu-id="407f6-107">Debe especificar un valor no negativo.</span><span class="sxs-lookup"><span data-stu-id="407f6-107">You must specify a non-negative value.</span></span>

``` syntax
[length_is( limited-expression-list )]
```

## <a name="parameters"></a><span data-ttu-id="407f6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="407f6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="407f6-109">*Limited-Expression-List*</span><span class="sxs-lookup"><span data-stu-id="407f6-109">*limited-expression-list*</span></span> 
</dt> <dd>

<span data-ttu-id="407f6-110">Especifica una o más expresiones del lenguaje C.</span><span class="sxs-lookup"><span data-stu-id="407f6-110">Specifies one or more C-language expressions.</span></span> <span data-ttu-id="407f6-111">Cada expresión se evalúa como un entero que representa el número de elementos de matriz que se van a transmitir.</span><span class="sxs-lookup"><span data-stu-id="407f6-111">Each expression evaluates to an integer that represents the number of array elements to be transmitted.</span></span> <span data-ttu-id="407f6-112">El compilador MIDL admite expresiones condicionales, expresiones lógicas, expresiones relacionales y expresiones aritméticas.</span><span class="sxs-lookup"><span data-stu-id="407f6-112">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="407f6-113">MIDL no permite invocaciones de función en expresiones y no permite operadores de incremento y decremento.</span><span class="sxs-lookup"><span data-stu-id="407f6-113">MIDL does not allow function invocations in expressions and does not allow increment and decrement operators.</span></span> <span data-ttu-id="407f6-114">Separe varias expresiones con comas.</span><span class="sxs-lookup"><span data-stu-id="407f6-114">Separate multiple expressions with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="407f6-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="407f6-115">Remarks</span></span>

<span data-ttu-id="407f6-116">El atributo **\[ length \_ \]** determina el valor de los índices de matriz correspondientes al **\[** atributo [**\_**](last-is.md) **\]** **\[ \_ \]** Last es cuando no se especifica Last.</span><span class="sxs-lookup"><span data-stu-id="407f6-116">The **\[length\_is\]** attribute determines the value of the array indexes corresponding to the **\[**[**last\_is**](last-is.md)**\]** attribute when **\[last\_is\]** is not specified.</span></span> <span data-ttu-id="407f6-117">La relación entre estos índices de matriz es la siguiente: length = Last-First + 1.</span><span class="sxs-lookup"><span data-stu-id="407f6-117">The relationship between these array indexes is as follows: length = last - first + 1.</span></span>

<span data-ttu-id="407f6-118">El atributo **\[ length \_ \]** no se puede usar al mismo tiempo que el atributo **\[** [**Last \_**](last-is.md) **\]** o el atributo **\[** [**String**](string.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="407f6-118">The **\[length\_is\]** attribute cannot be used at the same time as the **\[**[**last\_is**](last-is.md)**\]** attribute or the **\[**[**string**](string.md)**\]** attribute.</span></span>

<span data-ttu-id="407f6-119">Para definir una cadena contada con una **\[ longitud \_ \]** o el **\[** atributo [**Last \_ es**](last-is.md) **\]** , utilice una matriz de caracteres o un puntero sin el atributo de **\[** [**cadena**](string.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="407f6-119">To define a counted string with a **\[length\_is\]** or **\[**[**last\_is**](last-is.md)**\]** attribute, use a character array or pointer without the **\[**[**string**](string.md)**\]** attribute.</span></span>

<span data-ttu-id="407f6-120">El uso de una expresión constante con la **\[ longitud \_ es \]** un atributo que no es apropiado para el atributo.</span><span class="sxs-lookup"><span data-stu-id="407f6-120">Using a constant expression with the **\[length\_is\]** attribute is an inappropriate use of the attribute.</span></span> <span data-ttu-id="407f6-121">Es legal, pero ineficaz, y dará como resultado un código de serialización más lento.</span><span class="sxs-lookup"><span data-stu-id="407f6-121">It is legal, but inefficient, and will result in slower marshaling code.</span></span>

<span data-ttu-id="407f6-122">Puede usar el **\[** [**tamaño \_**](size-is.md) **\]** y la **\[ longitud \_ son \]** atributos juntos.</span><span class="sxs-lookup"><span data-stu-id="407f6-122">You can use the **\[**[**size\_is**](size-is.md)**\]** and **\[length\_is\]** attributes together.</span></span> <span data-ttu-id="407f6-123">Al hacerlo, el atributo **\[ size \_ \]** controla la cantidad de memoria asignada a los datos.</span><span class="sxs-lookup"><span data-stu-id="407f6-123">When you do, the **\[size\_is\]** attribute controls the amount of memory allocated for the data.</span></span> <span data-ttu-id="407f6-124">El atributo **\[ length \_ \]** especifica el número de elementos que se transmiten.</span><span class="sxs-lookup"><span data-stu-id="407f6-124">The **\[length\_is\]** attribute specifies how many elements are transmitted.</span></span> <span data-ttu-id="407f6-125">La cantidad de memoria especificada por el **\[ tamaño \_ es \]** y la **\[ longitud \_ \]** de los atributos no debe ser la misma.</span><span class="sxs-lookup"><span data-stu-id="407f6-125">The amount of memory specified by the **\[size\_is\]** and **\[length\_is\]** attributes need not be the same.</span></span> <span data-ttu-id="407f6-126">Por ejemplo, el cliente puede pasar un parámetro in **, \] out** a un servidor y especificar una asignación **\[ de** memoria grande con **\[ el tamaño \_ es \]**, aunque especifique un **\[ \_ \]** número pequeño de elementos de datos que se van a pasar con la longitud.</span><span class="sxs-lookup"><span data-stu-id="407f6-126">For instance, your client may pass an **\[in**, **out\]** parameter to a server and specify a large memory allocation with **\[size\_is\]**, even though it specifies a small number of data elements to be passed with **\[length\_is\]**.</span></span> <span data-ttu-id="407f6-127">Esto permite que el servidor rellene la matriz con más datos de los recibidos, que puede devolver al cliente.</span><span class="sxs-lookup"><span data-stu-id="407f6-127">This enables the server to fill the array with more data than it received, which it can then send back to the client.</span></span>

<span data-ttu-id="407f6-128">En general, no es útil especificar **\[** [**el tamaño \_ es**](size-is.md) **\]** y la **\[ longitud \_ está \]** en **\[** [](in.md) **\]** los parámetros in o **\[** [**out**](out-idl.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="407f6-128">In general, it isn't useful to specify both **\[**[**size\_is**](size-is.md)**\]** and **\[length\_is\]** on **\[**[**in**](in.md)**\]** or **\[**[**out**](out-idl.md)**\]** parameters.</span></span> <span data-ttu-id="407f6-129">En ambos casos, **\[ el \_ tamaño \] es** controlar la asignación de memoria.</span><span class="sxs-lookup"><span data-stu-id="407f6-129">In both cases, **\[size\_is\]** controls memory allocation.</span></span> <span data-ttu-id="407f6-130">La aplicación podría usar **\[ el \_ tamaño \]** para asignar más elementos de matriz de los transmitidos (según lo especificado por la **\[ longitud \_ es \]**).</span><span class="sxs-lookup"><span data-stu-id="407f6-130">Your application could use **\[size\_is\]** to allocate more array elements than it transmits (as specified by **\[length\_is\]**).</span></span> <span data-ttu-id="407f6-131">Sin embargo, esto sería ineficaz.</span><span class="sxs-lookup"><span data-stu-id="407f6-131">However, this would be inefficient.</span></span> <span data-ttu-id="407f6-132">También sería ineficaz especificar valores idénticos para **\[ el tamaño \_ \]** y la **\[ longitud \_ es \]**.</span><span class="sxs-lookup"><span data-stu-id="407f6-132">It would also be inefficient to specify identical values for **\[size\_is\]** and **\[length\_is\]**.</span></span> <span data-ttu-id="407f6-133">Porque crearía una sobrecarga adicional durante la serialización de parámetros.</span><span class="sxs-lookup"><span data-stu-id="407f6-133">Because it would create extra overhead during parameter marshaling.</span></span> <span data-ttu-id="407f6-134">Cuando los valores de **\[ size \_ es \]** y **\[ length \_ es \]** siempre el mismo, se omite el atributo **\[ length \_ \]** .</span><span class="sxs-lookup"><span data-stu-id="407f6-134">When the values of **\[size\_is\]** and **\[length\_is\]** are always the same, omit the **\[length\_is\]** attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="407f6-135">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="407f6-135">Examples</span></span>

``` syntax
/* counted string holding at most "size" characters */ 
typedef struct 
{ 
    unsigned short size; 
    unsigned short length; 
    [size_is(size), length_is(length)] char string[*]; 
 } COUNTED_STRING_TYPE; 
 
/* counted string holding at most 80 characters */ 
typedef struct 
{ 
    unsigned short length; 
    [length_is(length)] char string[80]; 
} STATIC_COUNTED_STRING_TYPE; 
 
HRESULT Proc1(
    [in] short iLength; 
    [in, length_is(iLength)] short asNumbers[10]);
```

## <a name="see-also"></a><span data-ttu-id="407f6-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="407f6-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="407f6-137">Atributos de campo</span><span class="sxs-lookup"><span data-stu-id="407f6-137">Field Attributes</span></span>](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[<span data-ttu-id="407f6-138">**el primero \_ es**</span><span class="sxs-lookup"><span data-stu-id="407f6-138">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="407f6-139">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="407f6-139">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="407f6-140">**última \_ es**</span><span class="sxs-lookup"><span data-stu-id="407f6-140">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="407f6-141">**Max \_ es**</span><span class="sxs-lookup"><span data-stu-id="407f6-141">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="407f6-142">**min \_ es**</span><span class="sxs-lookup"><span data-stu-id="407f6-142">**min\_is**</span></span>](min-is.md)
</dt> <dt>

[<span data-ttu-id="407f6-143">**el tamaño \_ es**</span><span class="sxs-lookup"><span data-stu-id="407f6-143">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="407f6-144">**string**</span><span class="sxs-lookup"><span data-stu-id="407f6-144">**string**</span></span>](string.md)
</dt> </dl>

 

 