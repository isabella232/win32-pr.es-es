---
title: first_is (atributo)
description: El atributo \ First \_ es \ especifica el índice del primer elemento de la matriz que se va a transmitir.
ms.assetid: 1de7821c-19e7-4b2c-98fc-2fae3563831c
keywords:
- first_is el atributo MIDL
topic_type:
- apiref
api_name:
- first_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1d8d1be33299354e77ef92d885bb3b092cccfb6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904603"
---
# <a name="first_is-attribute"></a><span data-ttu-id="2f4e6-104">el \_ atributo First es</span><span class="sxs-lookup"><span data-stu-id="2f4e6-104">first\_is attribute</span></span>

<span data-ttu-id="2f4e6-105">El \[ **primero \_ es** el \] atributo que especifica el índice del primer elemento de la matriz que se va a transmitir.</span><span class="sxs-lookup"><span data-stu-id="2f4e6-105">The \[**first\_is**\] attribute specifies the index of the first array element to be transmitted.</span></span>

``` syntax
first_is(limited-expression-list)
```

## <a name="parameters"></a><span data-ttu-id="2f4e6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2f4e6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f4e6-107">*Limited-Expression-List*</span><span class="sxs-lookup"><span data-stu-id="2f4e6-107">*limited-expression-list*</span></span> 
</dt> <dd>

<span data-ttu-id="2f4e6-108">Especifica una o más expresiones del lenguaje C.</span><span class="sxs-lookup"><span data-stu-id="2f4e6-108">Specifies one or more C-language expressions.</span></span> <span data-ttu-id="2f4e6-109">Cada expresión se evalúa como un entero que representa el índice de la matriz del primer elemento de la matriz que se va a transmitir.</span><span class="sxs-lookup"><span data-stu-id="2f4e6-109">Each expression evaluates to an integer that represents the array index of the first array element to be transmitted.</span></span> <span data-ttu-id="2f4e6-110">El compilador MIDL admite expresiones condicionales, expresiones lógicas, expresiones relacionales y expresiones aritméticas.</span><span class="sxs-lookup"><span data-stu-id="2f4e6-110">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="2f4e6-111">MIDL no permite invocaciones de función en expresiones y no permite operadores de incremento y decremento.</span><span class="sxs-lookup"><span data-stu-id="2f4e6-111">MIDL does not allow function invocations in expressions and does not allow increment and decrement operators.</span></span> <span data-ttu-id="2f4e6-112">Separe varias expresiones con comas.</span><span class="sxs-lookup"><span data-stu-id="2f4e6-112">Separate multiple expressions with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2f4e6-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2f4e6-113">Remarks</span></span>

<span data-ttu-id="2f4e6-114">Si el **\[ primer \_ \]** atributo no está presente, o si el índice especificado es un número negativo, el elemento de matriz cero es el primer elemento transmitido.</span><span class="sxs-lookup"><span data-stu-id="2f4e6-114">If the **\[first\_is\]** attribute is not present, or if the specified index is a negative number, array element zero is the first element transmitted.</span></span>

<span data-ttu-id="2f4e6-115">El **\[ primero \_ es \]** el atributo que también puede ayudar a determinar los valores de los índices de matriz correspondientes al **\[** atributo [**Last \_ es**](last-is.md) **\]** o **\[** [**length \_ es**](length-is.md) **\]** cuando no se especifican estos atributos.</span><span class="sxs-lookup"><span data-stu-id="2f4e6-115">The **\[first\_is\]** attribute can also help determine the values of the array indexes corresponding to the **\[**[**last\_is**](last-is.md)**\]** or **\[**[**length\_is**](length-is.md)**\]** attribute when these attributes are not specified.</span></span> <span data-ttu-id="2f4e6-116">La relación entre estos índices de matriz es:</span><span class="sxs-lookup"><span data-stu-id="2f4e6-116">The relationship between these array indexes is:</span></span>

``` syntax
length = last - first + 1
```

<span data-ttu-id="2f4e6-117">La relación siguiente también debe contener:</span><span class="sxs-lookup"><span data-stu-id="2f4e6-117">The following relationship must also hold:</span></span>

``` syntax
0 <= first_is <= max_is
```

<span data-ttu-id="2f4e6-118">La siguiente relación debe contener cuando **\[** [**Max \_ es**](max-is.md) **\] <= 0:**</span><span class="sxs-lookup"><span data-stu-id="2f4e6-118">The following relationship must hold when **\[**[**max\_is**](max-is.md)**\] <= 0:**</span></span>

``` syntax
first_is == 0
```

<span data-ttu-id="2f4e6-119">El **\[ \_ primer \]** atributo no se puede usar al mismo tiempo que el atributo de **\[** [**cadena**](string.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="2f4e6-119">The **\[first\_is\]** attribute cannot be used at the same time as the **\[**[**string**](string.md)**\]** attribute.</span></span>

<span data-ttu-id="2f4e6-120">El uso de una expresión constante con el **\[ primer \_ \]** atributo es un uso inadecuado del atributo.</span><span class="sxs-lookup"><span data-stu-id="2f4e6-120">Using a constant expression with the **\[first\_is\]** attribute is an inappropriate use of the attribute.</span></span> <span data-ttu-id="2f4e6-121">Es legal, pero ineficaz, y dará como resultado un código de serialización más lento.</span><span class="sxs-lookup"><span data-stu-id="2f4e6-121">It is legal, but inefficient, and will result in slower marshaling code.</span></span>

## <a name="examples"></a><span data-ttu-id="2f4e6-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="2f4e6-122">Examples</span></span>

``` syntax
HRESULT Proc1(
    [in] short First,
    [first_is(First)] Arr[10]);
```

## <a name="see-also"></a><span data-ttu-id="2f4e6-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="2f4e6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f4e6-124">atributos de campo \_</span><span class="sxs-lookup"><span data-stu-id="2f4e6-124">field\_attributes</span></span>](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[<span data-ttu-id="2f4e6-125">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="2f4e6-125">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="2f4e6-126">**última \_ es**</span><span class="sxs-lookup"><span data-stu-id="2f4e6-126">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="2f4e6-127">**la longitud \_ es**</span><span class="sxs-lookup"><span data-stu-id="2f4e6-127">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="2f4e6-128">**Max \_ es**</span><span class="sxs-lookup"><span data-stu-id="2f4e6-128">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="2f4e6-129">**min \_ es**</span><span class="sxs-lookup"><span data-stu-id="2f4e6-129">**min\_is**</span></span>](min-is.md)
</dt> <dt>

[<span data-ttu-id="2f4e6-130">**el tamaño \_ es**</span><span class="sxs-lookup"><span data-stu-id="2f4e6-130">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="2f4e6-131">**string**</span><span class="sxs-lookup"><span data-stu-id="2f4e6-131">**string**</span></span>](string.md)
</dt> </dl>

 

 