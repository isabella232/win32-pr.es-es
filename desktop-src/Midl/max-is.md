---
title: max_is (atributo)
description: El atributo \ Max \_ es \ designa el valor máximo de un índice de matriz válido.
ms.assetid: 8d09f610-cae6-45f6-815c-5ba916d8a5e7
keywords:
- max_is el atributo MIDL
topic_type:
- apiref
api_name:
- max_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27f2e2040acbc0e8f65c02f4f4ec7c3ad329959b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358866"
---
# <a name="max_is-attribute"></a><span data-ttu-id="981f9-104">\_atributo Max is</span><span class="sxs-lookup"><span data-stu-id="981f9-104">max\_is attribute</span></span>

<span data-ttu-id="981f9-105">El atributo **\[ Max \_ is \]** designa el valor máximo de un índice de matriz válido.</span><span class="sxs-lookup"><span data-stu-id="981f9-105">The **\[max\_is\]** attribute designates the maximum value for a valid array index.</span></span>

``` syntax
[max_is(limited-expression-list )]
```

## <a name="parameters"></a><span data-ttu-id="981f9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="981f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="981f9-107">*Limited-Expression-List*</span><span class="sxs-lookup"><span data-stu-id="981f9-107">*limited-expression-list*</span></span> 
</dt> <dd>

<span data-ttu-id="981f9-108">Especifica una o más expresiones del lenguaje C.</span><span class="sxs-lookup"><span data-stu-id="981f9-108">Specifies one or more C-language expressions.</span></span> <span data-ttu-id="981f9-109">Cada expresión se evalúa como un entero que representa el índice de matriz válido más alto.</span><span class="sxs-lookup"><span data-stu-id="981f9-109">Each expression evaluates to an integer that represents the highest valid array index.</span></span> <span data-ttu-id="981f9-110">El compilador MIDL admite expresiones condicionales, expresiones lógicas, expresiones relacionales y expresiones aritméticas.</span><span class="sxs-lookup"><span data-stu-id="981f9-110">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="981f9-111">MIDL no permite invocaciones de función en expresiones y no permite operadores de incremento y decremento.</span><span class="sxs-lookup"><span data-stu-id="981f9-111">MIDL does not allow function invocations in expressions and does not allow increment and decrement operators.</span></span> <span data-ttu-id="981f9-112">Separe varias expresiones con comas.</span><span class="sxs-lookup"><span data-stu-id="981f9-112">Separate multiple expressions with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="981f9-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="981f9-113">Remarks</span></span>

<span data-ttu-id="981f9-114">El atributo **\[ Max \_ is no se \]** corresponde necesariamente con el número de elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="981f9-114">The **\[max\_is\]** attribute does not necessarily correspond to the number of elements in the array.</span></span> <span data-ttu-id="981f9-115">En el caso de una matriz de tamaño *n* en C, donde el primer elemento de la matriz es el número de elemento cero, el valor máximo de un índice de matriz válido es *n*– 1.</span><span class="sxs-lookup"><span data-stu-id="981f9-115">For an array of size *n* in C, where the first array element is element number zero, the maximum value for a valid array index is *n*–1.</span></span>

<span data-ttu-id="981f9-116">El atributo **\[ Max \_ is \]** no se puede usar como atributo de campo al mismo tiempo que el **\[** [**atributo \_ size**](size-is.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="981f9-116">The **\[max\_is\]** attribute cannot be used as a field attribute at the same time as the **\[**[**size\_is**](size-is.md)**\]** attribute.</span></span>

<span data-ttu-id="981f9-117">Aunque es legal usar el atributo **\[ Max \_ is \]** con una expresión constante, hacerlo es ineficaz e innecesario.</span><span class="sxs-lookup"><span data-stu-id="981f9-117">While it is legal to use the **\[max\_is\]** attribute with a constant expression, doing so is inefficient and unnecessary.</span></span> <span data-ttu-id="981f9-118">Por ejemplo, use una matriz de tamaño fijo:</span><span class="sxs-lookup"><span data-stu-id="981f9-118">For example, use a fixed size array:</span></span>

``` syntax
/* transmits values of a[0]... a[MAX_SIZE-1] */ 
HRESULT Proc3([in] short Arr[MAX_SIZE]); 
```

<span data-ttu-id="981f9-119">en lugar de:</span><span class="sxs-lookup"><span data-stu-id="981f9-119">instead of:</span></span>

``` syntax
/* legal but marshaling code is much slower */ 
HRESULT Proc3([in max_is(MAX_SIZE-1)] short Arr[] );
```

## <a name="examples"></a><span data-ttu-id="981f9-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="981f9-120">Examples</span></span>

``` syntax
/* if m = 10, there are 11 transmitted elements (a[0]...a[10])*/ 
HRESULT Proc1( 
    [in] short m, 
    [in, max_is(m)] short a[]);  
 
/* if m = 10, the valid range for b is b[0...10][20] */ 
HRESULT Proc2( 
    [in] short m, 
    [in, max_is(m)] short b[][20];
```

## <a name="see-also"></a><span data-ttu-id="981f9-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="981f9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="981f9-122">Atributos de campo</span><span class="sxs-lookup"><span data-stu-id="981f9-122">Field Attributes</span></span>](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[<span data-ttu-id="981f9-123">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="981f9-123">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="981f9-124">**min \_ es**</span><span class="sxs-lookup"><span data-stu-id="981f9-124">**min\_is**</span></span>](min-is.md)
</dt> <dt>

[<span data-ttu-id="981f9-125">**el tamaño \_ es**</span><span class="sxs-lookup"><span data-stu-id="981f9-125">**size\_is**</span></span>](size-is.md)
</dt> </dl>

 

 