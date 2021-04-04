---
title: iid_is (atributo)
description: El atributo \ IID \_ es \ Pointer especifica el IID de la interfaz com a la que apunta un puntero de interfaz.
ms.assetid: 7fb5eb87-15d8-4717-b79a-e8a81f2f7293
keywords:
- iid_is el atributo MIDL
topic_type:
- apiref
api_name:
- iid_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e94c6f46a6828e81817e45ff6eb6eb8245b00a61
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076580"
---
# <a name="iid_is-attribute"></a><span data-ttu-id="ef232-104">el \_ atributo IID es</span><span class="sxs-lookup"><span data-stu-id="ef232-104">iid\_is attribute</span></span>

<span data-ttu-id="ef232-105">El atributo **\[ IID \_ es \]** Pointer especifica el IID de la interfaz com a la que apunta un puntero de interfaz.</span><span class="sxs-lookup"><span data-stu-id="ef232-105">The **\[iid\_is\]** pointer attribute specifies the IID of the COM interface pointed to by an interface pointer.</span></span>

``` syntax
[ iid_is(limited-expression) ]
```

## <a name="parameters"></a><span data-ttu-id="ef232-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ef232-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef232-107">*Limited-Expression*</span><span class="sxs-lookup"><span data-stu-id="ef232-107">*limited-expression*</span></span> 
</dt> <dd>

<span data-ttu-id="ef232-108">Especifica una expresión del lenguaje C.</span><span class="sxs-lookup"><span data-stu-id="ef232-108">Specifies a C-language expression.</span></span> <span data-ttu-id="ef232-109">El compilador MIDL admite expresiones condicionales, expresiones lógicas, expresiones relacionales y expresiones aritméticas.</span><span class="sxs-lookup"><span data-stu-id="ef232-109">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="ef232-110">MIDL no permite invocaciones de función en expresiones y no permite operadores de incremento y decremento.</span><span class="sxs-lookup"><span data-stu-id="ef232-110">MIDL does not allow function invocations in expressions and does not allow increment and decrement operators.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ef232-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ef232-111">Remarks</span></span>

<span data-ttu-id="ef232-112">Puede usar **\[ IID \_ está \]** en listas de atributos para los parámetros de función y para los miembros de estructura o Unión.</span><span class="sxs-lookup"><span data-stu-id="ef232-112">You can use **\[iid\_is\]** in attribute lists for function parameters and for structure or union members.</span></span> <span data-ttu-id="ef232-113">El código auxiliar usa el IID para determinar cómo calcular las referencias del puntero de interfaz.</span><span class="sxs-lookup"><span data-stu-id="ef232-113">The stubs use the IID to determine how to marshal the interface pointer.</span></span> <span data-ttu-id="ef232-114">Esto resulta útil para un puntero de interfaz que se escribe como un parámetro de clase base.</span><span class="sxs-lookup"><span data-stu-id="ef232-114">This is useful for an interface pointer that is typed as a base class parameter.</span></span>

<span data-ttu-id="ef232-115">Los archivos que utilizan el **\[ IID \_ es \]** deben compilarse con el compilador MIDL en el modo predeterminado, que no usa el modificador [**/OSF**](-osf.md)</span><span class="sxs-lookup"><span data-stu-id="ef232-115">Files that use the **\[iid\_is\]** attribute must be compiled with the MIDL compiler in default mode, that is not using the [**/osf**](-osf.md) switch.</span></span>

## <a name="examples"></a><span data-ttu-id="ef232-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ef232-116">Examples</span></span>

``` syntax
HRESULT    CreateInstance( 
    [in] REFIID riid, 
    [out, iid_is(riid)] IUnknown ** ppvObject);
```

## <a name="see-also"></a><span data-ttu-id="ef232-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="ef232-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef232-118">**objeto**</span><span class="sxs-lookup"><span data-stu-id="ef232-118">**object**</span></span>](object.md)
</dt> <dt>

[<span data-ttu-id="ef232-119">**uuid**</span><span class="sxs-lookup"><span data-stu-id="ef232-119">**uuid**</span></span>](uuid.md)
</dt> </dl>

 

 




