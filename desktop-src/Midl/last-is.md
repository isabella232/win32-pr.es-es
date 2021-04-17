---
title: last_is (atributo)
description: El atributo de campo \ Last \_ es \ especifica el índice del último elemento de la matriz que se va a transmitir. Cuando el índice especificado es cero o negativo, no se transmite ningún elemento de la matriz.
ms.assetid: 42a5cb0d-0887-4aa7-b34f-2fbad0f4c8ab
keywords:
- last_is el atributo MIDL
topic_type:
- apiref
api_name:
- last_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 453a51109452f3cdacb1a48e67b76ccbc9f2e257
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104533160"
---
# <a name="last_is-attribute"></a><span data-ttu-id="4a3ea-105">el \_ atributo Last es</span><span class="sxs-lookup"><span data-stu-id="4a3ea-105">last\_is attribute</span></span>

<span data-ttu-id="4a3ea-106">El atributo de campo **\[ Last \_ \]** especifica el índice del último elemento de la matriz que se va a transmitir.</span><span class="sxs-lookup"><span data-stu-id="4a3ea-106">The field attribute **\[last\_is\]** specifies the index of the last array element to be transmitted.</span></span> <span data-ttu-id="4a3ea-107">Cuando el índice especificado es cero o negativo, no se transmite ningún elemento de la matriz.</span><span class="sxs-lookup"><span data-stu-id="4a3ea-107">When the specified index is zero or negative, no array elements are transmitted.</span></span>

``` syntax
[last_is( limited-expression-list )]
```

## <a name="parameters"></a><span data-ttu-id="4a3ea-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4a3ea-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a3ea-109">*Limited-Expression-List*</span><span class="sxs-lookup"><span data-stu-id="4a3ea-109">*limited-expression-list*</span></span> 
</dt> <dd>

<span data-ttu-id="4a3ea-110">Especifica una o más expresiones del lenguaje C.</span><span class="sxs-lookup"><span data-stu-id="4a3ea-110">Specifies one or more C-language expressions.</span></span> <span data-ttu-id="4a3ea-111">Cada expresión se evalúa como un entero que representa el índice de la matriz del último elemento de la matriz que se va a transmitir.</span><span class="sxs-lookup"><span data-stu-id="4a3ea-111">Each expression evaluates to an integer that represents the array index of the last array element to be transmitted.</span></span> <span data-ttu-id="4a3ea-112">El compilador MIDL admite expresiones condicionales, expresiones lógicas, expresiones relacionales y expresiones aritméticas.</span><span class="sxs-lookup"><span data-stu-id="4a3ea-112">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="4a3ea-113">MIDL no permite invocaciones de función en expresiones y no permite operadores de incremento y decremento.</span><span class="sxs-lookup"><span data-stu-id="4a3ea-113">MIDL does not allow function invocations in expressions and does not allow increment and decrement operators.</span></span> <span data-ttu-id="4a3ea-114">Separe varias expresiones con comas.</span><span class="sxs-lookup"><span data-stu-id="4a3ea-114">Separate multiple expressions with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4a3ea-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4a3ea-115">Remarks</span></span>

<span data-ttu-id="4a3ea-116">El atributo **\[ Last \_ es \]** determina el valor del índice de matriz correspondiente a la **\[** [**\_**](length-is.md) **\]** **\[ \_ \]** longitud es Attribute cuando no se especifica length.</span><span class="sxs-lookup"><span data-stu-id="4a3ea-116">The **\[last\_is\]** attribute determines the value of the array index corresponding to the **\[**[**length\_is**](length-is.md)**\]** attribute when **\[length\_is\]** is not specified.</span></span> <span data-ttu-id="4a3ea-117">La relación entre estos índices de matriz es la siguiente: length = Last-First + 1.</span><span class="sxs-lookup"><span data-stu-id="4a3ea-117">The relationship between these array indexes is as follows: length = last - first + 1.</span></span>

<span data-ttu-id="4a3ea-118">Si el valor del índice de matriz especificado por **\[** [**First \_ es**](first-is.md) **\]** mayor que el valor especificado por **\[ Last \_ es \]**, se transmiten cero elementos.</span><span class="sxs-lookup"><span data-stu-id="4a3ea-118">If the value of the array index specified by **\[**[**first\_is**](first-is.md)**\]** is larger than the value specified by **\[last\_is\]**, zero elements are transmitted.</span></span>

<span data-ttu-id="4a3ea-119">El atributo **\[ Last \_ \] es** no se puede usar como atributo de campo al mismo tiempo que el atributo **\[** [**length \_**](length-is.md) **\]** o el **\[** atributo [**String**](string.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="4a3ea-119">The **\[last\_is\]** attribute cannot be used as a field attribute at the same time as the **\[**[**length\_is**](length-is.md)**\]** attribute or the **\[**[**string**](string.md)**\]** attribute.</span></span>

<span data-ttu-id="4a3ea-120">El uso de una expresión constante con el atributo **\[ Last \_ es \]** un uso inadecuado del atributo.</span><span class="sxs-lookup"><span data-stu-id="4a3ea-120">Using a constant expression with the **\[last\_is\]** attribute is an inappropriate use of the attribute.</span></span> <span data-ttu-id="4a3ea-121">Es legal, pero ineficaz, y dará como resultado un código de serialización más lento.</span><span class="sxs-lookup"><span data-stu-id="4a3ea-121">It is legal, but inefficient, and will result in slower marshaling code.</span></span>

<span data-ttu-id="4a3ea-122">Cuando el valor especificado por **\[** [**Max \_ es**](max-is.md) **\]** igual o mayor que cero, la relación siguiente debe ser true: 0 <= Last \_ es <= Max \_ es.</span><span class="sxs-lookup"><span data-stu-id="4a3ea-122">When the value specified by **\[**[**max\_is**](max-is.md)**\]** is equal to or greater than zero, the following relationship must be true: 0 <= last\_is <= max\_is.</span></span>

## <a name="examples"></a><span data-ttu-id="4a3ea-123">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4a3ea-123">Examples</span></span>

``` syntax
proc1(
    [in] short Last,
    [in, last_is(Last)] short asNumbers[MAXSIZE]);
```

## <a name="see-also"></a><span data-ttu-id="4a3ea-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="4a3ea-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a3ea-125">Atributos de campo</span><span class="sxs-lookup"><span data-stu-id="4a3ea-125">Field Attributes</span></span>](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[<span data-ttu-id="4a3ea-126">**el primero \_ es**</span><span class="sxs-lookup"><span data-stu-id="4a3ea-126">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="4a3ea-127">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="4a3ea-127">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="4a3ea-128">**la longitud \_ es**</span><span class="sxs-lookup"><span data-stu-id="4a3ea-128">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="4a3ea-129">**Max \_ es**</span><span class="sxs-lookup"><span data-stu-id="4a3ea-129">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="4a3ea-130">**el tamaño \_ es**</span><span class="sxs-lookup"><span data-stu-id="4a3ea-130">**size\_is**</span></span>](size-is.md)
</dt> </dl>

 

 